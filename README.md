# Projet Data Mining - Segmentation Client (RFM & K‑Means) - 2026

**Étudiants :**  
- C25496 Chighaly Khairy  
- C26144 Mostapha Mohamed Lfadel  
- C30175 Oum elkheir aliyine babah  

Ce dossier contient les livrables finaux pour le projet académique de Data Mining.

## 📋 Sujets Traités

Conformément aux consignes, un problème de segmentation client a été modélisé et résolu :

- **Segmentation client par RFM et K‑Means** – Catégorie : Marketing / Analyse client  

Les étapes réalisées sont :  
1. **Acquisition et ingestion des données** – Chargement du CSV et conversion en Parquet, avec comparaison des performances.  
2. **Nettoyage des données** – Suppression des CustomerID manquants, des factures annulées (InvoiceNo commençant par 'C'), des quantités négatives et des prix nuls.  
3. **Construction du modèle RFM** – Extraction des trois indicateurs (Récence, Fréquence, Montant) par client.  
4. **Transformation et normalisation** – Application de la transformation logarithmique `log(x+1)` pour réduire l'asymétrie, suivie d'une normalisation par `StandardScaler`.  
5. **Clustering K‑Means** – Détermination du nombre optimal de clusters par la méthode du coude (Elbow) et le score de silhouette.  
6. **Interprétation métier** – Identification des segments « Champions » (clients récents, fréquents et à fort montant) et « Clients à risque » (clients inactifs ou peu actifs).  
7. **Visualisations 2D et 3D** – Représentation graphique de la séparation des clusters pour validation visuelle.  
8. **Recommandations marketing** – Stratégies différenciées pour chaque segment (rétention, réactivation, cross-selling, etc.).

## 📁 Structure des Fichiers

| Fichier | Description |
|---------|-------------|
| `TP_DataMining_Probleme_9.ipynb` | Notebook Jupyter contenant tout le code, les visualisations 2D/3D et les commentaires détaillés. |
| `online_retail.csv` | Jeu de données source (disponible sur UCI / Kaggle) – déjà fourni dans le répertoire `data/`. |
| `requirements.txt` | Liste des dépendances Python nécessaires pour l'exécution. |
| `README.md` | Ce fichier explicatif. |

## 🛠️ Prérequis et Installation

Pour exécuter le notebook, vous devez disposer de Python (≥ 3.8). Installez les dépendances avec :

```bash
pip install -r requirements.txt
```

### Dépendances principales

- `pandas` : manipulation et analyse de données  
- `numpy` : calculs numériques  
- `scikit-learn` : modèles de machine learning (K-Means, StandardScaler)  
- `matplotlib` et `seaborn` : visualisations 2D  
- `plotly` : visualisations interactives (optionnel)  
- `pyarrow` : support du format Parquet  

## 🚀 Exécution

1. Ouvrez une terminal et accédez au répertoire du projet :
```bash
cd chemin/vers/projet-data-mining-rfm
```

2. Lancez Jupyter Notebook ou Jupyter Lab :
```bash
jupyter notebook
```

3. Ouvrez le fichier `notebook/TP_DataMining_Probleme_9.ipynb`.

4. Exécutez les cellules de haut en bas. Le notebook chargera automatiquement le fichier CSV du répertoire `data/` et générera un fichier Parquet temporaire à des fins de comparaison de performance.

## 📈 Résultats et Livrables

- **Notebook complet :** 
  - Code Python commenté et structuré en sections claires  
  - Visualisations détaillées : distributions RFM, courbes Elbow et Silhouette, scatter plots 2D et 3D  
  - Tableaux récapitulatifs des statistiques par cluster  
  - Interprétation métier des résultats  

- **Segments identifiés :**  
  - **Cluster 1 – Champions** : Clients récents (R faible), fréquents (F élevé), à fort montant (M élevé) → Actions : fidélisation premium, offres exclusives  
  - **Cluster 2 – Clients à risque** : Clients inactifs (R élevé), peu fréquents (F faible), faible montant (M faible) → Actions : campagnes de réactivation, offres spéciales  

## 📊 Points Clés de l'Analyse

- **K optimal** : Déterminé par la méthode du coude et validé par le score de silhouette  
- **Asymétrie** : Réduite par transformation logarithmique pour une normalisation efficace  
- **Scalabilité** : Solution exécutée sur ~4000 clients segmentés (après nettoyage)  
- **Performance** : Comparaison CSV vs Parquet montre un gain de compression ~13×
