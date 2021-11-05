# Filtre audio paramétrique

Cette documentation contient les différents éléments qui permettent de fabriquer le filtre paramétrique proposé :

- Fichiers Eagle (schéma électrique et routage)
- Fichiers Gerber
- Fichier d'implémentation des composants et dimensions
- Procédure de câblage (Wiki)
- Procédure de mise au point de la carte (Wiki)

Le filtre paramétrique proposé est inspiré de celiui proposé par Remy Mallard, Sonelec-musique https://www.sonelec-musique.com/electronique_realisations_filtre_bf_007.html﻿

# Procédure de câblage de la carte
Le câblage consiste à connecter par soudure tous les éléments ensembles (composants, connecteurs, sélecteurs, potentiomètres)
Le câblage de la carte peut être fait en 2 étapes que voici :
﻿
## Etape 1 : Soudure des composants
En suivant le schéma d'implantation présenté précédemment vous pouvez souder, dans l'ordre proposé, les éléments suivants :

1) Les liaisons filaires interne à la carte (aussi appelés strap ou jumper) en utilisants des fils (blanc par exemple)

2) Les résistances

3) les condensateurs

4) les deux supports de circuits intégrés

5) souder les potentiomètres sur la carte.
﻿
## Etape 2 : Câblage des éléments extérieurs
ATTENTION : les pastilles peuvent être fragiles et se décoller facilement, prenez soin d'être délicats !
Il est conseillé de câbler dans un premier temps tout les câbles sur le circuit imprimé. Les éléments extérieurs (connecteurs XLR, sélecteur et potentiomètre seront câblés en dernier)

1) Câbler l'alimentation externe sur la carte de circuit imprimé

* +12V en rouge
* - 12 V en orange
* gnd (la masse) en noir

﻿
2) Souder les fils de l'entrée audio sur la carte de circuit imprimé

* gnd en noir
* Le signal d'entrée en une couleur autre que le rouge ou le orange
* Les fils seront ensuite soudé à l'autre extrémité sur les connecteur XLR lorsque tous les câbles de tous les composants seront soudé à la carte (c'est juste un conseil, aucune obligation

﻿
3) Souder les fils de  sortie audio sur la carte de circuit imprimé

* gnd en noir
* Le signal de sortie en une couleur autre que le rouge ou le orange

﻿4) Souder les fils de l'inverseur dans des couleurs non-utilisés

5) Souder les fils des potentiométres

6) Souder enfin les connecteurs XLR, le sélecteur et les potentiomètres.

# Liste des composants nécéssaires
### Résistances

* 100 Ohm x1 (R4)
* 2k2 Ohm x1 (R8)
* 3k9 Ohm x1 (R11 et R12)
* 10k x 2 (R13, R15)
* 11k Ohm x1 (R16)
* 51k Ohm x 2 (R5 et R4)
* 100k Ohm x7 (R1, R2, R3, R6, R7, R9, R10)

### Condensateurs

* 1nF x2 (C2,C 3)
* 10 nF x2 (C4 et C5)
* 220 nF (C1)

### Potentiomètres

* 100k x1  (potentiomètre double) (RV3)
* 22k x1  (potentiomètre Simple Linéaire) (RV1)
* 100 k Ohm  (Potentiomètre simple logarithmique) (RV2)

﻿
### Amplificateurs opérationnels et leurs supports

    1	TL082P			
1	support DIL08
    1	TL084P	
    1 support 	DIL14	U2	OP AMP	avec son support

﻿
Inverseur

    Inverseur 2P2T
    l'interrupteur étant déporté, il faut utiliser du cable souple

﻿
Du câble souple pour :

    Câbles souples pour l'interrupteur
    -12 (orange)  +12(rouge)   gnd (noir)
    gnd (noir)  entr√©e	PINHD-1X2	1X02	J_IN	PIN HEADER
    sortie   gnd(noir)	PINHD-1X2	1X02	J_OUT	PIN HEADER

﻿
﻿
Du câble rigide pour les jumpers