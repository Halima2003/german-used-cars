# 🚗 Analyse de Données Automobiles

Projet d'analyse de données de voitures avec Machine Learning pour prédire les prix et identifier les segments de marché.

---

## 📌 Description du projet

Ce projet analyse un dataset de voitures allemandes pour :
- Prédire les prix des véhicules
- Identifier différents segments de marché
- Détecter les marques surcotées ou sous-cotées

---

## 🔬 Méthodologie

### 1. **Préparation des données**
- Normalisation des noms de colonnes
- Détection automatique des colonnes (prix, marque, kilométrage, puissance, année)
- Conversion des types de données
- Calcul de l'âge des véhicules (année actuelle - année du véhicule)
- Filtrage des valeurs aberrantes
- Gestion des valeurs manquantes

### 2. **Analyse exploratoire**
- Distribution des prix et âges
- Corrélation entre prix et âge
- Analyse par tranche d'âge
- Identification des marques les plus présentes

### 3. **Machine Learning**
- **Features utilisées** : âge, puissance, kilométrage, marque, type de carburant, transmission
- **Encodage** des variables catégorielles
- **3 modèles comparés** :
  - LightGBM
  - XGBoost
  - RandomForest
- **Métriques** : MAE, RMSE, R²
- Sélection du meilleur modèle
- Analyse de l'importance des variables

### 4. **Clustering**
- **Algorithme** : K-Means (5 clusters)
- **Normalisation** des données avec StandardScaler
- **Visualisation** en 2D avec PCA
- Profils moyens par cluster
- Labels descriptifs pour chaque segment

### 5. **Analyse de surcote**
- Calcul des résidus (écart entre prix réel et prédit)
- Identification des marques surcotées
- Visualisation par marque

---

## 🛠️ Technologies

- **Python 3.8+**
- **Pandas** - Manipulation de données
- **NumPy** - Calculs numériques
- **Scikit-learn** - Machine Learning (preprocessing, clustering, métriques)
- **LightGBM & XGBoost** - Modèles de prédiction
- **Matplotlib & Seaborn** - Visualisations
- **Jupyter Notebook** - Environnement de développement

---

## 📖 Utilisation

```python
# 1. Charger les données
df = pd.read_excel(r'chemin/vers/votre_fichier.xlsx')

# 2. Nettoyer les données
df_clean = clean_data(df)

# 3. Analyse exploratoire
exploratory_analysis(df_clean)

# 4. Machine Learning
X, y, features, data_ml = prepare_ml_features(df_clean)
best_model, X_test, y_test, y_pred = train_and_compare_models(X, y)

# 5. Clustering
df_final = perform_clustering(df_clean)
```

---
## 👤 Auteur

**Halima**  
Projet d'analyse de données - 2024
