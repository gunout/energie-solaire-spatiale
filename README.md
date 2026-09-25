# ☀️ Énergie Solaire Spatiale (SBSP) — Simulateur Expert

> Simulateur scientifique complet pour l'analyse de systèmes d'énergie solaire spatiale (SBSP) : calculs physiques avancés, modèles UIT, Monte-Carlo, optimisation Pareto et Business Plan intégré.

[![HTML5](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML) [![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript) [![Chart.js](https://img.shields.io/badge/Chart.js-4.4-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Sommaire

- [Présentation](#-présentation) · [Fonctionnalités](#-fonctionnalités) · [Installation](#-installation) · [Utilisation](#-utilisation) · [Modèles](#-modèles-physiques) · [Calculs](#-calculs-détaillés) · [Business Plan](#-business-plan) · [Contribuer](#-contribuer) · [Licence](#-licence)

## 🎯 Présentation

Simulateur scientifique avancé permettant d'analyser la viabilité technique et économique d'un système d'Énergie Solaire Spatiale (SBSP) : captation solaire en orbite, conversion en micro-ondes, transmission vers le sol, reconversion en électricité.

**Objectifs** : analyser les rendements réalistes, optimiser la configuration (Pareto), évaluer les risques (Monte-Carlo), vérifier la conformité ICNIRP, chiffrer un Business Plan.

## ✨ Fonctionnalités

**🛰 Satellite (modèle expert UIT)** — Modèles ITU-R P.676-13, P.838-3, P.840, P.618 ; interception Goubau (η = 1 − exp(−τ²)) ; tache Airy (θ = 1,22·λ/D) ; bilan Friis en dBW ; ICNIRP dynamique.

**🚁 Drone (MPT)** — Modèle Two-Ray (sol + LOS) ; atténuation gaz ITU-R P.676 ; effet Doppler ; bilan thermique ΔT ; marge de liaison avec seuils.

**⚡ Production** — LCOE actualisé (formule IEA) ; VAN / TRI / Payback ; analyse de sensibilité.

**🔬 Conception optimale** — Amplificateur GaN classe F⁻¹ (76 %) ; faisceau Flat-Top (Woodward-Lawson) ; rectenna métasurface + GaAs Schottky ; signal pulsé PAPR.

**🌍 LEO vs GEO** — Orbites képlériennes (T = 2π√(a³/μ)) ; temps de passage et disponibilité ; gain FSPL 36 dB.

**🔴 Laser 1064 nm** — FSPL optique 20·log₁₀(4πd/λ) ; divergence ; loi de Kruse.

**📊 Pareto** — 500 solutions aléatoires ; front de Pareto ; knee point (3 objectifs).

**🌫 Turbulence** — Profil Cn²(h) Hufnagel-Valley ; paramètre de Fried r₀ ; angle isoplanétique θ₀.

**🎲 Monte-Carlo** — 500 à 10 000 tirages ; Box-Muller ; statistiques μ, σ, P5, P95.

**🛡 ICNIRP** — Limites 1998/2020 (public/travailleurs) ; rayons d'exclusion ; zones graphiques.

**💼 Business Plan** — Résumé exécutif ; analyse financière ; 4 scénarios ; feuille de route 102 200 M€.

## 🚀 Installation

**Prérequis** : navigateur moderne (Chrome 90+, Firefox 88+, Safari 14+) et connexion Internet (Chart.js via CDN).

**Local** :
```
git clone https://github.com/gunout/energie-solaire-spatiale.git
cd energie-solaire-spatiale
python3 -m http.server 8000
```

**Hors ligne** : télécharger Chart.js puis remplacer le lien CDN.
```
curl -o chart.umd.min.js https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js
```
Remplacer dans `index.html` : `<script src="./chart.umd.min.js"></script>`

## 📖 Utilisation

| Onglet | Description |
|---|---|
| 🛰 Satellite | Simulateur satellite GEO/LEO |
| 🚁 Drone | Simulateur drone MPT |
| ⚡ Production | Analyse économique LCOE |
| 🔬 Conception | Optimisation 4 leviers |
| 🌍 LEO vs GEO | Comparaison orbites |
| 🔴 Laser | Faisceau optique 1064 nm |
| 📊 Pareto | Front multi-objectifs |
| 🌫 Turbulence | Hufnagel-Valley |
| 🎲 Monte-Carlo | Simulation probabiliste |
| 🛡 ICNIRP | Zones d'exclusion |
| 💼 Business Plan | Analyse stratégique |
| 📚 Composants | Bibliothèque technique |

**Workflow** : ouvrir Satellite → ajuster sliders → observer rendement → cliquer « ⚡ Optimal » → consulter « 🧮 Détail » → exporter JSON/CSV.

## 🔬 Modèles physiques

**Satellite** :

| Modèle | Formule | Source |
|---|---|---|
| FSPL | 20·log₁₀(d) + 20·log₁₀(f) + 92,45 | Friis |
| Gaz O₂/H₂O | γ = f(P, f, ρ) | ITU-R P.676-13 |
| Pluie | γ_R = k·R^α | ITU-R P.838-3 |
| Nuages | A = K_l·L/sin(θ) | ITU-R P.840 |
| Scintillation | σ = 3,5·10⁻⁴·N_wet·f^(7/12)/sin(θ)^1,2 | ITU-R P.618 |
| Gain antenne | G = 10·log₁₀(η·(πD/λ)²) | Théorie |
| Interception | η = 1 − exp(−τ²) | Goubau |
| Tache Airy | θ = 1,22·λ/D | Diffraction |

**Drone** : Distance slant d = √(h² + D²) ; Two-Ray Γ = (sinθ − √(ε_r−cos²θ))/(sinθ + √(ε_r−cos²θ)) ; Doppler f_d = f·v/c ; Thermique ΔT = P_diss/(h·A).

**Conception** : Classe F⁻¹ η = 1/(1 + (V_sat/V_dd)·π/2) ; Woodward-Lawson F(θ) = Σ aₙ·sinc(...) ; Diode Schottky f_c = 1/(2πR_s·C_j) ; PAPR optimal 10·log₁₀(V_br/V_seuil) − 3.

## 📁 Structure

```
energie-solaire-spatiale/
├── index.html              # Application complète
├── README.md               # Ce fichier
├── LICENSE                 # Licence MIT
├── .gitignore
├── docs/
│   ├── FORMULES.md
│   ├── BUSINESS_PLAN.md
│   ├── SOURCES.md
│   └── screenshots/
└── assets/
    └── chart.umd.min.js
```

## 🧮 Calculs détaillés

**Chaîne de rendement satellite** : `η_global = η_PV × η_DC→RF × η_transmission × η_RF→DC × η_distribution`

| Étage | Réaliste | Max théorique |
|---|---|---|
| PV (III-V 4J) | 40 % | 65 % |
| DC→RF (GaN) | 85 % | 90 % |
| Transmission (GEO) | 2 % | 95 % |
| RF→DC (rectenna) | 90 % | 95 % |
| Distribution | 95 % | 98 % |
| **Global** | **~1,3 %** | **~35 %** |

**Rendement par orbite** :

| Orbite | Distance | η_transmission | η_global |
|---|---|---|---|
| GEO | 35 786 km | 40 % | 9 % |
| LEO | 550 km | 85 % | 15 % |
| Lune (LLO) | 100 km | 100 % | 24 % |
| Mars (GEO) | 91 410 km | 100 % | 24 % |

**LCOE comparé** : Solaire au sol 30–50 ; Éolien 40–70 ; Nucléaire EPR 110–150 ; SBSP GEO 2 800 ; SBSP LEO 4 965 (€/MWh).

## 💼 Business Plan

**Résumé** : marché 280 Md€ ; rendement 1,3 % (GEO) — 24 % (Mars) ; CAPEX militaire 1 700 M€ ; ROI 3 ans ; LCOE civil 4 965 €/MWh.

**Scénarios** :

| Scénario | Puissance | CAPEX | LCOE | Recommandation |
|---|---|---|---|---|
| Militaire | 10 MW | 1 700 M€ | 1 803 €/MWh | ✅ Prioritaire |
| Civil | 1 GW | 100 000 M€ | 4 965 €/MWh | ❌ Abandonner |
| Lunaire | 1 MW | 5 000 M€ | 10 000 €/MWh | ⚠️ Mission |
| Martien | 10 MW | 20 000 M€ | 8 000 €/MWh | ⚠️ Mission |

**Feuille de route** :

| Phase | Période | Objectif | Budget |
|---|---|---|---|
| 1. R&D | 2025–2030 | Nanotubes, PV 4J | 1 000 M€ |
| 2. Démo | 2030–2035 | Satellite 10 kW LEO | 200 M€ |
| 3. Industrie | 2035–2045 | Constellation 3×1 MW | 1 000 M€ |
| 4. Déploiement | 2045–2060 | 10 GW orbital | 100 000 M€ |
| **Total** | | | **102 200 M€** |

## ⚡ Performances

Chargement < 500 ms ; calculs satellite < 5 ms ; mise à jour slider < 10 ms ; Monte-Carlo 2 000 tirages ~200 ms ; mémoire ~14 MB.

## 🌐 Compatibilité

Chrome 90+ · Firefox 88+ · Safari 14+ · Edge 90+ · Opera 76+.

## 🤝 Contribuer

**Convention de commit** : `feat` · `fix` · `docs` · `style` · `refactor` · `test` · `chore`.

**Idées** : mode sombre, export PDF, multilingue (EN/ES), tests Jest, scénarios Lune/Mars.

## 📄 Licence

MIT License — Copyright (c) 2026 Gunout

## 👤 Auteur

**Gunout** — [@gunout](https://github.com/gunout) · [energie-solaire-spatiale](https://github.com/gunout/energie-solaire-spatiale)

## 🙏 Remerciements

UIT (modèles ITU-R) · ICNIRP (limites) · NASA (AM0) · DSFR (design) · Chart.js (graphiques)

## 📚 Références

**Modèles UIT** : [ITU-R P.676-13](https://www.itu.int/rec/R-REC-P.676) · [ITU-R P.838-3](https://www.itu.int/rec/R-REC-P.838) · [ITU-R P.840](https://www.itu.int/rec/R-REC-P.840) · [ITU-R P.618](https://www.itu.int/rec/R-REC-P.618)

**Sécurité** : [ICNIRP 2020](https://www.icnirp.org/) · [Traité espace 1967](https://www.unoosa.org/)

**SBSP** : Glaser (1968) · NASA (2024) · ESA SOLARIS (2023)

---

<div align="center">

**⭐ Si ce projet vous plaît, n'hésitez pas à lui donner une étoile !**

Fait avec ❤️ par [Gunout](https://github.com/gunout)

</div>

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
