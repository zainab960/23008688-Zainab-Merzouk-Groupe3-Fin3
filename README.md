# Examen Pratique de Machine Learning : Prédiction de l'Inflation Mondiale

* **Étudiante :** Zainab Merzouk
* **Code Apogée :** 23008688
* **Groupe :** Groupe3-Fin3

## Problématique et Objectif
* **Question :** Peut-on prédire l'inflation d'un pays l'an prochain mieux qu'en recopiant celle de cette année ?  
* **Objectif chiffré :** Obtenir une erreur absolue moyenne (MAE) inférieure d'au moins 10 % à la règle simple (*baseline*) sur la période de test (2020–2024).

## Données et Méthodologie
* **Source :** Base de données internationale sur l'inflation (FMI / World Economic Outlook), 196 pays sur la période 1980–2024.
* **Préparation :** Passage au format panel (*1 ligne = 1 pays et 1 année*), création des variables de retard (`lag1`, `lag2`, `lag3`) et découpage temporel strict (Apprentissage $\le 2015$, Validation 2016–2019, Test 2020–2024).
* **Modèle :** Régression Ridge (pénalisation $L_2$, $\alpha = 100.0$).

## Résultats Principaux (Jeu de Test 2020–2024)
* **Règle simple (Baseline) :** RMSE = 666.15 | MAE = 34.92
* **Modèle Ridge ($\alpha=100.0$) :** RMSE = 269.26 | MAE = 30.75 *(Objectif atteint)*

## Structure du Dépôt
* `notebooks/` : Carnet Jupyter (`examen_ml_inflation.ipynb`) et rapport PDF.
* `requirements.txt` : Dépendances Python.
* `DECLARATION_IA.md` : Transparence sur l'utilisation de l'intelligence artificielle.
