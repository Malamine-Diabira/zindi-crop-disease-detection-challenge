# crop-disease-detection
### 1. **Contexte**
- **Agriculture en Afrique subsaharienne** : Cette région est fortement dépendante de l'agriculture, qui emploie plus de 60 % de la population et représente environ 23 % du PIB. Les cultures de maïs, de poivron et de tomate sont essentielles pour la sécurité alimentaire et les revenus des agriculteurs.
- **Impact des maladies et des ravageurs** : Les maladies des cultures peuvent réduire les rendements de 40 % par an, ce qui a des conséquences graves sur la sécurité alimentaire et l'économie locale. Des maladies telles que le **virus de la mosaïque de la tomate** et le **mildiou du poivron** ont déjà des effets néfastes sur les rendements.

### 2. **Problématique**
- **Augmentation des maladies** : Les changements climatiques et l'accès limité aux technologies agricoles avancées exacerbent la situation, rendant les cultures plus vulnérables aux maladies et aux ravageurs.
- **Difficultés de détection** : Les agriculteurs, souvent éloignés des ressources d'information, manquent d'outils efficaces pour détecter rapidement et précisément les maladies de leurs cultures. Cela peut entraîner des pertes de récolte importantes.

### 3. **Objectif de la Compétition**
Le défi consiste à **développer des modèles d'apprentissage automatique** qui peuvent :
- **Identifier et prédire les maladies** sur des images de cultures de maïs, de poivron et de tomate. Cela inclut la capacité à reconnaître plusieurs maladies sur la même image.
- **Généraliser** : Les modèles doivent être capables de bien performer sur des maladies qui n'étaient pas présentes dans l'ensemble d'entraînement. Cela nécessite une certaine robustesse et capacité d'adaptation.
- **Efficacité sur des appareils mobiles** : La plupart des agriculteurs utilisent des smartphones d'entrée de gamme. Par conséquent, les modèles doivent être optimisés pour fonctionner efficacement sur ces appareils, tant en termes de performance que de consommation de ressources.


### 4. **Défis Techniques**  
- **Qualité des données** : Les données d'images peuvent varier en qualité (résolution, éclairage) et en quantité, ce qui peut influencer la capacité du modèle à apprendre efficacement.
- **Variabilité des symptômes** : Les symptômes de maladies peuvent être similaires, ce qui complique la classification. Les agriculteurs peuvent également utiliser des méthodes de culture variées qui peuvent affecter l'apparence des plantes.
- **Accès à des technologies avancées** : Les agriculteurs dans les zones rurales peuvent ne pas avoir accès à des smartphones puissants, ce qui limite l'utilisation de modèles complexes.

### 5. **Solutions Proposées**
Pour répondre à ces défis, la compétition encourage les participants à :
- Utiliser des **techniques d'apprentissage automatique** pour traiter des ensembles de données d'images.
- Développer des **modèles légers** qui peuvent fonctionner sur des smartphones avec des ressources limitées.
- Incorporer des **techniques de transfert d'apprentissage** pour améliorer la performance sur des maladies moins représentées.


### 5.1 **Suggestions d’optimisation**
Traitement des classes déséquilibrées :
Techniques de rééchantillonnage : Appliquer un suréchantillonnage pour les classes rares ou un sous-échantillonnage pour les classes fréquentes pour équilibrer le dataset. Des techniques comme SMOTE (Synthetic Minority Over-sampling Technique) peuvent également générer des exemples synthétiques pour les classes minoritaires.
Pondération des classes dans la fonction de perte : En modifiant la fonction de perte pour attribuer un poids plus élevé aux classes rares, le modèle accorde plus d'importance aux maladies moins fréquentes.
Augmentation des données :
Appliquer une augmentation d'image spécifique à la tâche (rotation, recadrage, zoom, etc.) pour enrichir les données d'entraînement et améliorer la généralisation. Cette étape est cruciale pour réduire le surapprentissage, surtout dans les classes sous-représentées.
Choix d'un modèle plus léger et efficace :
Utiliser un modèle pré-entraîné comme MobileNet ou EfficientNet, qui est optimisé pour fonctionner sur des ressources GPU limitées (comme vous l’avez mentionné pour ce projet). Ces architectures sont légères tout en offrant de bonnes performances en classification d'image.
Hyperparameter Tuning :
Utiliser des techniques comme Grid Search ou Random Search pour optimiser les hyperparamètres. Pour les tâches à ressources limitées, Optuna est aussi un excellent choix, car il optimise intelligemment les hyperparamètres en se basant sur les résultats précédents.
Transfer Learning avec des modèles pré-entraînés :
Utiliser des poids pré-entraînés sur des datasets similaires (comme PlantVillage) peut améliorer la précision de détection des maladies. En ajustant les dernières couches pour votre dataset spécifique, vous pouvez bénéficier de connaissances transférables.

