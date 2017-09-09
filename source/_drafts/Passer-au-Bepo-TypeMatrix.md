---
title: Passer au Bépo TypeMatrix sous Linux (Ubuntu)
tags: Bépo
---


*Vous avez décidé de sauter le pas afin de soulager vos poignets: vous passez au bépo.
Pour ne pas faire les choses à moitié, vous avez même investi dans un nouveau clavier ergonomique.
Félicitations !*

 *C'est le moment d'installer le clavier*
<!-- more -->



 > <span style="color:red">⚠ Ne réalisez ces opérations que lorsque vous êtes sûrs de pouvoir passer définitivement en mode bépo; par exemple, assurez vous de pouvoir taper tous vos mots de passe sans difficulté avec le nouveau clavier.</span>

___
## Configurez l'agencement du clavier

* Ouvrez un terminal et lancez la commande `sudo dpkg-reconfigure keyboard-configuration`
* Selon votre type de clavier, sélectionnez un des TypeMatrix (ou la marque correspondant à votre clavier). Pour ma part, j'ai sélectionné « TypeMatrix EZ-Reach 2030 USB », qui était abrégé « TMx2030USB » sur l'emballage du clavier.
* Pour les autres questions, à moins de connaître la réponse, appuyez sur entrée: cela conserve la réponse par défaut.


## Passez en mode de saisie bépo

* Ouvrez les paramètres de saisie de texte (sans doute une petite icône
[FR] en haut à gauche)
* En dessous de « sources d'entrée à utiliser », si « Français (Bépo, ergonomique, façon Dvorak) » n'apparaît pas dans la liste, il faut le rajouter. Vous pouvez l'ajouter avec l’icône en forme de petite croix en bas de l'encart.

Pour vérifier que vous avez la configuration qui correspond effectivement à votre clavier, il y a une dernière étape:

* Comparez la disposition de votre clavier à celle que vous pouvez visualiser en cliquant sur la même petite icône [Fr] et en sélectionnant « Agencement du clavier ».
* Si ce n'est pas la même, il vous faudra relancer la commande `dpkg-reconfigure keyboard-configuration` et sélectionner un autre clavier.

Vous pouvez à présent ouvrir un éditeur de texte et commencer à taper (en pensant bien à désactiver le pavé numérique).

## Optionnel — Désactiver votre clavier natif sous Linux (Ubuntu)

Si vous branchez votre nouveau clavier USB sur votre ordinateur portable, il se peut que vous désiriez désactiver le clavier built-in. Dans ce cas, vous pouvez le faire en tapant les commandes suivantes, selon si vous désirez désactiver votre clavier temporairement ou définitivement:


### Désactivation temporaire

(extrait traduit de [ceci](https://askubuntu.com/questions/160945/is-there-a-way-to-disable-a-laptops-internal-keyboard)):

* Lancez la commande `xinput list`. Cette commande liste les périphériques d'entrées (souris, clavier, touchpad...).
* Dans la liste, vous devriez voir apparaître « AT Translated Set 2 keyboard ». Il s'agit de votre clavier d'ordinateur portable, celui que vous souhaitez désactiver. Relevez son numéro d'**id** et aussi le numéro du « **master** », qui se trouve à cet emplacement: `[slave keyboard (#master)]`
* Pour désactiver le clavier, exécutez la commande `xinput float <#id>`, où `<#id>` est ne numéro que vous avez relevé en face de « AT Translated Set 2 keyboard ». Par exemple si l'id était 14, la commande à lancer est  `xinput float 14`.
Il est également possible de le désactiver avec la commande `xinput disable "AT Translated Set 2 keyboard"` directement.

Pour réactiver ce clavier là, il faudra lancer la commande `xinput reattach <#id> <#master>`.


### Désactivation « définitive »

* Éditer (en mode super utilisateur) le fichier `/etc/default/grub`.
* Trouver la ligne `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"` et la remplacer par `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash i8042.nokbd"`. Sauvegardez.
* Mettez votre grub à jour avec la commande `sudo update-grub` et redémarrez votre ordinateur.


# Conseils génériques pour une transition au bépo

 Les principaux conseils pour réussir votre transition vers une nouvelle disposition de touche tiennent en 2 lignes:
 - [Ne pas regarder son clavier lors de l'apprentissage](https://bepo.fr/wiki/Apprentissage). Vous pouvez par exemple vous entraîner plusieurs heures par jour sur [Bépodactyl](http://tazzon.free.fr/dactylotest/bepodactyl/).
 - Ne pas revenir en arrière (malgré les tentations). Dès lors que vous passez une de vos machine en Bépo, tenez-vous y.

 ___

 *Billet rédigé en 2 heures pour la première prise en main de mon nouveau TypeMatrix.*
