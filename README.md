# 🇲🇦 Morocco Energy Map
link = https://chhaib22.github.io/Morocco-Energy-Map/
Application web interactive visualisant les **ressources énergétiques renouvelables**
des 12 régions du Maroc, sous forme de **carte choroplèthe** (Leaflet.js).

## 🎯 Objectif
Permettre d'explorer et comparer en un coup d'œil le potentiel **solaire**, **éolien**
et de **biomasse** de chaque région marocaine, avec des couleurs proportionnelles aux valeurs.

## ✅ Fonctionnalités réalisées

### Carte
- Centrée sur le Maroc (lat **31.5**, lng **-7**, zoom **6**).
- Fond de carte sombre (CARTO dark).
- **12 régions** affichées en polygones cliquables (GeoJSON intégré).
- **Carte choroplèthe** : couleur de chaque région selon la couche sélectionnée.

### Couches énergétiques (commutables)
1. ☀️ **Irradiation solaire** (kWh/m²/jour) — échelle jaune → orange → rouge
2. 💨 **Vitesse du vent** (m/s) — échelle bleu clair → bleu → bleu foncé
3. 🌿 **Potentiel biomasse** (TWh/an) — échelle vert clair → vert foncé

### Interactions
- **Clic** sur une région → popup avec le nom + les 3 valeurs énergétiques.
- **Survol** → surbrillance de la région + infobulle de la valeur de la couche active.
- **Boutons de bascule** (Solaire / Éolien / Biomasse) → mise à jour des couleurs de la carte,
  de la légende et de la carte d'information.

### Interface (en français)
- **Barre supérieure** (navbar sombre) : titre + 3 boutons de couche stylés avec état actif.
- **Bas-gauche** : légende dynamique (échelle de couleurs + unité).
- **Bas-droite** : carte d'information détaillant la région cliquée (nom FR + nom AR + 3 métriques).
- Design moderne, responsive (adaptation mobile/tablette).

### Langue
- Interface entièrement en **français**.
- Noms des régions en **français** avec leur équivalent **arabe** officiel.

## 📂 Structure du projet
```
index.html      # Application complète (HTML + CSS + JS dans un seul fichier)
README.md       # Ce fichier
```

## 🔗 Point d'entrée
- `index.html` — page unique de l'application (aucun paramètre d'URL requis).

## 🧱 Modèle de données
Données statiques intégrées dans le JS :

| Champ     | Type   | Unité          | Description                    |
|-----------|--------|----------------|--------------------------------|
| `solar`   | number | kWh/m²/jour    | Irradiation solaire moyenne    |
| `wind`    | number | m/s            | Vitesse moyenne du vent        |
| `biomass` | number | TWh/an         | Potentiel de biomasse          |

Géométries des régions : objet **GeoJSON** simplifié (polygones approximatifs) intégré au script.
Les valeurs énergétiques sont **approximatives et indicatives**.

## 🛠️ Technologies
- HTML5 / CSS3 / JavaScript (vanilla, fichier unique)
- [Leaflet.js 1.9.4](https://leafletjs.com/) via CDN jsDelivr
- Font Awesome 6 + Google Fonts (Inter)
- Tuiles CARTO dark + OpenStreetMap

## 🚧 Améliorations possibles (non implémentées)
- Géométries des régions issues de frontières officielles précises (shapefile).
- Comparaison multi-régions / classement.
- Export des données (CSV) ou impression de la carte.
- Année de référence des données et sources citées.
- Mode clair / sombre commutable.

## 👨‍💻 Auteur
**Mohamed-Amine Chhaib**
- 🎓 DUT Énergies Renouvelables & Efficacité Énergétique — EST Guelmim
- 🔗 [SolarAI Maroc](https://chhaib22.github.io/SolarAI-Maroc/)
- 🐙 [GitHub](https://github.com/chhaib22)

## 🚀 Déploiement
Pour mettre le site en ligne, utilisez l'onglet **Publish** qui publiera le projet
en un clic et fournira l'URL du site.
