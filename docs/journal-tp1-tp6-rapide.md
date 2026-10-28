# Journal de projet — TP1 à TP6

## 1. Identification du projet

Projet : sentiment-app

Binôme :
- Membre A : Hiba Ayatallah
- Membre B : Hiba Ayatallah

## 2. Objectif du projet

Le projet vise à développer une application de classification de sentiments à partir d'avis textuels. Il s'inscrit dans une logique progressive : cadrage du besoin, configuration de l'environnement, entraînement du modèle, exposition API, interface utilisateur, validation fonctionnelle et finalisation du livrable.

## 3. TP1 — Cadrage et validation initiale

Le TP1 a permis de cadrer le besoin métier et de préparer la base technique du projet. Les trois fiches de cadrage ont été remplies et validées. La structure du dépôt a été vérifiée, l'environnement virtuel configuré et la suite de tests exécutée avec succès.

Validation réalisée :
- 38 tests passés
- 0 erreur(s)
- 0 avertissement(s)

Fichiers clés :
- `docs/cadrage/cas1-pharmacie.md`
- `docs/cadrage/cas2-reglement.md`
- `docs/cadrage/cas3-avis-negatifs.md`
- `README.md`

Captures :
- `TP0-A.png`, `TP0-B.png`
- `TP1-T0.png` à `TP1-T6.png`

## 4. TP2 — Entraînement du modèle

Le deuxième volet du projet a consisté à entraîner un modèle capable de classer les avis comme positifs ou négatifs. La solution repose sur un pipeline composé de vectorisation TF-IDF et de régression logistique.

Objectif :
- validation de la performance du modèle sur un jeu de test non vu pendant l'entraînement ;
- sauvegarde du modèle entraîné dans `models/sentiment.joblib`.

Captures prévues :
- `TP2-C1.png`
- `TP2-C2.png`
- `TP2-C3.png`

## 5. TP3 — API de prédiction

Le modèle est ensuite intégré dans une API afin de pouvoir effectuer des prédictions à distance à partir de textes soumis par un client.

Objectif :
- exposer le service de prédiction ;
- valider les entrées/sorties et le comportement du service.

Captures prévues :
- `TP3-C1.png`
- `TP3-C2.png`
- `TP3-C3.png`

## 6. TP4 — Interface utilisateur

Une interface de démonstration a été envisagée afin de rendre le système accessible à un utilisateur non technique. Elle permet de saisir un avis ou de traiter un fichier CSV contenant une colonne `review`.

Objectif :
- démonstration du service de classification dans un environnement ergonomique.

Captures prévues :
- `TP4-C1.png`
- `TP4-C2.png`
- `TP4-C3.png`

## 7. TP5 — Validation fonctionnelle et intégration

La validation fonctionnelle a pour objectif de vérifier la cohérence globale du système, de la donnée à la réponse finale. Elle assure l'intégration des différents modules et la robustesse du service.

Objectif :
- vérifier le bon fonctionnement des composants et des flux de données.

Captures prévues :
- `TP5-C1.png`
- `TP5-C2.png`
- `TP5-C3.png`

## 8. TP6 — Finalisation et remise du projet

Le TP6 consiste à finaliser le livrable, consolider la documentation et préparer la présentation du projet dans son ensemble.

Objectif :
- présenter le projet de manière claire et structurée ;
- valider le dépôt dans son intégralité.

Captures prévues :
- `TP6-C1.png`
- `TP6-C2.png`
- `TP6-C3.png`

## 9. Conclusion

Le projet est validé au terme du TP1 et constitue une base solide pour la suite du développement. Les étapes suivantes permettent d'aboutir à un système complet, fonctionnel et documenté, du cadrage initial jusqu'à la remise finale du projet.
