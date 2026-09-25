<div align="center">

# 🛰 Énergie Solaire Spatiale — Projet SBSP

**Simulateurs physiques avancés · Satellite · Drone · Bibliothèque technique**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
[![SVG](https://img.shields.io/badge/SVG-FFB13B?style=for-the-badge&logo=svg&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/SVG)
[![Zéro dépendance](https://img.shields.io/badge/zéro--dépendance-00ff88?style=for-the-badge)](#)

[![Cloudflare Pages](https://img.shields.io/badge/Cloudflare%20Pages-En%20ligne-00e5ff?style=for-the-badge&logo=cloudflare&logoColor=white)](https://sbsp.pages.dev)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Miroir-ff10f0?style=for-the-badge&logo=github&logoColor=white)](https://gunout.github.io/sbsp)
[![Licence](https://img.shields.io/badge/Licence-MIT-ffb800?style=for-the-badge)](LICENSE)

[![Étoiles](https://img.shields.io/github/stars/gunout/sbsp?style=social)](https://github.com/gunout/sbsp/stargazers)
[![Forks](https://img.shields.io/github/forks/gunout/sbsp?style=social)](https://github.com/gunout/sbsp/network/members)
[![Issues](https://img.shields.io/github/issues/gunout/sbsp?style=flat-square)](https://github.com/gunout/sbsp/issues)
[![Dernier commit](https://img.shields.io/github/last-commit/gunout/sbsp?style=flat-square)](https://github.com/gunout/sbsp/commits/main)

</div>

---

## 📖 À propos

**SBSP (Space-Based Solar Power)** est une plateforme éducative interactive qui modélise les deux principales applications du **transport d'énergie sans fil par micro-ondes** :

- 🛰 **Satellite en orbite géostationnaire** — Production solaire spatiale à l'échelle du gigawatt
- 🚁 **Drone en vol** — Alimentation sans fil d'un drone multirotor (banc d'essai des technologies orbitales)

Le projet combine **illustrations SVG animées**, **simulateurs physiques temps réel** (plus de 40 formules : FSPL, ITU-R P.676, ITU-R P.838, Airy, ICNIRP…) et une **bibliothèque technique complète** de composants experts.

---

## 📊 État du projet

<div align="center">

### 🚦 Vue d'ensemble

| Composant | État | Détails |
|:----------|:----:|:--------|
| **Onglet Satellite** | 🟢 **Stable** | Scène SVG + simulateur 12 paramètres / 21 indicateurs |
| **Onglet Drone** | 🟢 **Stable** | Scène SVG + simulateur 8 paramètres / 18 indicateurs |
| **Onglet Composants** | 🟢 **Stable** | 13 fiches techniques + filtres + impression |
| **Simulateur Satellite** | 🟢 **Complet** | FSPL, ITU-R P.676, P.838, bilan de liaison, ICNIRP |
| **Simulateur Drone** | 🟢 **Complet** | Distance 3D, pénalité vent, autonomie, densité |
| **Export PDF** | 🟢 **Fonctionnel** | Impression stylée avec accordéons ouverts |
| **Responsive** | 🟢 **Testé** | Mobile / tablette / ordinateur |
| **Dépendances externes** | ⚪ **Aucune** | 100 % HTML/CSS/JS/SVG pur |

</div>

### 🎯 Matrice de progression

```
🛰 Satellite      [████████████████████░░]  95 %  · Simulateur complet
🚁 Drone          [██████████████████████] 100 %  · Stable & documenté
📚 Bibliothèque   [███████████████████░░░]  88 %  · 13 fiches
🎨 Design         [████████████████████░░]  95 %  · Thème néon / espace
📄 Documentation  [██████████████████░░░░]  90 %  · README + fiches en ligne
🧪 Tests          [██████████░░░░░░░░░░░░]  45 %  · Validation manuelle
🌍 Internationalisation  [█████░░░░░░░░░░░░░░░░░]  25 %  · Français uniquement
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

- [x] Onglet Satellite avec scène SVG animée
- [x] Onglet Drone avec scène SVG animée
- [x] Simulateur satellite — modèle physique complet
- [x] Simulateur drone — modèle physique complet
- [x] Bibliothèque de 13 fiches composants
- [x] Bouton Export PDF / Impression
- [x] Design responsive
- [ ] Version anglaise (EN)
- [ ] Graphiques de courbes (rendement vs distance)
- [ ] Sauvegarde des paramètres dans l'URL
- [ ] Mode comparaison côte à côte (Satellite vs Drone)
- [ ] Tests automatisés (Jest + Playwright)

---

## ⚡ Démarrage rapide

### Option 1 — Déploiement en 30 secondes

1. **Forkez** ce dépôt
2. Connectez-le à **Cloudflare Pages** ou **GitHub Pages**
3. C'est en ligne ✅

### Option 2 — En local

```bash
# Cloner le dépôt
git clone https://github.com/gunout/sbsp.git
cd sbsp

# Lancer un serveur local
python3 -m http.server 8000

# → http://localhost:8000
```

### Option 3 — En un seul fichier

Copiez le contenu de `index.html` dans un fichier local et ouvrez-le dans un navigateur. **Aucun build, aucune dépendance.**

---

## 🧮 Modèles physiques implémentés

### 🛰 Satellite

| # | Formule | Utilisation |
|:-:|:--------|:------------|
| 1 | `d = h / sin(θ)` | Distance effective avec angle d'élévation |
| 2 | `E = E₀ × (1 − 0,02)^n` | Dégradation des panneaux sur 15 ans |
| 3 | `P = E × S × η` | Puissance solaire captée |
| 4 | `FSPL = 20·log₁₀(d) + 20·log₁₀(f) + 92,45` | Perte en espace libre |
| 5 | `A_gaz ≈ 0,005·f^1,1` | Atténuation gazeuse (ITU-R P.676) |
| 6 | `γ_R = k·R^α` | Atténuation pluie (ITU-R P.838) |
| 7 | `G = 10·log₁₀(η·(πD/λ)²)` | Gain antenne parabolique |
| 8 | `θ = 1,22·λ/D` | Largeur de faisceau (Airy) |
| 9 | `P_rx = P_tx + G_Tx + G_Rx − FSPL − A_atm` | Bilan de liaison |
| 10 | `ρ = P/(π·(θd/2)²)` | Densité au sol |
| 11 | `S_min = P/10` | Surface minimale ICNIRP |
| 12 | `CO₂ = P·8760·0,5/1000` | CO₂ évité annuel |

### 🚁 Drone

| # | Formule | Utilisation |
|:-:|:--------|:------------|
| 1 | `d = √(h² + dist²)` | Distance 3D émetteur-drone |
| 2 | `FSPL = 20·log₁₀(d) + 20·log₁₀(f) + 92,45` | Perte en espace libre |
| 3 | `G = 10·log₁₀(η·(πD/λ)²)` | Gain réseau phasé |
| 4 | `ΔP = 0,5·v²` | Pénalité vent sur consommation |
| 5 | `T = (Capacité / P_eff) × 60` | Autonomie sans faisceau |

---

## 📁 Structure du projet

```
sbsp/
├── index.html              ← Application complète (HTML + CSS + JS)
├── README.md               ← Ce fichier
├── LICENSE                 ← MIT
└── assets/
    └── apercu.png          ← Capture d'écran pour les métadonnées
```

---

## 🎨 Aperçu

<div align="center">

| Onglet Satellite | Onglet Drone | Bibliothèque |
|:----------------:|:------------:|:------------:|
| Scène orbitale | Faisceau vert animé | 13 fiches techniques |
| 21 indicateurs | 18 indicateurs | Filtres + PDF |
| 12 curseurs | 8 curseurs | Accordéons |

</div>

---

## 🛠 Pile technique

<div align="center">

| Technologie | Utilisation |
|:-----------:|:------------|
| ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) | Structure sémantique |
| ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) | Thème spatial, animations, styles d'impression |
| ![JS](https://img.shields.io/badge/-JavaScript%20pur-F7DF1E?style=flat-square&logo=javascript&logoColor=black) | Simulateurs, calculs, interactions |
| ![SVG](https://img.shields.io/badge/-SVG-FFB13B?style=flat-square&logo=svg&logoColor=white) | Illustrations vectorielles animées |

</div>

**Aucun framework, aucune dépendance, aucun build.** Le fichier s'ouvre directement dans n'importe quel navigateur moderne.

---

## 🌐 Compatibilité

| Navigateur | Support |
|:-----------|:-------:|
| Chrome ≥ 90 | ✅ Complet |
| Firefox ≥ 88 | ✅ Complet |
| Safari ≥ 14 | ✅ Complet |
| Edge ≥ 90 | ✅ Complet |
| Mobile (iOS / Android) | ✅ Responsive |

---

## 🤝 Contribution

Les contributions sont les bienvenues !

```bash
# 1. Forkez le dépôt
# 2. Créez une branche
git checkout -b fonctionnalite/nouvelle-fiche

# 3. Commitez
git commit -m "Ajout fiche composant XYZ"

# 4. Poussez
git push origin fonctionnalite/nouvelle-fiche

# 5. Ouvrez une Pull Request
```

### Bonnes pratiques

- ✅ Une **fiche** = un accordéon dans l'onglet Composants
- ✅ Une **formule** = un bloc `<code>` dans le `<details>` correspondant
- ✅ Les **badges** sont générés par [shields.io](https://shields.io)
- ✅ Les **commentaires** dans le code sont en français

---

## 📜 Licence

Ce projet est distribué sous licence **MIT**. Voir [LICENSE](LICENSE).

---

## 🙏 Remerciements

- **Caltech SSPP** — Mission SSPD-1 (2023)
- **Université Xidian** — Démonstration drone 3,1 h (2021)
- **JAXA OHISAMA** — Satellite démonstrateur (2025)
- **ITU-R** — Recommandations P.676 (gaz) et P.838 (pluie)
- **ICNIRP** — Limites d'exposition RF

---

## 📞 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=for-the-badge&logo=github)](https://github.com/gunout)

</div>

---

<div align="center">

**⭐ Si ce projet vous plaît, laissez une étoile ! ⭐**

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
