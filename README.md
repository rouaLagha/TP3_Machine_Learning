# Compte Rendu du TP : Modélisation et Prédiction avec des Algorithmes de Machine Learning

## Exercice 1 : Prédiction de la Popularité d'une Publication sur les Réseaux Sociaux avec un Réseau de Neurones

### Objectif :
L'objectif de cet exercice était de construire un modèle de Deep Learning simple pour prédire la popularité d'une publication (mesurée par le nombre de likes et de partages) en fonction de ses caractéristiques telles que la longueur du texte, l'heure de publication, la présence d'images/vidéos, et le nombre initial d'abonnés.

### Méthodologie :
1. **Chargement et Exploration des Données :**  
   Le dataset contenant des informations sur les publications sur les réseaux sociaux a été chargé. Une première exploration a permis d’identifier les caractéristiques suivantes comme pertinentes pour la prédiction de la popularité : longueur du texte, présence d'images/vidéos, heure de publication, et nombre initial d'abonnés.
   
2. **Prétraitement des Données :**  
   Les données ont été nettoyées, avec un traitement des valeurs manquantes par imputation. Une normalisation a été effectuée sur les variables numériques afin d'assurer une meilleure convergence du modèle.
   
3. **Séparation des Données :**  
   Les données ont été séparées en deux ensembles : un ensemble d'entraînement (80%) et un ensemble de test (20%).
   
4. **Construction du Modèle :**  
   Un réseau de neurones artificiels simple a été construit avec une couche d'entrée, une couche cachée, et une couche de sortie. Le modèle a été créé à l’aide de Keras avec une fonction d'activation ReLU pour la couche cachée et une fonction d'activation linéaire pour la sortie, adaptée à un problème de régression.
   
5. **Entraînement et Évaluation :**  
   Le modèle a été entraîné en utilisant la méthode de rétropropagation et l'optimiseur Adam. L'évaluation de la performance a été réalisée en utilisant l'indicateur RMSE (Root Mean Squared Error) pour mesurer l’erreur de prédiction.

### Résultats :
Le modèle a montré une performance raisonnable avec une erreur RMSE acceptable. Cependant, des améliorations peuvent être apportées en augmentant le nombre de couches cachées ou en ajustant les hyperparamètres du modèle.

---

## Exercice 2 : Clustering de Clients avec l'Algorithme K-Means

### Objectif :
L'objectif était de segmenter des clients en groupes ayant des comportements similaires à l'aide du clustering non supervisé, en utilisant l'algorithme K-Means.

### Méthodologie :
1. **Chargement et Exploration des Données :**  
   Le dataset contenant des informations sur les clients a été chargé. Une analyse exploratoire a révélé que les variables pertinentes incluent l’âge, le revenu annuel, le score de fidélité et les dépenses moyennes.
   
2. **Prétraitement des Données :**  
   Les variables numériques ont été normalisées afin de garantir que chaque caractéristique contribue également à l'algorithme K-Means.

3. **Application de K-Means :**  
   L'algorithme K-Means a été appliqué avec un nombre de clusters initialement arbitraire. Ensuite, la méthode du coude (Elbow Method) a été utilisée pour déterminer le nombre optimal de clusters, qui s'est avéré être 4.

4. **Visualisation des Résultats :**  
   Les clusters obtenus ont été visualisés en 2D sur un graphique, où chaque point représente un client. La segmentation a montré des groupes de clients ayant des comportements similaires.

### Résultats :
Les profils types des clients dans chaque groupe étaient les suivants :
- **Cluster 1 :** Clients avec un revenu élevé et un score de fidélité faible.
- **Cluster 2 :** Clients jeunes avec un revenu moyen et des dépenses modérées.
- **Cluster 3 :** Clients âgés avec un revenu faible et un score de fidélité élevé.
- **Cluster 4 :** Clients ayant un revenu moyen et des dépenses élevées.

---

## Exercice 3 : Détection d'Emails Spam avec un Classifieur Naïve Bayes

### Objectif :
L'objectif de cet exercice était de construire un modèle de classification pour détecter les emails spam à partir de leur contenu textuel.

### Méthodologie :
1. **Chargement et Exploration des Données :**  
   Le dataset d'emails labellisés "spam" ou "non spam" a été chargé. Une analyse exploratoire a montré que des mots-clés comme "promotion", "urgent", "offre", étaient fréquents dans les emails spam.

2. **Prétraitement des Données :**  
   Les données textuelles ont été nettoyées par suppression des stopwords, lemmatisation et vectorisation TF-IDF. Ces étapes ont permis de transformer le texte en vecteurs numériques utilisés par le classifieur.

3. **Division des Données :**  
   Les données ont été divisées en un ensemble d'entraînement (80%) et un ensemble de test (20%).

4. **Entraînement du Modèle :**  
   Un classifieur Naïve Bayes a été utilisé pour la classification. Ce modèle a été choisi en raison de sa simplicité et de son efficacité pour les tâches de classification de texte.

5. **Évaluation et Analyse des Résultats :**  
   La performance du modèle a été évaluée en utilisant la précision, le rappel et le F1-score. Les mots les plus influents pour prédire un email spam étaient "promotion", "offre", et "urgent", ce qui correspond à des caractéristiques typiques des emails indésirables.

### Résultats :
Le modèle Naïve Bayes a donné des résultats satisfaisants avec une bonne précision, mais il pourrait être amélioré par l’utilisation de modèles plus complexes ou l'augmentation de la taille du dataset.

---

## Conclusion

Ce TP a permis d'appliquer des algorithmes de machine learning classiques à des problèmes de prédiction, clustering et classification. Chaque exercice a renforcé la compréhension des différentes étapes du processus de machine learning, de la préparation des données à l'évaluation du modèle. Les résultats obtenus sont prometteurs, mais des améliorations peuvent être apportées pour optimiser les performances des modèles.
