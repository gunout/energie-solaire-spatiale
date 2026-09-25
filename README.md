# ☀️ Énergie Solaire Spatiale (SBSP) — Simulateur Expert

> **Simulateur scientifique complet** pour l'analyse de systèmes d'énergie solaire spatiale (Space-Based Solar Power) : calculs physiques avancés (modèles UIT officiels), optimisation multi-objectifs (Pareto), simulation probabiliste (Monte-Carlo), contraintes de sécurité (ICNIRP) et Business Plan stratégique intégré.

[![HTML5](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS-3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Made in France](https://img.shields.io/badge/Made%20in-France-0055A4)](https://www.gouvernement.fr/)

---

## 📋 Sommaire

- [Présentation](#-présentation)
- [Points clés](#-points-clés)
- [Fonctionnalités](#-fonctionnalités)
- [Démo en ligne](#-démo-en-ligne)
- [Installation](#-installation)
- [Utilisation](#-utilisation)
- [Architecture technique](#-architecture-technique)
- [Modèles physiques](#-modèles-physiques)
- [Calculs détaillés](#-calculs-détaillés)
- [Business Plan](#-business-plan)
- [Structure du projet](#-structure-du-projet)
- [Performances](#-performances)
- [Compatibilité](#-compatibilité)
- [Contribuer](#-contribuer)
- [Licence](#-licence)
- [Auteur](#-auteur)
- [Remerciements](#-remerciements)
- [Références](#-références)

---

## 🎯 Présentation

Ce projet est un **simulateur scientifique avancé** permettant d'analyser la viabilité technique et économique d'un système d'**Énergie Solaire Spatiale (SBSP)**.

Le SBSP consiste à :
1. **Capter** l'énergie solaire en orbite via des panneaux photovoltaïques
2. **Convertir** cette énergie en micro-ondes
3. **Transmettre** le faisceau vers une rectenna au sol
4. **Reconvertir** en électricité pour le réseau

Ce simulateur calcule les **rendements de conversion** à chaque étape, les **pertes de propagation** (atmosphère, pluie, nuages), les **contraintes de sécurité** (ICNIRP) et évalue la **rentabilité financière** (LCOE, VAN, TRI).

---

## 🔑 Points clés

| Indicateur | Valeur |
|---|---|
| **Rendement GEO réaliste** | ~1,3 % |
| **Rendement LEO réaliste** | 15–20 % |
| **Rendement Mars (GEO)** | ~24 % |
| **LCOE civil** | 4 965 €/MWh |
| **LCOE militaire** | 1 803 €/MWh |
| **Marché adressable** | 280 Md€ |
| **CAPEX militaire** | 1 700 M€ |
| **ROI militaire** | 3 ans (bénéfices indirects) |

> ⚠️ **Conclusion principale** : le SBSP **n'est pas compétitif** pour la production terrestre civile (100× plus cher que le solaire au sol), mais présente un **intérêt stratégique majeur** pour les applications **militaires, spatiales et isolées**.

---

## ✨ Fonctionnalités

### 🛰 Simulateur Satellite (modèle expert UIT)

- **Modèles UIT officiels** :
  - `ITU-R P.676-13` — Atténuation gazeuse (modèle à 3 raies O₂ + H₂O)
  - `ITU-R P.838-3` — Atténuation pluie (coefficients k et α)
  - `ITU-R P.840` — Atténuation nuages (K_l × L)
  - `ITU-R P.618` — Scintillation troposphérique
- **Efficacité d'interception Goubau** : `η = 1 − exp(−τ²)`
- **Tache de diffraction Airy** : `θ = 1,22·λ/D`
- **Bilan de liaison complet** (Friis en dBW)
- **Vérification ICNIRP** dynamique
- **Graphique** : rendement vs altitude (échelle logarithmique)

### 🚁 Simulateur Drone (MPT)

- **Modèle Two-Ray** (sol + LOS)
- **Atténuation gaz** ITU-R P.676
- **Effet Doppler** et temps de cohérence
- **Bilan thermique** ΔT
- **Marge de liaison** avec seuils de décision
- **Graphique** : marge vs distance

### ⚡ Production électrique

- **LCOE actualisé** (formule IEA)
- **VAN / TRI / Payback**
- **Analyse de sensibilité**
- **Graphique** : production et profit cumulés

### 🔬 Conception optimale MPT

- **Amplificateur GaN classe F⁻¹** (76 %)
- **Faisceau Flat-Top** (Woodward-Lawson)
- **Rectenna métasurface + GaAs Schottky**
- **Signal pulsé** à haut PAPR
- **Graphique** : rendements des 4 étages

### 🌍 Constellation LEO vs GEO

- **Orbites képlériennes** : `T = 2π√(a³/μ)`
- **Temps de passage** et **disponibilité**
- **Gain FSPL** vs GEO (36 dB)
- **Graphique** : fenêtres de visibilité sur 24h

### 🔴 Faisceau laser 1064 nm

- **FSPL optique** : `20·log₁₀(4πd/λ)`
- **Divergence** et **tache au sol**
- **Loi de Kruse** pour l'atténuation atmosphérique
- **Sécurité laser** (classes ICNIRP)

### 📊 Optimisation Pareto

- **500 solutions** aléatoires
- **Front de Pareto** (non-dominées)
- **Knee point** (meilleur compromis)
- **3 objectifs** : rendement, CAPEX, masse
- **Graphique** : rendement vs CAPEX (scatter)

### 🌫 Turbulence Hufnagel-Valley

- **Profil Cn²(h)** complet
- **Paramètre de Fried r₀**
- **Angle isoplanétique θ₀**
- **Temps de Greenwood τ₀**
- **Graphique** : profil Cn²(h) en log-log

### 🎲 Monte-Carlo

- **500 à 10 000 tirages**
- **Box-Muller** pour gaussienne
- **Statistiques** : μ, σ, P5, P95
- **Corrélations** paramètre → rendement
- **Graphique** : distribution du rendement

### 🛡 Zones d'exclusion ICNIRP

- **Limites 1998/2020** (public/travailleurs)
- **Rayons d'exclusion** calculés
- **Zones graphiques** (doughnut)
- **Mise à jour dynamique** avec le satellite

### 💼 Business Plan complet

- **Résumé exécutif** (chiffres clés, marché)
- **Analyse financière** (CAPEX, OPEX, LCOE, VAN, TRI)
- **4 scénarios** (militaire, civil, lunaire, martien)
- **Feuille de route** (4 phases, 102 200 M€)
- **SWOT** et **Monte-Carlo**
- **Graphiques** : cash-flow, CAPEX, budget, financement

---

## 🌐 Démo en ligne

🔗 **Version en ligne** : [https://gunout.github.io/energie-solaire-spatiale/](https://gunout.github.io/energie-solaire-spatiale/)

### Captures d'écran

| Satellite | Drone |
|---|---|
| ![Satellite](docs/screenshots/satellite.png) | ![Drone](docs/screenshots/drone.png) |

| Business Plan | Pareto |
|---|---|
| ![Business Plan](docs/screenshots/business-plan.png) | ![Pareto](docs/screenshots/pareto.png) |

---

## 🚀 Installation

### Prérequis

- **Navigateur moderne** : Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Connexion Internet** (pour Chart.js via CDN)

### Installation locale

```bash
# Cloner le dépôt
git clone https://github.com/gunout/energie-solaire-spatiale.git
cd energie-solaire-spatiale

# Ouvrir dans le navigateur (3 options)

# Option 1 : double-clic sur index.html
open index.html

# Option 2 : serveur Python
python3 -m http.server 8000
# → http://localhost:8000

# Option 3 : serveur Node.js
npx serve
# → http://localhost:3000
```

### Installation hors ligne

Pour un usage **sans connexion Internet**, télécharger Chart.js en local :

```bash
# Télécharger Chart.js
curl -o chart.umd.min.js https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js
```

Puis modifier dans `index.html` :

```html
<!-- Remplacer -->
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>

<!-- Par -->
<script src="./chart.umd.min.js"></script>
```

---

## 📖 Utilisation

### Navigation

Le simulateur comporte **12 onglets** :

| Onglet | Description |
|---|---|
| 🛰 **Satellite** | Simulateur satellite GEO/LEO |
| 🚁 **Drone** | Simulateur drone MPT |
| ⚡ **Production** | Analyse économique LCOE |
| 🔬 **Conception** | Optimisation 4 leviers |
| 🌍 **LEO vs GEO** | Comparaison orbites |
| 🔴 **Laser** | Faisceau optique 1064 nm |
| 📊 **Pareto** | Front multi-objectifs |
| 🌫 **Turbulence** | Hufnagel-Valley |
| 🎲 **Monte-Carlo** | Simulation probabiliste |
| 🛡 **ICNIRP** | Zones d'exclusion |
| 💼 **Business Plan** | Analyse stratégique (4 sous-onglets) |
| 📚 **Composants** | Bibliothèque technique |

### Workflow type

1. **Ouvrir** l'onglet Satellite
2. **Ajuster** les sliders (altitude, fréquence, surfaces d'antennes)
3. **Observer** le rendement en temps réel
4. **Cliquer** sur « ⚡ Optimal » pour charger la configuration optimale
5. **Consulter** « 🧮 Détail des calculs » pour comprendre les formules
6. **Exporter** en JSON/CSV pour analyse externe

### Boutons d'action

| Bouton | Description |
|---|---|
| ⚡ **Optimal** | Charge la configuration optimale |
| ⚡ **LEO** | Mode orbite basse |
| ⚠️ **Dégradé** | Configuration dégradée |
| 📥 **JSON** | Export des données en JSON |
| 📥 **CSV** | Export des données en CSV |
| 🧮 **Détail des calculs** | Accordéon avec formules |

---

## 🏗 Architecture technique

### Stack technique

- **Frontend** : HTML5, CSS3 (DSFR Marianne), JavaScript ES6+
- **Graphiques** : Chart.js 4.4 (13 graphiques interactifs)
- **Architecture** : Single Page Application (SPA), **0 dépendance framework**
- **Style** : Design System de l'État Français (DSFR)

### Design Pattern

Gestion centralisée des graphiques pour éviter les fuites mémoire :

```javascript
const charts = {};

function createChart(id, config) {
  destroyChart(id);
  charts[id] = new Chart(canvas, config);
}

function resizeAllVisibleCharts() {
  Object.keys(charts).forEach(id => {
    const canvas = document.getElementById(id);
    if (canvas && canvas.offsetParent !== null) {
      charts[id].resize();
    }
  });
}
```

### Optimisations

- **Debounce** sur sliders (150 ms)
- **Destroy + recreate** graphiques (pas de fuite)
- **Resize conditionnel** (visible uniquement)
- **Pas de framework** (0 dépendance npm)
- **Chargement différé** des graphiques par onglet

---

## 🔬 Modèles physiques

### Satellite

| Modèle | Formule | Source |
|---|---|---|
| FSPL | `20·log₁₀(d) + 20·log₁₀(f) + 92,45` | Friis |
| Gaz O₂/H₂O | `γ = f(P, f, ρ)` | ITU-R P.676-13 |
| Pluie | `γ_R = k·R^α` | ITU-R P.838-3 |
| Nuages | `A = K_l·L/sin(θ)` | ITU-R P.840 |
| Scintillation | `σ = 3,5·10⁻⁴·N_wet·f^(7/12)/sin(θ)^1,2` | ITU-R P.618 |
| Gain antenne | `G = 10·log₁₀(η·(πD/λ)²)` | Théorie |
| Interception | `η = 1 − exp(−τ²)` | Goubau |
| Tache Airy | `θ = 1,22·λ/D` | Diffraction |
| Densité | `ρ = P_nette / (π·(D_tache/2)²)` | — |

### Drone

| Modèle | Formule |
|---|---|
| Distance slant | `d = √(h² + D²)` |
| Two-Ray | `Γ = (sinθ − √(ε_r−cos²θ))/(sinθ + √(ε_r−cos²θ))` |
| Doppler | `f_d = f·v/c` |
| Thermique | `ΔT = P_diss/(h·A)` |
| Marge | `Marge = P_rx(dBm) − 10·log₁₀(P_conso)` |

### Conception

| Modèle | Formule |
|---|---|
| Classe F⁻¹ | `η = 1/(1 + (V_sat/V_dd)·π/2)` |
| Woodward-Lawson | `F(θ) = Σ aₙ·sinc(...)` |
| Diode Schottky | `f_c = 1/(2πR_s·C_j)` |
| PAPR optimal | `10·log₁₀(V_br/V_seuil) − 3` |

### Turbulence Hufnagel-Valley

| Paramètre | Formule |
|---|---|
| Profil Cn²(h) | `0,00594·(v/27)²·h¹⁰·exp(−h/1000) + 2,7×10⁻¹⁶·exp(−h/1500) + A·exp(−h/100)` |
| Fried r₀ | `[0,423·k²·∫Cn²(h)·dh]^(−3/5)` |
| θ₀ | `[2,91·k²·∫Cn²(h)·h^(5/3)·dh]^(−3/5)` |
| σ_I² | `2,25·k^(7/6)·∫Cn²(h)·h^(5/6)·dh` |

---

## 🧮 Calculs détaillés

### Chaîne de rendement satellite

```
η_global = η_PV × η_DC→RF × η_transmission × η_RF→DC × η_distribution
```

| Étage | Valeur réaliste | Maximum théorique |
|---|---|---|
| PV (III-V 4J) | 40 % | 65 % |
| DC→RF (GaN) | 85 % | 90 % |
| Transmission (GEO) | 2 % | 95 % |
| RF→DC (rectenna) | 90 % | 95 % |
| Distribution | 95 % | 98 % |
| **Global** | **~1,3 %** | **~35 %** |

### Rendement par orbite

| Orbite | Distance | η_transmission | η_global |
|---|---|---|---|
| GEO | 35 786 km | 40 % | 9 % |
| LEO | 550 km | 85 % | 15 % |
| Lune (LLO) | 100 km | 100 % | 24 % |
| Mars (GEO) | 91 410 km | 100 % | 24 % |

### LCOE comparé

| Technologie | LCOE (€/MWh) |
|---|---|
| Solaire au sol | 30–50 |
| Éolien terrestre | 40–70 |
| Éolien offshore | 80–120 |
| Nucléaire EPR | 110–150 |
| **SBSP GEO** | **2 800** |
| **SBSP LEO** | **4 965** |

> ⚠️ Le SBSP est **100× plus cher** que le solaire au sol pour la production civile.

---

## 💼 Business Plan

### Résumé exécutif

| Indicateur | Valeur |
|---|---|
| Marché adressable | 280 Md€ |
| Rendement réaliste | 1,3 % (GEO) — 24 % (Mars) |
| CAPEX militaire | 1 700 M€ |
| OPEX annuel | 65 M€ |
| ROI militaire | 3 ans (bénéfices indirects) |
| LCOE civil | 4 965 €/MWh |
| LCOE solaire (référence) | 40 €/MWh |

### Scénarios comparés

| Scénario | Puissance | Orbite | CAPEX | LCOE | Recommandation |
|---|---|---|---|---|---|
| **Militaire** | 10 MW | LEO | 1 700 M€ | 1 803 €/MWh | ✅ **Prioritaire** |
| Civil | 1 GW | GEO | 100 000 M€ | 4 965 €/MWh | ❌ **Abandonner** |
| Lunaire | 1 MW | LLO | 5 000 M€ | 10 000 €/MWh | ⚠️ **Justifié par mission** |
| Martien | 10 MW | GEO Mars | 20 000 M€ | 8 000 €/MWh | ⚠️ **Justifié par mission** |

### Feuille de route (4 phases)

| Phase | Période | Objectif | Budget |
|---|---|---|---|
| 1. R&D | 2025–2030 | Nanotubes, PV 4J, rectenna | 1 000 M€ |
| 2. Démonstration | 2030–2035 | Satellite 10 kW LEO | 200 M€ |
| 3. Industrialisation | 2035–2045 | Constellation 3×1 MW | 1 000 M€ |
| 4. Déploiement | 2045–2060 | 10 GW orbital + bases | 100 000 M€ |
| **Total** | | | **102 200 M€** |

### Analyse SWOT

| 💪 Forces | ⚠️ Faiblesses |
|---|---|
| Indépendance énergétique | CAPEX très élevé |
| Déployable en heures | LCOE 100× solaire |
| Discrétion (pas de convoi) | Rendement faible |
| 24h/24 (GEO) ou 95 % (LEO) | Dépendance lanceurs |

| 🚀 Opportunités | ⛔ Menaces |
|---|---|
| Coût lancement ↓ (Starship) | Concurrence solaire |
| Constellations LEO | Traité de l'espace |
| Bases lunaires/Mars | Débris spatiaux |
| Zones isolées | Opposition ICNIRP |

---

## 📁 Structure du projet

```
energie-solaire-spatiale/
│
├── index.html                  # Application complète (single-file)
├── README.md                   # Ce fichier
├── LICENSE                     # Licence MIT
├── .gitignore                  # Fichiers ignorés
│
├── docs/                       # Documentation
│   ├── FORMULES.md            # Détail des formules physiques
│   ├── BUSINESS_PLAN.md       # Business plan complet
│   ├── SOURCES.md             # Références scientifiques
│   └── screenshots/           # Captures d'écran
│       ├── satellite.png
│       ├── drone.png
│       ├── pareto.png
│       ├── business-plan.png
│       └── demo.gif
│
└── assets/                     # Ressources optionnelles
    ├── chart.umd.min.js       # Chart.js (hors ligne)
    └── fonts/                 # Polices locales (optionnel)
```

---

## ⚡ Performances

### Temps de chargement

| Métrique | Valeur |
|---|---|
| Chargement initial | < 500 ms |
| Chart.js CDN | ~150 ms |
| Calculs satellite | < 5 ms |
| Mise à jour slider | < 10 ms |
| Monte-Carlo 2 000 tirages | ~200 ms |
| Pareto 500 solutions | ~300 ms |

### Utilisation mémoire

| Composant | Mémoire |
|---|---|
| Page de base | ~5 MB |
| 13 graphiques Chart.js | ~8 MB |
| Données Pareto (500 sol.) | ~1 MB |
| **Total** | **~14 MB** |

---

## 🌐 Compatibilité

### Navigateurs

| Navigateur | Version minimale | Support |
|---|---|---|
| Chrome | 90+ | ✅ Complet |
| Firefox | 88+ | ✅ Complet |
| Safari | 14+ | ✅ Complet |
| Edge | 90+ | ✅ Complet |
| Opera | 76+ | ✅ Complet |

### Technologies

- HTML5 (Canvas, Details, Range input)
- CSS3 (Grid, Flexbox, Variables, Animations)
- JavaScript ES6+ (Arrow functions, Template literals, Destructuring)
- Chart.js 4.4 (via CDN)

---

## 🤝 Contribuer

Les contributions sont **les bienvenues** !

### Étapes

```bash
# 1. Fork le projet
# 2. Cloner votre fork
git clone https://github.com/VOTRE-USERNAME/energie-solaire-spatiale.git

# 3. Créer une branche
git checkout -b feature/nouvelle-fonctionnalite

# 4. Commit
git commit -m "feat: ajout de la fonctionnalité X"

# 5. Push
git push origin feature/nouvelle-fonctionnalite

# 6. Ouvrir une Pull Request
```

### Convention de commit

| Type | Description |
|---|---|
| `feat` | Nouvelle fonctionnalité |
| `fix` | Correction de bug |
| `docs` | Documentation |
| `style` | Formatage |
| `refactor` | Refactoring |
| `test` | Tests |
| `chore` | Maintenance |

### Idées de contributions

- [ ] Mode sombre
- [ ] Export PDF direct
- [ ] Support multilingue (EN, ES, DE)
- [ ] Tests unitaires (Jest)
- [ ] Amélioration modèles physiques
- [ ] Nouveaux scénarios (Lune, Mars, astéroïdes)
- [ ] Comparaison avec d'autres technologies (fusion, hydrogène)

---

## 📄 Licence

Ce projet est sous licence **MIT**.

```
MIT License

Copyright (c) 2026 Gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👤 Auteur

**Gunout**

- 🐙 GitHub : [@gunout](https://github.com/gunout)
- 📦 Projet : [energie-solaire-spatiale](https://github.com/gunout/energie-solaire-spatiale)

---

## 🙏 Remerciements

- **UIT** (Union Internationale des Télécommunications) pour les modèles ITU-R
- **ICNIRP** pour les limites d'exposition
- **NASA** pour les données AM0 (constante solaire)
- **DSFR** pour le design system français
- **Chart.js** pour la librairie de graphiques

---

## 📚 Références

### Modèles UIT

- [ITU-R P.676-13](https://www.itu.int/rec/R-REC-P.676) — Attenuation by atmospheric gases
- [ITU-R P.838-3](https://www.itu.int/rec/R-REC-P.838) — Specific attenuation model for rain
- [ITU-R P.840](https://www.itu.int/rec/R-REC-P.840) — Attenuation due to clouds
- [ITU-R P.618](https://www.itu.int/rec/R-REC-P.618) — Propagation data for Earth-space

### Sécurité

- [ICNIRP Guidelines 2020](https://www.icnirp.org/) — Limites d'exposition
- [Traité de l'espace 1967](https://www.unoosa.org/) — Droit spatial

### SBSP

- Glaser, P. E. (1968) — *Power from the Sun: Its Future*
- NASA (2024) — *Space-Based Solar Power Study*
- ESA (2023) — *SOLARIS Initiative*

---

<div align="center">

**⭐ Si ce projet vous plaît, n'hésitez pas à lui donner une étoile !**

**Fait avec ❤️ par [Gunout](https://github.com/gunout)**

</div>

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>

---

