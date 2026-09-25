<div align="center">

# ⚡ Énergie Solaire Spatiale — Projet SBSP

**Simulateur scientifique français de production d'énergie par satellite et drone**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
[![SVG](https://img.shields.io/badge/SVG-FFB13B?style=for-the-badge&logo=svg&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/SVG)
[![Zéro dépendance](https://img.shields.io/badge/zéro--dépendance-00c853?style=for-the-badge)](#)

[![Cloudflare Pages](https://img.shields.io/badge/Cloudflare%20Pages-Live-00e5ff?style=for-the-badge&logo=cloudflare&logoColor=white)](https://energie-solaire-spatiale.pages.dev)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Mirror-000091?style=for-the-badge&logo=github&logoColor=white)](https://gunout.github.io/energie-solaire-spatiale)
[![Licence MIT](https://img.shields.io/badge/Licence-MIT-E1000F?style=for-the-badge)](LICENSE)

[![Stars](https://img.shields.io/github/stars/gunout/energie-solaire-spatiale?style=social)](https://github.com/gunout/energie-solaire-spatiale/stargazers)
[![Forks](https://img.shields.io/github/forks/gunout/energie-solaire-spatiale?style=social)](https://github.com/gunout/energie-solaire-spatiale/network/members)
[![Issues](https://img.shields.io/github/issues/gunout/energie-solaire-spatiale?style=flat-square)](https://github.com/gunout/energie-solaire-spatiale/issues)
[![Dernier commit](https://img.shields.io/github/last-commit/gunout/energie-solaire-spatiale?style=flat-square)](https://github.com/gunout/energie-solaire-spatiale/commits/main)
[![Taille du repo](https://img.shields.io/github/repo-size/gunout/energie-solaire-spatiale?style=flat-square)](https://github.com/gunout/energie-solaire-spatiale)

[![Marianne](https://img.shields.io/badge/République-Française-000091?style=flat-square)](#)
[![ICNIRP](https://img.shields.io/badge/Conforme-ICNIRP-18753C?style=flat-square)](#)
[![ITU-R](https://img.shields.io/badge/Modèles-ITU--R%20P.676%20%2F%20P.838-0063CB?style=flat-square)](#)

</div>

---

## 📖 À propos

**Énergie Solaire Spatiale** est un simulateur scientifique open-source qui modélise les deux principales applications du **transport d'énergie sans fil par micro-ondes** (MPT — Microwave Power Transfer) :

- 🛰 **Satellite géostationnaire** — Production solaire spatiale à l'échelle du gigawatt
- 🚁 **Drone multirotor** — Alimentation continue sans fil en vol stationnaire

Le projet intègre les **modèles physiques officiels** utilisés dans l'industrie spatiale :

- **ITU-R P.676** — Atténuation atmosphérique par les gaz
- **ITU-R P.838** — Atténuation par la pluie
- **Limites ICNIRP** — Exposition du public aux champs électromagnétiques
- **Formules de Friis** — Bilan de liaison complet
- **Tache d'Airy** — Diffraction du faisceau

---

## 🎯 Fonctionnalités

### 🛰 Simulateur Satellite

- **10 paramètres ajustables** : altitude, élévation, fréquence, diamètres antennes, surface panneaux, rendements, pluie
- **12 indicateurs calculés en temps réel** : puissance solaire, FSPL, gains, bilan de liaison, densité au sol, puissance nette, foyers alimentés
- **Bloc de configuration optimale** avec 14 étapes de calcul détaillées
- **Alertes ICNIRP dynamiques** (densité > 10 W/m²)

### 🚁 Simulateur Drone

- **9 paramètres ajustables** : altitude, distance, puissance RF, fréquence, diamètres antennes, consommation, vent, rendement rectenna
- **12 indicateurs calculés** : distance slant, FSPL, gains, puissance reçue, marge de liaison, EIRP, densité, autonomie, effet Doppler
- **Animation visuelle en SVG** : drone stable, instable, ou en chute selon la marge
- **Graphique Canvas** : marge de liaison en fonction de la distance
- **Comparaison de fréquences** : 2,4 / 5,8 / 10 / 24 / 30 GHz avec portées maximales

### ⚡ Simulateur de Production

- **Modèle économique complet** : CAPEX, OPEX, ROI, LCOE
- **Impact environnemental** : CO₂ évité, arbres équivalents, voitures retirées
- **Graphique cumulé sur 30 ans** : production + profit
- **Mode comparaison A/B** : deux configurations côte à côte

### 📚 Bibliothèque de composants

- **5 fiches techniques** : photovoltaïque spatial, convertisseur DC→RF, rectenna, batterie, phased array
- **Filtres par catégorie** : Satellite / Drone / Commun
- **Tableau récapitulatif** avec niveaux TRL (Technology Readiness Level)

---

## 📊 État du projet

<div align="center">

| Module | État | Détails |
|:-------|:----:|:--------|
| **Simulateur Satellite** | 🟢 **Stable** | 10 curseurs · 12 indicateurs · 14 étapes de calcul |
| **Simulateur Drone** | 🟢 **Stable** | 9 curseurs · 12 indicateurs · 3 presets |
| **Simulateur Production** | 🟢 **Stable** | Modèle économique complet + comparaison A/B |
| **Bibliothèque Composants** | 🟢 **Stable** | 5 fiches + filtres + TRL |
| **Animation Drone SVG** | 🟢 **Fonctionnelle** | Stable / instable / chute |
| **Graphiques Canvas** | 🟢 **Fonctionnels** | Marge vs distance + Production cumulée |
| **Design DSFR** | 🟢 **Conforme** | Charte Marianne officielle |
| **Responsive** | 🟢 **Testé** | Mobile / tablette / desktop |
| **Dépendances** | ⚪ **Aucune** | 100 % HTML/CSS/JS/SVG pur |

</div>

### 🎯 Matrice de progression

```
🛰 Satellite      [██████████████████████] 100 %  · Complet & documenté
🚁 Drone          [██████████████████████] 100 %  · Complet & animé
⚡ Production     [█████████████████████░]  95 %  · Modèle économique complet
📚 Composants     [███████████████████░░░]  88 %  · 5 fiches documentées
🎨 Design DSFR    [██████████████████████] 100 %  · Charte Marianne respectée
📄 Documentation  [███████████████████░░░]  90 %  · README + fiches inline
🧪 Tests          [██████████░░░░░░░░░░░░]  45 %  · Validation manuelle
🌍 i18n (EN/FR)   [█████░░░░░░░░░░░░░░░░░]  25 %  · Français uniquement
```

### 📋 Légende des états

| Symbole | Signification |
|:-------:|:--------------|
| 🟢 | **Stable / Complet** — Prêt pour utilisation |
| 🟡 | **En cours** — Fonctionnel mais à enrichir |
| 🔴 | **Cassé / Bloqué** — Nécessite une correction |
| 🔵 | **Planifié** — Sur la roadmap |
| ⚪ | **Non applicable** — Sans objet |

### 🗺 Feuille de route

- [x] Simulateur satellite avec modèles ITU-R
- [x] Simulateur drone avec animation SVG
- [x] Simulation de production économique
- [x] Bibliothèque de composants techniques
- [x] Design Marianne (DSFR)
- [x] Alertes ICNIRP dynamiques
- [x] Graphiques Canvas temps réel
- [x] Mode comparaison A/B
- [ ] Version anglaise (EN)
- [ ] Export PDF des rapports
- [ ] Sauvegarde des paramètres dans l'URL
- [ ] API REST pour intégration externe
- [ ] Tests automatisés (Jest + Playwright)

---

## 🚀 Démarrage rapide

### Option 1 — Consultation en ligne (recommandé)

Ouvrez directement le site déployé :

👉 **[energie-solaire-spatiale.pages.dev](https://energie-solaire-spatiale.pages.dev)**

### Option 2 — En local

```bash
# Cloner le dépôt
git clone https://github.com/gunout/energie-solaire-spatiale.git
cd energie-solaire-spatiale

# Lancer un serveur local
python3 -m http.server 8000
# → http://localhost:8000
```

### Option 3 — Fichier unique

Téléchargez `index.html` et ouvrez-le dans n'importe quel navigateur moderne. **Aucun build, aucune dépendance.**

---

## 🧮 Modèles physiques implémentés

### Satellite

| # | Formule | Utilisation |
|:-:|:--------|:------------|
| 1 | `d = h / sin(θ)` | Distance effective avec élévation |
| 2 | `P_solar = 1361 × S × η` | Puissance solaire captée (AM0) |
| 3 | `FSPL = 20·log₁₀(d) + 20·log₁₀(f) + 92,45` | Perte en espace libre |
| 4 | `A_gaz ≈ 0,005·f^1,1 · 10/sin(θ)` | Atténuation gazeuse (ITU-R P.676) |
| 5 | `γ_R = k·R^α` | Atténuation pluie (ITU-R P.838) |
| 6 | `G = 10·log₁₀(η·(πD/λ)²)` | Gain antenne parabolique |
| 7 | `P_rx = P_tx + G_Tx + G_Rx − FSPL − A_atm` | Bilan de liaison |
| 8 | `θ_Airy = 1,22·λ/D` | Tache de diffraction |
| 9 | `ρ = P/(π·(θd/2)²)` | Densité de puissance au sol |

### Drone

| # | Formule | Utilisation |
|:-:|:--------|:------------|
| 1 | `d = √(h² + D²)` | Distance slant 3D |
| 2 | `FSPL = 20·log₁₀(d) + 20·log₁₀(f) + 92,45` | Perte en espace libre |
| 3 | `G = 10·log₁₀(η·(πD/λ)²)` | Gain antenne |
| 4 | `EIRP = P_tx + G_Tx` | Puissance isotrope rayonnée |
| 5 | `Marge = P_utile − P_conso` | Marge de liaison |
| 6 | `f_D = f·v/c` | Effet Doppler |

### Production

| # | Formule | Utilisation |
|:-:|:--------|:------------|
| 1 | `E = P × 8760 × η_dispo` | Production annuelle |
| 2 | `CO₂ = E × 0,446` | CO₂ évitée (mix EU) |
| 3 | `LCOE = (CAPEX + ΣOPEX) / (E × durée)` | Coût actualisé |
| 4 | `ROI = (profit × durée − CAPEX) / CAPEX` | Retour sur investissement |

---

## 📁 Structure du projet

```
energie-solaire-spatiale/
├── index.html              ← Application complète (HTML + CSS + JS + SVG)
├── README.md               ← Ce fichier
├── LICENSE                 ← MIT
└── assets/
    └── apercu.png          ← Capture d'écran pour le README
```

**Le projet tient en un seul fichier HTML autonome de ~50 ko.** Aucun framework, aucune dépendance npm, aucun build.

---

## 🎨 Aperçu de l'interface

<div align="center">

| Onglet Satellite | Onglet Drone | Onglet Production |
|:---:|:---:|:---:|
| Scène orbitale SVG | Drone animé SVG | Graphiques Canvas |
| 12 indicateurs | Animation de chute | Modèle économique |
| Bloc optimal 14 étapes | Tableau fréquences | Comparaison A/B |

</div>

**Design conforme à la charte de l'État français (DSFR) :**
- Bandeau Marianne tricolore
- Palette officielle : bleu `#000091`, rouge `#E1000F`, blanc
- Typographie Marianne
- Boutons style DSFR
- Fil d'Ariane institutionnel
- Footer 4 colonnes

---

## 🛠 Stack technique

<div align="center">

| Technologie | Utilisation |
|:-----------:|:------------|
| ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) | Structure sémantique |
| ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) | Design DSFR, animations, print |
| ![JavaScript](https://img.shields.io/badge/-Vanilla%20JS-F7DF1E?style=flat-square&logo=javascript&logoColor=black) | Simulateurs, calculs, Canvas |
| ![SVG](https://img.shields.io/badge/-SVG-FFB13B?style=flat-square&logo=svg&logoColor=white) | Illustrations vectorielles animées |

</div>

**Aucune dépendance externe.** Pas de CDN, pas de Google Fonts, pas de jQuery. Le fichier s'ouvre directement dans n'importe quel navigateur moderne.

---

## 🌐 Compatibilité

| Navigateur | Version minimale | Support |
|:-----------|:----------------:|:-------:|
| **Chrome** | 90 | ✅ Complet |
| **Firefox** | 88 | ✅ Complet |
| **Safari** | 14 | ✅ Complet |
| **Edge** | 90 | ✅ Complet |
| **Mobile iOS** | 14 | ✅ Responsive |
| **Mobile Android** | 10 | ✅ Responsive |

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment procéder :

```bash
# 1. Forkez le dépôt sur GitHub

# 2. Clonez votre fork
git clone https://github.com/VOTRE-USER/energie-solaire-spatiale.git

# 3. Créez une branche
git checkout -b fonctionnalite/nouvelle-fiche

# 4. Faites vos modifications et commitez
git commit -m "Ajout fiche composant XYZ"

# 5. Poussez sur votre fork
git push origin fonctionnalite/nouvelle-fiche

# 6. Ouvrez une Pull Request
```

### Bonnes pratiques

- ✅ Une **fiche** = un accordéon dans l'onglet Composants
- ✅ Une **formule** = un bloc `<code>` dans le `<details>` correspondant
- ✅ Les **commentaires** dans le code sont en français
- ✅ Les **badges** sont générés par [shields.io](https://shields.io)
- ✅ Le **design** respecte la charte DSFR (couleurs Marianne)
- ✅ Les **calculs** suivent les recommandations ITU-R et ICNIRP

---

## 📚 Sources et références

- **ITU-R P.676-12** — Attenuation by atmospheric gases
- **ITU-R P.838-3** — Specific attenuation model for rain
- **ICNIRP 2020** — Guidelines for limiting exposure to electromagnetic fields
- **NASA SSPP** — Space Solar Power Project (Caltech, 2023)
- **Xidian University** — Démonstration drone MPT (2021)
- **JAXA OHISAMA** — Satellite démonstrateur (2025)
- **DSFR** — Système de Design de l'État français

---

## 📜 Licence

Ce projet est distribué sous licence **MIT**. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

Vous êtes libre de :
- ✅ Utiliser le code à des fins commerciales
- ✅ Modifier le code
- ✅ Distribuer le code
- ✅ Utiliser le code à des fins privées

Sous condition de :
- ⚠️ Inclure la licence MIT dans toute copie
- ⚠️ Ne pas tenir les auteurs responsables

---

## 🙏 Remerciements

- **Caltech SSPP** — Mission SSPD-1 (2023)
- **Université Xidian** — Démonstration drone 3,1 h (2021)
- **JAXA OHISAMA** — Satellite démonstrateur (2025)
- **ITU-R** — Recommandations P.676 et P.838
- **ICNIRP** — Limites d'exposition RF
- **DINUM** — Système de Design de l'État français

---

## 📞 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=for-the-badge&logo=github)](https://github.com/gunout)

**Projet SBSP** — Énergie Solaire Spatiale

</div>

---

<div align="center">

### ⭐ Si ce projet vous plaît, laissez une étoile ! ⭐

**République Française** · Projet national d'innovation énergétique

*Dernière mise à jour : 2026*

</div>

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
