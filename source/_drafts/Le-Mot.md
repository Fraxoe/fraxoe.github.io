---
title: Le Mot
tags:
- Linguistique
- NLP
- Tokenisation
---

*De nombreux concepts fondamentaux, et pourtant ambigus, discutés en linguistique sont liés aux unités de base autour desquelles se structurent les langues. En fonction de la perspective linguistique ou de la langue considérée, il peut arriver qu’il n’y ait pas de consensus concernant la question des unités les plus basiques comme le morphème ou le mot.*

*C'est du mot dont il sera question dans ce billet.*
<!-- more -->

___
# Le mot existe t'il ?

Le locuteur du français a une compréhension intuitive de ce qu’il considère être un mot, intuition fondée sur la typographie. Le français, comme la plupart des écritures alphabétiques, dispose de caractères de segmentation «évidents» (espaces et ponctuation) pour permettre au lecteur d’identifier confortablement les éléments du lexique.
Les étudiants linguistes apprennent rapidement que le«mot», qui semble intuitivement être une notion triviale, est difficile à définir formellement.

## Un exemple

     J'ai regardé germer cette pomme de terre.

 Cette phrase comporte 8 mots typographiques (que l'on appellera aussi«tokens»), séparés par des espaces ou des marques de ponctuation (ici, une apostrophe). Deux éléments posent question dans leur nature de mot:
* *pomme de terre* (1 ou 3 mots ?)
* *J'ai* (1 ou 2 mot(s) ?).

## Définitions proposées


Packard (2000) a recensé plusieurs définitions possibles du mot. Parmi elles, les mots lexicaux , les mots sémantiques, les mots morphologiques et les mots syntaxiques. Ces définitions se situent à différents niveaux d’analyse linguistique.

 Au niveau **syntaxique**, les mots sont des entités qui peuvent apparaître librement dans le discours et être remplacées par des entités similaires au même emplacement sur l’axe syntagmatique. Ces entités, lorsqu’elles se situent sur un même axe paradigmatique, possèdent la même partie du discours.

 Dans la phrase d'exemple précédente, «*J'*» (ou«*je*» ne peut pas apparaître indépendamment du verbe, avec lequel il forme«un seul mot **prosodique**» (Miller & Monachesi, 2003). Ce type d'unité, dont les propriétés semblent à première vue intermédiaires entre celles des mots et celles des affixes, sont appelées *clitiques*.
«*pomme de terre*» peut être remplacé par«*fleur*», avec la même partie du discours (ici, un nom).

 Au niveau **morphologique**, les mots sont « les sorties correctes produites par les règles morphologiques de la langue ». Une analyse morphologique sur ces mots, selon leur complexité, permet d’identifier des morphes, des racines ou même des lemmes, ainsi que des catégories flexionnelles.

 Les mots **lexicaux** correspondent aux associations « idiosyncratiques et arbitraires de sons et de sens » ne pouvant pas être déduites de règles de formations (Packard , 2000 , p.9). Typiquement, ce sont des unités susceptibles d’apparaître dans des listes lexicales, à l’instar d’entrées de dictionnaires. Les trouver de façon automatique est une tâche complexe car il s’agit d’identifier des unités de type lemme (dans les langues exhibant des phénomènes de flexion et de dérivation), mais aussi des locutions, des termes, voire des entités nommées.

 Les mots **sémantiques** font quand à eux référence à des concepts unitaires, qui en appellent plus aux propriétés ontologiques qu’aux propriétés fonctionnelles d’un mot. On peut considérer qu’il existe une équivalence grossière entre le mot sémantique et le mot lexical .


	 [TODO: Autres définitions du mot ? cf Magistry ( 2013 )]

 Comme le montre l'exemple«*pomme de terre*», il n'y a pas nécessairement de correspondance entre ces différents mots (ici, le mot typographique et le mot lexical/sémantique).


# Le mot n'existe pas !


Nous venons de le voir, définir ce qu'est un mot en français est une tâche plus délicate qu'il n'y paraît. Il est encore plus difficile d’avoir une notion de mot valable à travers les langues.
Comme nous l'avons vu, un première indice permettant une première approximation des frontières de mot dans la plupart des systèmes syllabographiques et phonographiques réside dans l'utilisation des séparateurs de mots typographiques (espaces, ponctuation...). Or les systèmes d’écritures utilisés par les langues ont un impact considérable sur la segmentation. [Faire un billet sur la typologie des langues]


Prenons des exemples dans 3 langues topologiquement très éloignées:




Cette intuition, influencée par l’environnement linguistique du locuteur, peut toutefois varier d’une personne à l’autre, et ce même si des connaissances linguistique sur les questions relatives au mot entrent en jeu ( Allwood etal. , 2010 ). Cette notion est encore plus ambiguë si on l’envisage depuis des langues très différentes : un Inuit et un Chinois auront probablement de grandes difficultés à comprendre intuitivement quel est le mot de l’autre


mots morphologiques: Il est relativement aisé de les détecter dans du texte. Cependant, ils ont pour inconvénient, dans les langues analytiques, d’être des variantes d’un même mot sémantique.

Cette tendance n’est pas systématique. Par exemple, les systèmes d’écritures employés par des langues
comme le thaï (abugida), le grec primitif ou latin classique (alphabets) sont ou ont été
scriptio continua. À l’inverse, il peut exister une « sur-segmentation ». C’est la cas en vietnamien, comme cela sera évoqué par la suite.






Parler des clitiques, de pomme de terre,...




Approche computationnelle: Représentation du mot

https://arxiv.org/pdf/1607.04606.pdf

co-occurrence
Sémantique distributionnelle / word embedding


Représenter un mot avec un vecteur, mais ignorent la structure interne du mot, ce qui est limitant dans les langues à morphologie riche (https://arxiv.org/pdf/1607.04606.pdf).


___


# Bibliographie

Résumé de https://hal.archives-ouvertes.fr/tel-01257201/document


