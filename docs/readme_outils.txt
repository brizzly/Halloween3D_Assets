==============================

 Pour la compilation des maps

==============================


A. Compilation Normale/developpeur:
-----------------------------------
ase.exe fichier.ase
bsp.exe fichier.pts

 => fichier.map

Compilation rapide et sans problemes de geometrie utilisee pendant le developpement des maps.
On obtient au final un FPS moyen linéaire avec le nombre de faces.


B. Compilation Finale:
----------------------
ase.exe fichier.ase
bsp.exe -v fichier.pts
vis.exe fichier.map

 => fichier.map, fichier.prt, fichier.pvs

Compilation plus lente et a risquee selon la geometrie utilisee pour calculer la visibilite finale dans la map.
On obtient au final un bien meilleur FPS non linéaire avec le nombre de faces. Risque de bugs!!
(Les maps en exterieurs ne sont pas geree pour le moment).


C. Relecture des maps dans le jeu:
----------------------------------
Compiler une map soit avec la méthode A. ou B. au choix.
Placer les fichiers ci-dessus dans le repertoire /system/maps
Placer les textures utilisées dans le repertoite /system/textures
Le format des textures est du TGA (NON COMPRESSE) 24/32Bits de taille: (n^2 x m^2).


D. Astuces:
-----------
1. Pour mettre un point de depart dans une map placer une boite portant le nom: startX ou X est un entier compris entre 0 et 259. Il s'agit de l'orientation en degre de la camera au point de depart situe par la boite. (Ex: start180).
2. Nommer dans l'editeur les petits objets de details en: detail.
3. Nommer dans l'editeur les surfaces liquides en: lava.
4. Utiliser le grid 10 de l'editeur pour placer correctement ses points et ainsi obtenir un alignement parfait.
5. Utiliser texture UVW box 100 100 100 (ou autres valeurs) pour placer correctement les textures.
6. Exporter en *.ASE avec le mode Mapping Coordinates.
7. Configurer les chemins d'exportation.. par exemple: system/maps/
8. Lors d'une copie depuis un CDROM s'assurer que les fichiers de textures sont en mode Archive seulement.
9. Pendant le developpement des maps, mettre halloween en mode fenetree pour eviter de perdre du temps avec les changement de mode video, qui peuvent a la longue user inutilement l'ecran.
10. Dans l'editeur de map, dans la pile des modifications, placer le <<Texture UVW>> en haut de la pile pour que ça texture l'objet correctement.
11. Mettre un bloc et l'appeller << invisible >> dans l'editeur pour bloquer les mouvements du joueur au niveau de fenetres ou autre, sans que le bloc s'affiche dans le jeu.
12. Au moment du debogage de la map tapper << noclip >> dans la console pour passer a traver les murs et << pview >> pour etre en mode camera libre.
13. Se faire un repertoire d'objets deja modeliser << brushs >> et les mergers dans les maps pour etre efficace.



Bug? <julienm@jadeware.org>
--
(C) 2001 By Jadeware
ALL RIGHTS RESERVED.