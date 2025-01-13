---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
css: unocss
---

# Étude Comparative des Algorithmes Non Supervisés
Détection de Malwares à partir d'Exécutables

---
layout: two-cols
---

# K-Means Clustering

::right::

<div class="ml-4">
<img src="https://scikit-learn.org/stable/_images/sphx_glr_plot_kmeans_assumptions_001.png" class="h-60 rounded shadow" />
</div>

- Algorithme de partitionnement
- Divise les données en K clusters
- Principe:
  1. Initialisation aléatoire des centroids
  2. Attribution des points au centroid le plus proche
  3. Recalcul des centroids
  4. Répétition jusqu'à convergence

---
layout: two-cols
---

# DBSCAN

::right::

<div class="ml-4">
<img src="https://scikit-learn.org/stable/_images/sphx_glr_plot_dbscan_001.png" class="h-60 rounded shadow" />
</div>

- Clustering basé sur la densité
- Avantages:
  - Détecte les clusters de forme arbitraire
  - Identifie les points de bruit
- Paramètres clés:
  - eps: rayon de voisinage
  - min_samples: nombre minimum de points

---
layout: two-cols
---

# Gaussian Mixture Model (GMM)

::right::

<div class="ml-4">
<img src="https://scikit-learn.org/stable/_images/sphx_glr_plot_gmm_pdf_001.png" class="h-60 rounded shadow" />
</div>

- Modèle probabiliste
- Suppose que les données suivent plusieurs distributions gaussiennes
- Caractéristiques:
  - Clustering souple (probabilités d'appartenance)
  - Adapté aux clusters de forme elliptique
  - Utilise l'algorithme EM

---
layout: default
---

# Méthodologie

```mermaid
graph TD
    A[Dataset] --> B[Prétraitement]
    B --> C[Division Train/Test]
    C --> D[Entraînement des Modèles]
    D --> E[Évaluation]
    E --> F[Comparaison]
```

---
layout: two-cols
---

# Métriques d'Évaluation

- Silhouette Score
  - Mesure la qualité des clusters
  - Score entre -1 et 1

::right::

- Davies-Bouldin Index
  - Évalue la séparation des clusters
  - Plus petit = meilleur

- Homogeneity/Completeness
  - Pour validation avec labels connus

---
layout: center
---

# Comparaison des Résultats

| Algorithme | Silhouette Score | Davies-Bouldin | Temps d'exécution |
|------------|------------------|----------------|-------------------|
| K-Means    | {score}          | {score}        | {temps}          |
| DBSCAN     | {score}          | {score}        | {temps}          |
| GMM        | {score}          | {score}        | {temps}          |

---
layout: end
---

# Merci de votre attention

Questions ?