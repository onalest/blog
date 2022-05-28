---
title: Premier article
description: Premier article de test
author: onalest
date: 22 mai 2022
tags:
  - misc
---

_{{ date }} - {{ description }}_


## Motivation

Cela fait maintenant un certain temps que je souhaite écrire à nouveau, en langage naturel et dans ma langue maternelle, c'est-à-dire renouer avec un vecteur d'expression que j'ai trop longtemps laissé de côté. Ayant il y a environ deux ans pris la décision de changer l'agencement de mon clavier de l'AZERTY vers le QWERTY, et n'ayant plus l'occasion dans ma vie de tous les jours d'écrire en français, à l'exception donnée du téléphone, j'ai progressivement perdu la capacité et la motivation à écrire dans ma langue sans recourir à la correction automatique, ou bien sans faire le choix délibéré d'omettre les accents.

S'exprimer dans un tel format me permettra aussi d'alléger les proches que j'ai pu encombrer de mes longs _pavés_...

Mais avant de commencer, il faut mettre en place un certain environnement de travail confortable afin d'éloigner toute contrainte inutile.

## Outils


### `qwerty-fr`

Puis, une collègue m'a parlé d'un type d'agencement spécial, [`qwerty-fr`](https://qwerty-fr.org/), permettant d'écrire les lettres accentuées de la langue française sans se contorsionner les doigts. En écrivant ces lignes, j'apprends progressivement son utilisation.
Malheureusement, je n'ai pas pu associer sur Ubuntu la touche spéciale permettant de transformer une lettre vers une lettre accentuée via la touche ++super++ gauche, j'utilise donc la touche ++alt++ droite. Il ajoute également le fameux tiret long — habilement placé sur la touche ++minus++. Enfin, l'écriture de majuscules accentuées se fait simplement en maintenant la touche ++shift++ enfoncée.

Voici une liste non exhaustive de combinaisons de touches permettant l'insertion d'une lettre accentuée :

- ++alt+w++ : é
- ++alt+e++ : è
- ++alt+3++ : ê
- ++alt+9++ : ô
- ++alt+c++ : ç
- ++alt+a++ : à
- ++alt+shift+w++ : É
- ++alt+shift+e++ : È
- ++alt+shift+3++ : Ê
- ++alt+shift+9++ : Ô
- ++alt+shift+c++ : Ç
- ++alt+shift+a++ : À
- ++alt+minus++ : —

Pour activer cet agencement j'utilise :

```bash
setxkbmap us qwerty-fr
```

### Editeur de texte et langage

Afin de pouvoir écrire mon texte sans avoir à recourir à des outils différents de ceux que j'utilise au quotidien, je recoure à... VSCode. En effet, j'ai déjà pour habitude de prendre mes notes en texte brut et au format [Markdown](https://fr.wikipedia.org/wiki/Markdown), cela me paraissait donc naturel de faire de même pour ce projet.

### Générateur de site statique

Bien que le texte brut présente de nombreux avantages, tels que le versionnage via Git, une moindre dépendance vers des logiciels tiers obfuscant les données sauvegardées, il reste la question du _style_, c'est-à-dire comment rendre le texte vers une page web facilement accessible. Pour cela, j'utilise [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), une surcouche de l'outil de documentation `mkdocs` offrant la possibilité de convertir un dossier contenant des fichiers markdown en un joli site statique en quelques commandes. Cet outil à été conçu initialement pour gérer de la documentation, en ayant pour philosophie de considérer la documentation comme du code. J'adhère à ce principe également pour gérer mes posts.

### Hébergement

Le code source est stocké sur GitHub, qui fournit également un service d'hébergement gratuit de sites statiques, ce qui est exactement le cas de ce blog.


### Corrections orthographique

Il est possible de faire passer le texte brut à la moulinette d'un utilitaire nommé `aspell`.

```bash
sudo apt install aspell
sudo apt install aspell-fr
```

Pour ce fichier par exemple :

```bash
aspell check --lang=fr docs/blog/2022/premier.md
```

## Conclusion

Mon environnement d'écriture étant en place, je devrais maintenant pouvoir m'exprimer. Trop bien !