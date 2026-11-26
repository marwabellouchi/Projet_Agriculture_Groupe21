# Analyse de la production agricole — Dataset ICRISAT (Groupe 21)

Ce projet a pour objectif d'explorer et d'analyser les données agricoles du dataset **ICRISAT** afin d'identifier les cultures les plus productives, les régions (États) dominantes et l'évolution temporelle des surfaces cultivées, des rendements et de la production.

## Objectifs de l'analyse
- **Classement des cultures :** Identifier les cultures les plus importantes en volume de production cumulée (ex. : riz, blé, canne à sucre, oléagineux, maïs).
- **Analyse géographique :** Repérer les principaux États producteurs pour les cultures clés.
- **Évolution temporelle :** Suivre dans le temps les surfaces (`AREA`), les rendements (`YIELD`) et la production (`PRODUCTION`) afin de distinguer l'extension des surfaces des gains de productivité.

## Structure du projet
```text
├── data/                        # Dataset ICRISAT (fichier CSV/Excel)
├── notebooks/                   # Notebooks Jupyter d'exploration et d'analyse
├── src/                         # Scripts Python réutilisables (nettoyage, agrégations, visualisations)
├── outputs/                     # Graphiques et tableaux exportés
└── README.md                    # Documentation du projet
```

## Méthodologie et points d'attention
- **Gestion des valeurs manquantes :** Éviter un `dropna()` global sur l'ensemble des colonnes afin de ne pas supprimer inutilement des observations valides pour une culture ou une année donnée ; traiter les valeurs manquantes selon la métrique et la culture étudiées.
- **Colonnes agrégées vs cultures individuelles :** Vérifier la distinction entre les cultures individuelles et les catégories regroupées (ex. `OILSEEDS`, `FRUITS AND VEGETABLES`) pour éviter les doubles comptages.
- **Rendement moyen :** Privilégier un rendement moyen pondéré par la surface cultivée lors des agrégations régionales ou annuelles.

## Installation et exécution
1. Cloner le dépôt et accéder au dossier du projet :
   ```bash
   git clone <url-du-repo>
   cd Projet_Agriculture_Groupe21
   ```
2. Installer les dépendances nécessaires :
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Lancer le notebook d'analyse :
   ```bash
   jupyter notebook
   ```

## Auteurs
- **Groupe 21** — *BELLOUCHI Marwa - BOUHOU Imane*
