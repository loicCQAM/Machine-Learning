# Galaxy Predictions

Ce travail porte sur la définition et l’extraction de primitives sur des fichiers multimédias. Le
problème de classification qui est présenté est le problème Galaxy Zoo (voir l’adresse
https://www.galaxyzoo.org/ pour de plus amples informations) dont le but est de classer des images de
galaxies dans diverses catégories.

## Résultats

### Decision Tree
| Paramètre X      | Résultat |
| ---------------- |:---------:
| max_depth = None | 96.36%   |
| max_depth = 3    | 87.91%   |
| max_depth = 5    | 91.28%   |
| max_depth = 10   | 95.04%   |


### K-Nearest Neighbour
| Paramètre X                       | Résultat |
| --------------------------------- |:---------:
| Neighbors : 3, weight : uniform   | 74.50%   |
| Neighbors : 5, weight : uniform   | 68.95%   |
| Neighbors : 10, weight : uniform  | 65.48%   |
| Neighbors : 3, weight : distance  | 83.70%   |
| Neighbors : 5, weight : distance  | 83.23%   |
| Neighbors : 10, weight : distance | 83.34%   |


### Bernouilli
| Paramètre X  | Résultat |
| ------------ |:---------:
| MinMaxScaler | 55.53%   |
| Discretizer  | N/A      |

### 10-fold
| Modèle        | Résultat |
| ------------- |:---------:
| KNN           | 86.49%  |
| Naive Bayes   | 70.96%  |
| Decision Tree | 96.85%  |

### Améliorations potentielles
* Augmenter le nombre de d’exemples dans les données d’entraînement
* Améliorer les capacités de discrimination des primitives
* Traiter les données aberrantes
* Normaliser les données

