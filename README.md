# Projet 18 — Détection de fraude par carte bancaire

Ce projet est un notebook Jupyter beginner-friendly de Data Mining pour détecter des fraudes rares dans des transactions bancaires.

## Dataset utilisé

Le dataset utilisé est **Credit Card Fraud Detection** disponible sur Kaggle.

Le fichier attendu s'appelle :

```text
creditcard.csv
```

Pour respecter le chargement relatif demandé, placez `creditcard.csv` dans le même dossier que le notebook :

```text
notebooks/creditcard.csv
```

## Structure du projet

```text
data/
notebooks/
  fraud_detection_project.ipynb
reports/
README.md
requirements.txt
```

## Comment exécuter le notebook

1. Installer les dépendances :

```bash
pip install -r requirements.txt
```

2. Placer le fichier Kaggle `creditcard.csv` dans le dossier `notebooks/`.

3. Lancer Jupyter :

```bash
jupyter notebook
```

4. Ouvrir puis exécuter :

```text
notebooks/fraud_detection_project.ipynb
```

## Bibliothèques nécessaires

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- jupyter

## Résultats attendus

Le notebook compare trois approches :

- Logistic Regression avec `class_weight="balanced"`
- Random Forest avec `class_weight="balanced"`
- Isolation Forest comme méthode de détection d'anomalies

Les résultats sont évalués avec des métriques adaptées à un dataset très déséquilibré :

- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Matrice de confusion

Le projet montre aussi pourquoi l'accuracy est trompeuse dans la détection de fraude, et compare l'impact de deux seuils de décision, par exemple `0.5` et `0.2`.
