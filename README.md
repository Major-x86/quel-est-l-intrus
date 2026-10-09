# Quel est l'intrus ? 100 tests de logique visuelle

Un site d'entraînement au raisonnement logique, entièrement en français. Chaque question présente cinq figures numérotées : quatre suivent la même règle, une seule y échappe. Il faut trouver laquelle.

**Démo en ligne :** https://major-x86.github.io/quel-est-l-intrus/

## Ce que propose le site

- 100 questions réparties en 5 séries de 20, de difficulté croissante
- Deux modes : entraînement sans limite de temps, ou chrono de 40 secondes par question
- Deux indices par question : le premier désigne le critère à observer, le second écarte deux mauvaises réponses
- Une correction expliquée après chaque réponse
- Un bilan en fin de série (score, points, temps, indices utilisés)
- Une progression enregistrée dans le navigateur, avec reprise là où l'on s'est arrêté
- Un affichage adapté aux ordinateurs, aux iPhone et aux téléphones Android, avec un mode sombre automatique
- Des raccourcis clavier : touches 1 à 5 pour répondre, H pour un indice, flèches pour naviguer

## Les séries

| Série | Contenu |
|---|---|
| 1 | Les bases : une seule différence, tout le reste est identique |
| 2 | Six règles possibles, détails fixes |
| 3 | Des couleurs et des détails qui varient pour brouiller les pistes |
| 4 | Un lien entre le nombre de triangles et le nombre de côtés s'ajoute |
| 5 | Plus d'éléments, des couleurs et des règles liées |

## Barème

Une bonne réponse rapporte 1 point sans indice, 0,5 point avec un indice et 0,25 point avec deux indices. Une réponse fausse ou un temps écoulé vaut 0.

## Comment les questions sont fabriquées

Les figures ne sont pas dessinées à la main. Chaque question est générée par du code à partir d'une graine fixe, ce qui donne toujours les mêmes 100 questions.

Une règle porte sur l'un de ces critères : le nombre de petits triangles, le nombre de côtés de la forme centrale, le remplissage des triangles, le remplissage de la forme centrale, la présence d'un point au centre, le sens des pointes (vers le centre ou vers l'extérieur), ou le lien entre triangles et côtés.

Après chaque génération, le programme contrôle qu'une seule règle désigne un intrus. Si un autre critère isole aussi une figure par hasard, la question est rejetée et régénérée. Chaque question a donc une seule bonne réponse, justifiable.

## Lancer le projet

Aucune installation n'est nécessaire. Le site tient dans un seul fichier.

1. Télécharge `index.html`.
2. Ouvre-le dans ton navigateur, ou lance un petit serveur local :

```
python -m http.server 8000
```

puis ouvre `http://localhost:8000`.

## Technologies

HTML, CSS et JavaScript, sans framework ni dépendance. Les figures sont des SVG produits par le script. Seules les polices Sora et Inter sont chargées depuis Google Fonts, avec des polices de secours si elles ne sont pas disponibles.

## Limites

Ce sont des exercices d'entraînement. Ils n'ont fait l'objet d'aucun étalonnage et ne mesurent pas un QI. Ils ne remplacent pas un test psychotechnique officiel.

## Pistes d'amélioration

- Ajouter d'autres règles : symétrie, position, rotation
- Proposer un mode de questions aléatoires
- Ajouter un classement par série

## Auteur

Chris Kazanga
