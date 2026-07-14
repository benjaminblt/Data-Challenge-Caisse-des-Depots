# Scoring des risques physiques climatiques

Construire un score géographique et financier permettant d’évaluer l’exposition climatique d’un portefeuille d’actifs situés en France métropolitaine.

## Contexte

Projet réalisé dans le cadre d’un **Data Challenge Caisse des Dépôts**.

L’objectif est de mesurer quatre risques physiques :

- sécheresse et stress hydrique ;
- inondations ;
- feux de forêt ;
- vagues de chaleur.

Le modèle tient compte de la localisation, de la maturité du financement, du secteur d’activité, de l’encours et des contreparties multi-sites.

## Données

- projections climatiques DRIAS ;
- fichiers spécialisés sur les précipitations et les feux ;
- contours communaux et codes INSEE ;
- portefeuille fictif de 99 actifs ;
- secteurs NACE, maturités et encours.

Trois horizons sont étudiés : 2021-2050, 2051-2070 et 2071-2100.

## Méthodologie

1. nettoyage et harmonisation des données ;
2. construction d’indicateurs par aléa ;
3. segmentation par K-Means pour la sécheresse, les feux et la chaleur ;
4. conversion des groupes en niveaux faible, modéré, élevé ou critique ;
5. jointure spatiale au niveau communal ;
6. cartographie sous GeoPandas et QGIS ;
7. pondération selon le secteur, l’horizon et l’encours ;
8. agrégation au niveau des actifs, des contreparties et du portefeuille.

## Résultats clés

| Indicateur | Valeur |
|---|---:|
| Actifs étudiés | 99 |
| Score global | 6,50471 |
| Score maximal | 10,9908 |
| Niveau relatif du portefeuille | **59,2 %** |

Principaux enseignements :

- les inondations contribuent le plus au risque moyen ;
- la chaleur et la sécheresse progressent selon les horizons ;
- le risque feu reste plus localisé, notamment dans le sud ;
- les secteurs eau, construction et santé figurent parmi les plus exposés.

## Technologies

`Python` · `pandas` · `scikit-learn` · `GeoPandas` · `Matplotlib` · `QGIS` · `Excel`

## Ce que ce projet démontre

- traitement de données climatiques hétérogènes ;
- machine learning non supervisé ;
- analyse géospatiale ;
- création d’un score décisionnel ;
- agrégation financière ;
- restitution cartographique.

## Limites et améliorations

Le portefeuille est fictif et les pondérations sectorielles nécessitent une validation experte. Une extension pertinente serait d’ajouter des scénarios climatiques multiples, des fonctions de dommage et des intervalles d’incertitude.

## Auteur

Projet réalisé par **Benjamin BAILLET**.

---
