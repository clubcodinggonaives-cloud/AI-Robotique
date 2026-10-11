# Devoir de Robotique et Intelligence Artificielle

## Projet : modèle d'orientation scolaire par fine-tuning

**Élève :** Desulma Jhonsley

**Cours :** Robotique et Intelligence Artificielle

**Fichier du travail :** [`Leson2_FineTuning_Oryantasyon.ipynb`](Leson2_FineTuning_Oryantasyon.ipynb)

## Objectif du projet

Réaliser un modèle de classification de texte qui analyse les intérêts exprimés par un élève en français ou en créole haïtien et propose jusqu'à trois domaines d'études ou de métiers. Le programme associe aussi chaque domaine à des exemples de métiers et de formations.

## Outils et composants utilisés

- Python et Jupyter Notebook (exécution possible dans Google Colab)
- PyTorch et le modèle multilingue `distilbert-base-multilingual-cased`
- Hugging Face `transformers` et `datasets`
- `scikit-learn`, `pandas` et `numpy` pour préparer et évaluer les données
- Un jeu d'exemples rédigés en français et en créole haïtien, répartis entre 14 domaines

## Fonctionnement

1. Le notebook prépare les domaines, les métiers, les formations et les phrases d'exemple.
2. Il transforme les phrases en données numériques avec le tokenizer du modèle.
3. Il sépare les exemples en un ensemble d'entraînement (80 %) et un ensemble de test (20 %).
4. Il adapte le modèle pré-entraîné pour classer les phrases dans les 14 domaines.
5. La fonction `konseye()` affiche les trois domaines les plus probables et leurs métiers et formations associés.
6. Le modèle entraîné, le tokenizer et les informations sur les domaines sont enregistrés dans `modèl_oryantasyon`.

## Résultats obtenus

Le notebook contient le code permettant d'entraîner et de tester le modèle, mais il n'a pas encore été exécuté dans la version remise. La précision, la perte et les prédictions réelles restent donc à relever après l'exécution de toutes les cellules. Elles ne sont pas estimées dans ce rapport.

Après exécution, compléter cette section avec la précision affichée, quelques prédictions observées et une courte interprétation. La précision mesurée sur un petit jeu de test ne suffit pas à démontrer que le modèle fonctionnera bien sur tous les élèves.

## Captures d'écran

Ajouter ici les captures d'écran demandées montrant au minimum l'entraînement ou ses métriques, puis des exemples de prédictions. Les captures ne sont pas encore présentes dans la version actuelle du dépôt.

## Limites et précautions

Le jeu de données est petit et les exemples sont construits manuellement. Les prédictions peuvent être erronées ou biaisées, et le modèle propose toujours une classe même si le texte ne correspond à aucun des domaines. Il s'agit d'un outil d'aide à la réflexion, pas d'une décision d'orientation. Les métiers, formations et établissements cités doivent être vérifiés.
