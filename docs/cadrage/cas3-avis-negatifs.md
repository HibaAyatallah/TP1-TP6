# Fiche de cadrage : Priorisation des avis négatifs

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Identifier rapidement les avis négatifs les plus graves pour prioriser la réponse commerciale et améliorer la qualité de service.

## Utilisateur final (obligatoire)

L'équipe de support client et la direction e-commerce, qui doivent trier les plaintes selon leur urgence et leur risque pour la relation client.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [x] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

Le site possède déjà des milliers d'avis historiques, souvent annotés par le service client selon le type de problème et l'urgence, ce qui suffit pour un modèle supervisé (a). Le coût est très faible par requête quand on traite des flux volumineux, et la vérifiabilité est acceptable parce que l'on peut évaluer la précision et le rappel sur un jeu de test séparé (b, c). Une mauvaise priorité a une conséquence concrète sur la satisfaction client, donc il faut un seuil strict et une relecture humaine pour les cas les plus critiques (d).

## Données nécessaires et leur origine (obligatoire)

Les avis clients, leur note, le texte libre, la catégorie de réclamation et l'histoire de traitement, extraits de la base de commentaires du site et des tickets de support.

## Métrique de succès et seuil d'acceptation (obligatoire)

On cible la précision et le rappel sur la classe des avis à traiter en priorité, avec un F1 macro supérieur à 0,80 et un rappel sur les cas critiques d'au moins 0,90.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Un avis grave classé comme banal peut retarder une réponse à un client mécontent et nuire à la marque. Une équipe support valide donc les avis classés comme critiques avant l'action commerciale.

## Risques éthiques ou de confidentialité (obligatoire)

Les avis peuvent contenir des données personnelles ou des références à des transactions ; il faut anonymiser les textes avant traitement et ne pas les exposer inutilement à des équipes non autorisées.

## Approche écartée et pourquoi (facultatif)

Les règles métier sur des mots-clés seraient trop fragiles face à la variété des réactions clientes, tandis qu'un classifieur supervisé apprend mieux les schémas de plainte et la gravité.

