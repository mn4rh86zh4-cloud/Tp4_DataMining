# Projet de Data Mining : Segmentation Stratégique RFM avec K-Means

Ce dépôt contient le code, le notebook et le rapport d'un pipeline complet de Data Mining visant à segmenter les clients d'un commerce de détail en ligne. Le projet utilise le modèle **RFM** (Récence, Fréquence, Montant) couplé à l'algorithme de clustering **K-Means**.

## 📊 Description du Projet

L'objectif métier est de regrouper les clients selon leurs comportements d'achat historiques afin de lancer des campagnes marketing personnalisées. À partir du dataset **Online Retail Dataset** (provenant de l'UCI / Kaggle), le projet aborde les problématiques suivantes :
- Prétraitement et nettoyage de données réelles (valeurs manquantes, anomalies).
- Feature Engineering pour extraire les indicateurs RFM.
- Entraînement et optimisation d'un modèle non supervisé (K-Means).
- Interprétation métier des clusters obtenus et recommandations d'actions marketing.

## 📁 Structure du Dépôt

```
projet-data-mining-rfm/
│
├── data/
│   ├── online_retail.csv        # Données brutes converties en CSV (Généré à l'exécution)
│   ├── online_retail.parquet    # Données optimisées pour la lecture (Généré à l'exécution)
│
├── notebook/
│   ├── DataMining_RFM_KMeans.ipynb # Notebook contenant tout le code et les analyses
│
├── report/
│   ├── rapport_overleaf.tex     # Code source LaTeX du rapport académique
│   ├── bibliography.bib         # Bibliographie pour le rapport
│   ├── figures/                 # Dossier pour les figures générées (pour inclusion LaTeX)
│
├── requirements.txt             # Liste des dépendances Python
├── README.md                    # Ce fichier
```

## 🛠️ Installation

1. Assurez-vous d'avoir Python 3.8+ installé.
2. Clonez ce dépôt sur votre machine locale.
3. Installez les dépendances requises en utilisant `pip` :

```bash
pip install -r requirements.txt
```

## 🚀 Exécution

1. Lancez Jupyter Notebook ou Jupyter Lab :
```bash
jupyter notebook
```
2. Ouvrez le fichier `notebook/DataMining_RFM_KMeans.ipynb`.
3. Exécutez les cellules de haut en bas. 
   - *Note : Lors de la première exécution, le code se chargera de télécharger le fichier Excel original (~24 MB) depuis UCI et de générer les fichiers CSV et Parquet dans le dossier `data/`.*

## 📈 Résultats et Livrables

- **Notebook complet :** Code commenté, visualisations (2D PCA, 3D Scatter, Boxplots, Heatmap) et interprétation.
- **Rapport Académique :** Vous pouvez importer le dossier `report/` directement dans Overleaf pour compiler le PDF final détaillant l'approche méthodologique et les résultats.

## ⚙️ Contraintes Techniques
- Python 3.x
- Bibliothèques principales : `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `plotly`.