### 6. **Implications et Importance**
- **Amélioration de la productivité agricole** : Une détection rapide et précise des maladies peut aider les agriculteurs à agir rapidement, réduisant ainsi les pertes de rendement.
- **Renforcement de la sécurité alimentaire** : En optimisant les rendements des cultures, on peut contribuer à la sécurité alimentaire dans une région où cela est crucial.
- **Innovation locale** : Encourager les solutions basées sur l'IA développées localement favorise l'innovation et l'autonomisation des communautés agricoles.

En résumé, le problème que cette compétition vise à résoudre est complexe et multidimensionnel, alliant des éléments techniques d'apprentissage automatique à des enjeux sociaux et économiques. L'utilisation de l'IA pour détecter les maladies des cultures représente une approche prometteuse pour soutenir les agriculteurs dans leur lutte contre les pertes de rendement dues aux maladies et aux ravageurs. Si tu as des questions sur un aspect particulier ou si tu souhaites explorer un sujet plus en détail, fais-le moi savoir !

### 7. **Projets Similaires**
https://www.kaggle.com/code/imtkaggleteam/plant-diseases-detection-pytorch

### 8. **Ressources**
https://www.youtube.com/watch?v=a5z_J2oBH0k
https://www.youtube.com/watch?v=dA4pVGQ1isk   faster r-cnn object detection tensorflow
https://www.youtube.com/watch?v=XQnVjc-B9i4    Introduction to Colab Enterprise on Vertex AI

https://www.youtube.com/watch?v=PwYHoiB4Fag  TPU VM on Google Cloud
https://www.youtube.com/watch?v=utxbUlo9CyY   DETR - End to end object detection with transformers (ECCV2020)
https://www.youtube.com/watch?v=AM8D4j9KoaU   How to Train DETR Object Detection Transformer on Custom Dataset
https://www.youtube.com/watch?v=1d4BzR_7Nbc   Deploying production ML models with TensorFlow Serving overview
Guide To Transfer Learning in Deep Learning
https://medium.com/@davidfagb/guide-to-transfer-learning-in-deep-learning-1f685db1fc94#id_token=eyJhbGciOiJSUzI1NiIsImtpZCI6IjFkYzBmMTcyZThkNmVmMzgyZDZkM2EyMzFmNmMxOTdkZDY4Y2U1ZWYiLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJodHRwczovL2FjY291bnRzLmdvb2dsZS5jb20iLCJhenAiOiIyMTYyOTYwMzU4MzQtazFrNnFlMDYwczJ0cDJhMmphbTRsamRjbXMwMHN0dGcuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJhdWQiOiIyMTYyOTYwMzU4MzQtazFrNnFlMDYwczJ0cDJhMmphbTRsamRjbXMwMHN0dGcuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJzdWIiOiIxMDAyODA4MjQ1NjcwMjcxNDAyMDciLCJlbWFpbCI6ImRpYWJpcmEubWFsYW1pbmUxMUBnbWFpbC5jb20iLCJlbWFpbF92ZXJpZmllZCI6dHJ1ZSwibmJmIjoxNzMxOTcxMjg5LCJuYW1lIjoiTWFsYW1pbmUgRGlhYmlyYSIsInBpY3R1cmUiOiJodHRwczovL2xoMy5nb29nbGV1c2VyY29udGVudC5jb20vYS9BQ2c4b2NKU3o0ckJLQi1Mc3RsXzZZMFVJbHJnSHIxbUlqSHV4aVd5WTBkMWhyWnZVd3IwN2c9czk2LWMiLCJnaXZlbl9uYW1lIjoiTWFsYW1pbmUiLCJmYW1pbHlfbmFtZSI6IkRpYWJpcmEiLCJpYXQiOjE3MzE5NzE1ODksImV4cCI6MTczMTk3NTE4OSwianRpIjoiNDUxOWEwNmJhNTE2ZjUyZjE0MzM0YTA0M2JiZTZkODAxYmU2NmJjMCJ9.qLOWcGKBx7WPq8RQPInES4E2HVgotubjykYm1hDZyf84eMkKWgp_mCOL6G9452aXJ5iYAR2HyB0g9H1JfsqnEPZNOAT6JQSlaiRgjdnS6arTUEJrlE2WLAPF_YuaX0r6u7BAkYYeq5dHT2-fSUUEWbf-EIZLs55giCJ7tG-Kk8QNfNo5-V6arvRgPleHSFMUGI_AVgIovoUX-4UziFFuWrXvovjAf32ExlcrAeSouSLJ1orqhyxZfYGCF3zqhPeFVdjeibqrVsroAXQuDyvhxq3guJDmS4-3L5SOFBSZ03DlEhKOXtUv61Tms5PT115V0yBRgk-WIKku56ydm0NKiQ

