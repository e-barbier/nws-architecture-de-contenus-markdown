# Architecture de contenus en Markdown

Dans ce chapitre, nous verrons ce que sont les "typologies de contenus", les "taxonomies", les "metas", les produire et les organiser avec des fichiers [Markdown](https://fr.wikipedia.org/wiki/Markdown).

Vous trouvez, ici un dossier "exemple-structure" contenant quelques exemple de structure.


## Typologie de contenu

Pour déterminer ma stratégie de communication en ligne, il me faut maîtriser la **typologie des informations** que je souhaite proposer. En d’autres mots, je dois pouvoir identifier et distinguer les types d’information que je peux donner à mes publics et adapter ces types à leurs **besoins**, **comportements** et **tendances**.

Voici quelques exemples de types de contenu et leur usage :

### Les pages

Elles sont de type dit "hiérarchique. C'est à dire qu'elles peuvent s'organiser en arborescence. En d'autres termes, une page peut être enfant de sa parente.

Pour créer une page, il suffit simplement de mettre un fichier à la racine du dossier "content". Si vous souhaitez créer des sous-pages, vous créez un dossier représentant le premier niveau, dans lequel vous mettez une page index

Exemple :

```
- Page parente
  - Page enfant
  - Page enfant
  - ...
- Page parente
  - Page enfant
  - Page enfant
  - ...
```

Et les informations "meta" dont nous aurions besoin pour notre page seraient simplement "Le titre".
Nous aurons également besoin du "contenu" situé en dessous des `---` fermant le frontmatter. Ce qui pourrait se traduire en markdown par :

```
---
title: "Titre de ma page"
---

Ici le contenu de ma page au format Markdown
```

### Les articles

Dit non hiérarchique. C'est à dire que chaque article est au même niveau que les autres :

En revanche, contrairement aux pages, ils sont classés par date de publication ou par ordre alphabetique. Puisqu'ici, ce qui est important, c'est de placer son article d'actualité dans une temporalité. C'est ainsi que la plus part des médias (ex. *Le Monde*, *Le Parisien*, *Paris-Normandie*, etc...) fonctionnent. De ce fait, la date est une information que l'on doit pouvoir exploiter.

On peut donc retrouver cette information dans le nom du fichier :

```
- 2020-11-24-mon-second-article.md
- 2020-11-22-mon-premier-article.md
- ...
```

Le classement systeme des fichiers par rapport à leur nom fait naturellement le classement par ordre alpha/numerique.

On peut aussi décider d'exploiter cette information comme une data que nous retrouverons, dans notre exemple en Markdown, dans le frontmatter. Et ici, contrairement aux pages, nous aurions besoin du nom de l'auteur que nous ajouterons dans notre Frontmatter :

```
---
title: "Mon titre d'aticle"
date: 2020-11-24
author: "Raphael"
---

Contenu de l'article au format markdown...
```

## Taxonomies

Les taxonomies permettent de classer nos contenus en catégories. On peu aussi créer plusieurs taxonomies différentes. Dans notre exemple ci-dessous, nous retrouvons deux **taxonomies** (ici "Catégories" et "tags") contenant chaqu'une un ou plusieurs **termes**

```
---
title: "Mon titre d'aticle"
date: 2020-11-24
author: "Raphael"

categories: ["Cours"]
tags: ["Taxonomies", "Rédactionnel", "Web"]
---

# Titre de mon article

Contenu de l'article au format markdown...
```

## Les metas

Les metas permettent d'ajouter des informations à un contenu.

Dans le cas par exemple d'une fiche de film (qui est vous l'aurez compris, un type de contenu), nous aurions besoin de : l'année de sortie, le réalisateur, etc...

Nous pourrions le traduire ainsi dans notre frontmatter :

```
---
title: "La Ligne verte"
date: 2020-11-24

genres: ["Policier", "Fantastique"]

realisateur: "Frank Darabont"
sortie: "1 mars 2000"
duree: "3h09min"
---

# La Ligne verte

Paul Edgecomb, Gardien-chef du pénitencier de Cold Mountain en 1935, était chargé de veiller au bon déroulement des exécutions capitales. Parmi les prisonniers se trouvait un colosse du nom de John Coffey...
```

Vous constaterez également que nous avons ajouté une nouvelle taxonomie "Genre" qui nous permettra de regrouper les films par genre.

## Exercice

Le but de l'exercice est de créer et structurer, à l'aide de dossiers et fichiers Markdown, différent types de contenus.

  1. Créez votre dossier de projet "nom-de-mon-projet"
  2. Créez un dossier "Content" dans lequel vous prototyperez vos contenus
  3. Pour chaqu'un de ces types de contenus, vous ajouterez des metas ainsi qu'une ou plusieurs taxonomies pour les classer.
  4. Enfin, pour chaque contenu, vous ajouterez un peu de contenu éditorial


### Condition de rendu

Pour le rendu, vous avez deux possibilités :

**Sur github** : Dans un dépôt et vous mettrez le lien sur Classroom.

ou, si vous n'êtes pas à l'aise avec Github,

**Sur classroom** : Dans un dossier zippé contenant votre code source.

### Barème de notation

 - Création et organisation des types de contenus ( __/4)
 - Création de metas appropriées pour chaque types de contenus ( __/4)
 - Création de taxonomies pertinantes ( __/4)
 - Bonne structuration sémantique de vos contenus ( __/4)
 - Respect des consignes, autonomie, respect des délais ( __/4)

