# Fiche de cadrage : Questions sur le règlement intérieur

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Répondre automatiquement aux questions sur le règlement intérieur à partir d'un corpus documenté, en donnant une réponse fiable et citée.

## Utilisateur final (obligatoire)

Les élèves et les personnels de l'école, qui demandent une clarification rapide sans devoir parcourir tout le règlement.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [ ] Machine learning
- [x] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

La bonne réponse doit être extraite du règlement existant et justifiée par les articles, ce qui donne une forte exigence de vérifiabilité (b). Le système peut s'appuyer sur des documents déjà disponibles et non sur des données annotées, ce qui évite le coût de création d'étiquettes (a). Le coût par requête reste raisonnable dans une école où la base est limitée, et une mauvaise réponse a des conséquences sur la compréhension des règles et la confiance des usagers (d).

## Données nécessaires et leur origine (obligatoire)

Le règlement intérieur, les procédures, les FAQs et les éventuelles clarifications de l'administration, tous extraits du site institutionnel ou des documents officiels de l'école.

## Métrique de succès et seuil d'acceptation (obligatoire)

On mesure la précision sur un ensemble de questions test, avec un seuil de 0,90 de bonnes réponses fondées sur les sources, ainsi qu'un taux de réponse avec citation d'articles supérieur à 0,95.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une mauvaise réponse peut provoquer une mauvaise interprétation d'une règle ou une sanction injustifiée. Un membre du service administratif vérifie donc les réponses sensibles avant envoi ou publication.

## Risques éthiques ou de confidentialité (obligatoire)

Les questions peuvent contenir des informations personnelles ou de contexte interne, mais le corpus est public ou institutionnel ; il faut néanmoins limiter l'accès et éviter toute réponse inventée ou non documentée.

## Approche écartée et pourquoi (facultatif)

Le modèle génératif seul est écarté car il peut citer des articles faux ou paraphraser le règlement sans preuve, ce qui est incompatible avec un document administratif officiel.

