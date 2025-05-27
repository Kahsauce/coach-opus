# Interface Coaching Multi-Sport

Une application React moderne pour la gestion et la planification d'entraînements multi-sport basée sur des principes scientifiques de périodisation et de nutrition sportive.

## 🎯 Objectif

Cette interface de coaching permet de générer automatiquement des plans d'entraînement personnalisés pour des sportifs pratiquant plusieurs disciplines (football vétéran, triathlon, trail, musculation) en appliquant les principes scientifiques de :

- **Périodisation** : Macrocycles, mésocycles et microcycles
- **Nutrition sportive** : Calculs BMR, NAP, macronutriments
- **Gestion des blessures** : Prévention et adaptation
- **Règle 80/20** : Répartition intensité/volume

## 🏃‍♂️ Sports Supportés

- **Football Vétéran** : Entraînements techniques, matchs, récupération
- **Triathlon** : Natation, vélo, course à pied avec enchaînements
- **Trail** : Course en nature, dénivelé, endurance
- **Musculation** : Renforcement fonctionnel, prévention blessures
- **Souplesse/Mobilité** : Récupération active, prévention

## 🧠 Logique Scientifique

### Génération d'Entraînements

L'application utilise un système basé sur des règles scientifiques :

#### Périodisation
- **Préparation Générale** : Endurance de base, volume élevé
- **Préparation Spécifique** : Intensité modérée, spécificité sport
- **Construction** : Haute intensité, pics de forme
- **Affûtage** : Réduction volume, maintien intensité
- **Compétition** : Performance optimale
- **Récupération** : Régénération active

#### Règles Football Vétéran
- J-1 : Entraînement léger/tactique
- J+1 : Récupération active ou repos
- Pas plus de 2 jours consécutifs haute intensité
- Adaptation selon âge et expérience

#### Règle 80/20 Endurance
- 80% du volume en zones 1-2 (endurance de base)
- 20% du volume en zones 4-5 (haute intensité)
- Zone 3 limitée (zone grise)

### Calculs Nutritionnels

#### Métabolisme de Base (BMR)
```
Hommes: BMR = 10 × poids + 6.25 × taille - 5 × âge + 5
Femmes: BMR = 10 × poids + 6.25 × taille - 5 × âge - 161
```

#### Niveau d'Activité Physique (NAP)
- Facteur de base : 1.2 (sédentaire)
- Ajustement selon sport et intensité
- Football match : +0.4/heure
- Course intense : +0.35/heure
- Vélo modéré : +0.2/heure

#### Macronutriments
- **Protéines** : 1.6-2.0g/kg (sportifs vétérans)
- **Glucides** : 3-8g/kg selon intensité
- **Lipides** : 0.8-1.2g/kg (25-30% calories)

## 🖥️ Fonctionnalités

### 📊 Tableau de Bord
- Vue d'ensemble des métriques du jour
- Séances planifiées et charge d'entraînement
- Objectifs nutritionnels calculés
- Conseils personnalisés

### 🏋️ Plan d'Entraînement
- Génération automatique des microcycles
- Détail des séances par sport
- Adaptation selon événements
- Suivi RPE et sensations

### 🥗 Plan Nutritionnel
- Calculs personnalisés BMR/NAP
- Répartition macronutriments
- Timing nutritionnel péri-entraînement
- Base de recettes adaptées

### 📅 Calendrier
- Gestion des événements sportifs
- Priorités A, B, C
- Interface drag & drop (à venir)
- Synchronisation avec planification

### 👤 Profil Utilisateur
- Données anthropométriques
- Expérience par sport
- Objectifs et disponibilité
- Matériel disponible

### 📈 Analyses
- Statistiques d'entraînement
- Évolution RPE et charge
- Répartition par sport
- Graphiques interactifs

## 🛠️ Technologies

- **React 18** avec TypeScript
- **Material-UI v5** pour l'interface
- **Date-fns** pour la gestion des dates
- **Recharts** pour les graphiques
- **Day.js** pour les composants de date

## 🚀 Installation

```bash
# Cloner le repository
git clone [url-du-repo]

# Installer les dépendances
cd coaching-interface
npm install

# Lancer l'application
npm start
```

## 📁 Structure du Projet

```
src/
├── components/          # Composants React
│   ├── Dashboard.tsx    # Tableau de bord
│   ├── TrainingPlan.tsx # Plan d'entraînement
│   ├── NutritionPlan.tsx# Plan nutritionnel
│   ├── Calendar.tsx     # Calendrier
│   ├── UserProfile.tsx  # Profil utilisateur
│   └── Analytics.tsx    # Analyses
├── types/              # Types TypeScript
│   └── index.ts        # Définitions des interfaces
├── utils/              # Utilitaires
│   ├── trainingGenerator.ts  # Générateur d'entraînements
│   └── nutritionCalculator.ts# Calculateur nutrition
├── data/               # Données d'exemple
│   └── sampleData.ts   # Profil et événements exemple
└── App.tsx             # Application principale
```

## 🔬 Principes Scientifiques Appliqués

### Périodisation (Bompa & Buzzichelli)
- Planification à long terme
- Adaptation progressive
- Pics de forme ciblés

### Nutrition Sportive (ACSM Guidelines)
- Besoins énergétiques individualisés
- Timing des nutriments
- Hydratation optimisée

### Entraînement Polarisé (Seiler)
- Distribution intensité 80/20
- Évitement zone grise
- Maximisation adaptations

### Football Vétéran (FIFA Medical)
- Récupération prolongée
- Prévention blessures
- Adaptation physiologique âge

## 🎯 Fonctionnalités Futures

- [ ] Interface drag & drop pour le calendrier
- [ ] Intégration capteurs (FC, puissance)
- [ ] Base de données recettes étendue
- [ ] Notifications et rappels
- [ ] Export PDF des plans
- [ ] Synchronisation calendriers externes
- [ ] Analyse biomécanique
- [ ] Coaching IA adaptatif

## 📚 Références Scientifiques

1. Bompa, T. & Buzzichelli, C. (2019). Periodization Training for Sports
2. ACSM (2016). Nutrition and Athletic Performance Position Stand
3. Seiler, S. (2010). What is Best Practice for Training Intensity Distribution?
4. FIFA Medical Assessment and Research Centre (2019). Veteran Football Guidelines

## 🤝 Contribution

Les contributions sont les bienvenues ! Merci de :
1. Fork le projet
2. Créer une branche feature
3. Commit vos changements
4. Push vers la branche
5. Ouvrir une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

---

**Note** : Cette application est un prototype éducatif basé sur des principes scientifiques reconnus. Pour un suivi médical ou des conseils personnalisés, consultez toujours des professionnels qualifiés.
