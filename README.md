# 🎓 Orientation IA — Fine-tuning d'un modèle de recommandation

Ce projet est un tutoriel pratique qui montre comment adapter un modèle de langue pré-entraîné pour recommander des domaines professionnels à partir des intérêts exprimés par un élève.

Le modèle utilise des exemples en français et en créole haïtien, puis classe un texte dans l'un des domaines suivants :

- Développement logiciel et web
- Données et mathématiques
- Psychologie et travail social
- Art et design
- Biologie et santé
- Écriture et journalisme
- Génie mécanique et civil
- Business et entrepreneuriat
- Enseignement
- Musique et son
- Robotique
- Électronique et systèmes embarqués
- Intelligence artificielle
- Technologie pour la santé

## ✨ Objectif

Créer un assistant d'orientation qui :

1. Analyse un intérêt ou une aspiration exprimée par une personne.
2. Identifie les domaines professionnels les plus probables.
3. Affiche les métiers et formations associés à chaque domaine.
4. Fournit trois recommandations avec leurs probabilités.

> ⚠️ Ce modèle est un outil d'aide à la réflexion, pas une décision définitive. Les recommandations doivent toujours être vérifiées avec un conseiller ou un professionnel.

## 🧠 Approche

Le projet repose sur :

- `distilbert-base-multilingual-cased` comme modèle de base.
- Un jeu de données créé manuellement à partir de phrases en français et en créole.
- L'augmentation des données pour obtenir plusieurs exemples par domaine.
- Une séparation entre les données d'entraînement et les données de test.
- La bibliothèque `transformers` de Hugging Face.
- `TrainingArguments` et `Trainer` pour l'entraînement.
- Une fonction de classification permettant d'obtenir les trois principaux domaines.

## 📁 Contenu

- `Leson2_FineTuning_Oryantasyon.ipynb` : notebook principal contenant toutes les étapes du projet.

## 🚀 Prérequis

Avant de lancer le notebook, il est recommandé d'avoir :

- Un compte Google ou un environnement Python compatible.
- Une connexion Internet pour télécharger les bibliothèques et le modèle.
- Une ressource GPU, idéalement une Tesla T4 ou une GPU équivalente.
- Python 3.9 ou une version plus récente.

## 🔧 Installation

Le notebook installe automatiquement les dépendances suivantes :

```bash
pip install -q transformers datasets accelerate pandas scikit-learn numpy
```

Dans Google Colab, choisissez :

**Runtime → Change runtime type → GPU → T4**

L'entraînement peut prendre environ 2 à 5 minutes selon la puissance de la GPU et la charge du service.

## ▶️ Utilisation

1. Ouvrez le notebook `Leson2_FineTuning_Oryantasyon.ipynb`.
2. Exécutez toutes les cellules dans l'ordre.
3. Vérifiez que le modèle détecte une GPU disponible.
4. Lancez l'entraînement avec les paramètres configurés dans le notebook.
5. Testez le modèle avec des phrases nouvelles.
6. Sauvegardez le modèle, le tokenizer et la liste des domaines.

Exemple de requête :

```python
konseye("Mwen renmen fè eksperyans ak kaptè epi pwograme yon ti robo")
```

Le modèle renverra généralement les trois domaines les plus probables, ainsi que les métiers et formations associés.

## 🧪 Évaluation

Le notebook utilise 20 % des données comme jeu de test. Il affiche ensuite :

- La perte de validation.
- La précision obtenue sur les données de test.
- Les trois domaines recommandés avec leurs probabilités.

Pour un jeu de données limité, une précision comprise entre 60 % et 90 % peut être considérée comme normale. Une précision de 100 % ne signifie pas nécessairement que le modèle fonctionne parfaitement, car le jeu de test est très petit.

## 💾 Sauvegarde du modèle

L'entraînement crée un dossier nommé `modèl_oryantasyon` contenant :

- Le modèle entraîné.
- Le tokenizer.
- Les métadonnées des domaines.

Le modèle peut être rechargé avec `pipeline("text-classification", model=...)`.

## ⚠️ Limitations

- La quantité de données est volontairement limitée.
- Le modèle peut reproduire les biais présents dans les exemples.
- Il peut fournir une réponse même lorsqu'il ne connaît pas le domaine.
- Les résultats dépendent de la qualité et de la diversité des données.
- Le modèle ne doit pas être utilisé pour évaluer une personne de manière définitive.
- Les formations et institutions mentionnées doivent être vérifiées et mises à jour.

## 🎯 Mini-défi

Le notebook propose d'ajouter un 15e domaine, par exemple :

- Agriculture et environnement.

Pour ce faire, il faut :

1. Ajouter le nouveau domaine dans la liste `domen`.
2. Ajouter au moins six exemples en français et en créole.
3. Relancer les cellules à partir de l'étape de préparation des données.
4. Tester le modèle avec une phrase liée à l'agriculture.

## 🤝 Contribution

Les contributions sont les bienvenues. Vous pouvez :

- Ajouter de nouveaux domaines.
- Augmenter le jeu de données.
- Améliorer les exemples en français et en créole.
- Corriger les formations et les métiers.
- Ajouter une validation plus complète des résultats.

## 📄 Licence

Ce projet n’indique pas de licence explicite. Avant de publier le dépôt public, vérifiez la licence applicable et ajoutez un fichier `LICENSE` si nécessaire.

## 👤 Auteur

Desulma Jhonsley
# AI-Robotique
