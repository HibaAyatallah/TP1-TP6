# Fiche de cadrage : Ordonnances incomplètes en pharmacie

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Détecter automatiquement les ordonnances incomplètes afin d'éviter la validation d'un traitement partiel ou dangereux.

## Utilisateur final (obligatoire)

Le pharmacien et son équipe de validation, qui doivent être alertés avant la préparation ou la délivrance du médicament.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [x] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

Les dossiers d'ordonnance passés sont déjà étiquetés par les pharmaciens lors de la validation, ce qui favorise un classifieur supervisé (a). La vérification finale reste humaine, mais le modèle est rapide et peu coûteux à exécuter en masse (c), tandis que la conséquence d'une erreur est grave car une prescription incomplète peut conduire à un traitement incorrect ou à une mauvaise délivrance (d). La solution doit aussi rester explicable et aisément auditable, ce qui limite les risques d'une décision opaque (b).

## Données nécessaires et leur origine (obligatoire)

Il faut les champs de l'ordonnance (médicament, dosage, posologie, patient, prescripteur, durée), les données de validation historiques et l'état final de la prescription, issus du système de gestion de la pharmacie ou des dossiers logiciels de prescription.

## Métrique de succès et seuil d'acceptation (obligatoire)

On mesurerait le rappel sur la classe « ordonnance incomplète » et la précision globale, avec un seuil de 0,95 de rappel et au moins 0,90 de précision sur un jeu de test séparé.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une ordonnance incomplète validée à tort peut entraîner une délivrance inadéquate ou un traitement dangereux pour le patient. Un pharmacien vérifie donc toute alerte avant la préparation, et les erreurs de détection sont remontées au système pour améliorer les données.

## Risques éthiques ou de confidentialité (obligatoire)

Les données de santé sont sensibles ; il faut anonymiser les fichiers, limiter l'accès et stocker les résultats dans un environnement sécurisé conforme à la réglementation.

## Approche écartée et pourquoi (facultatif)

Les règles métier simples ne suffisent pas car les cas incomplets varient selon les prescripteurs et les formulaires, tandis qu'un modèle supervisé exploite les erreurs déjà corrigées par les pharmaciens.

