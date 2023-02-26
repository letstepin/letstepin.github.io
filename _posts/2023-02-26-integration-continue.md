---
layout: post
title:  "L'intégration continue, c'est quoi ?"
author: henri
categories: [ Jekyll, tutorial ]
image: assets/images/6.jpg
---
Nous allons voir, comment faire en sorte que votre code soit prêt à être déployé. L'intégration continue est une culture dans une équipe de développement qui consiste à ce que les déveleppeurs intègrent régulièrement leurs modifications à une branche principale de code. De ce fait, des opérations de création de test sont automatiquement menées. L'objectif principal est de corriger le plus tôt possible les bogues, d'améliorer la qualité du logiciel et surtout réduire le temps nécessaire pour valider et publier les nouvelles mise à jour.

## Quel est le problème ? 
Imaginons une équipe composée de plusieurs déveleppeurs travaillant sur de nouvelles fonctionnalités pour une de leurs applications. Chacun des développeurs a travaillé sur des branches séparées pendant deux (2) semaines. Maintenant, ils sont tous prêts à fusionner leurs changements avec la branche principale. Soudain, plein de conflits remplissent leur console! Avec les délai de livraison le responsable de l'équipe est forcément déçu car ça prend beaucoup plus de temps. Cela aurait pu être évité s'ils avaient utilisé une approche d'intégration continue.

## Pourquoi l'intégration continue ?

L'intégration continue est une pratique qui se compose de deux éléments principaux :
1. Fusionner les modifications du code source sur une base **fréquente**.
2. Produire les changement sous leurs forme définitive et les tester, le tout, dans un processus automatique.
La combinaison de ces deux pliés garantit que les nouveaux ajouts sont souvent produits et testés.

L'intégration continue nécessite souvent de changer la façon dont nous travaillons avec la gestionnaire de configuration. Voyons pourquoi l'intégration continue peut nous inciter à nous éloigner des méthodes de développement traditionnel orienté par des branches de fonctionnalités.

## Approche traditionnelle de développement
Dans le passé, les approches traditionnelles de développement utilisaient une approche de gestion de configuration ayant branches à longue durée de vie. Ces branches n'étaient fusionnées qu'une fois la fonctionnalité associée à la branche est achevée. Cela peut fonctionner pour les petits projets avec un développeur. Cependant, des problèmes se posent avec les projets plus grand :

1. La durée de vie des branches sont relativement importante
2. Lors de la fusion de branches avec la branche principale il peut y avoir de nombreux conflits.

N'oubliez pas que l'objectif de l'intégration de composants est de fusionner, construire et tester **fréquemment les modifications** du code ur une branche principale. 

Discutons d'une approche de gestion de configuration compatible avec l'intégration continue.

## Gestion de configuration adaptée à l'intégration continue

Ce mode de développement consiste à fusionner fréquemment de petites modifications dans la branche principale. Voici quelques-uns des avantages de cette approche:
* La découverte précoce des bogues plutôt qu'à la fin.
* De petits changements signifient moins de conflits et des corrections plus simples.

Voici une illustration de ce que ça représente ![Intégration continue!](/assets/images/Continous_Integration.png "Schéma Intégration Continue")

Ainsi l'intégration continue combine d'une part cette approche de gestion de configuration, qui consiste à merger plus régulièrement les différentes branches et d'autres part l'automatisation de la construction des builds et des tests. Après chaque merge à la branche principale, une production de cette évolution est automatiquement lancée et testé. Ce processus permet d'avoir toujours dans notre base de gestion de configuration, un code source prêt à être déployé. Maintenant que nous comprenons le concept d'intégration continue, examinons quelques outils qui peuvent aider à l'automatisation.

## Outils populaires d'intégration continue
De nombreux outils d'intégration continue utilisent des serveurs pour surveiller les changements depuis le dépôt. ou les déclencheurs du référentiel du projet. Les outils peuvent être configurés pour exécuter des tests automatiquement. Les outils d'intégration continue les plus populaires sont les suivants :
* **Jenkins:** Jenkins est un outil open source de serveur d'automatisation. Il aide à automatiser les parties du développement logiciel liées au build, aux tests et au déploiement, et facilite l'intégration continue et la livraison continue.
* **Github Actions**, et **CircleCI**.

L'apprentissage d'au moins un de ces outils peut être très utile pour une équipe qui souhaite intégrer des pratiques d'intégration continue.

## Mise ne place des pratiques d'intégration continue

La mise en place des pratiques de l'intégration continue sur un projet passent par ces étapes suivantes :

1. S'assurer que le projet utilise une seule branche principale.
2. Choisissez un des nombreux outils pour contrôler les builds et les tests automatiques.
3. Configurer votre serveur d'intégration continue pour qu'il déclencher automatiquement les builds lors des fusions.
4. Développer des tests et configurer votre serveur d'intégration pour les exécuter.
5. Configurer des notifications pour des erreurs de build ou de test.

Cela semble représenter beaucoup de travail supplémentaire, mais heureusement, il existe de nombreux outils d'aide à l'intégration de composants. L'idée de l'intégration continue et que le code soit en état à être déployé.