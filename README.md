## Bienvenue dans les annexes du mémoire de M2 TNAH de Fantin Le Ber ##

Le dossier MCD et le fichier présentation Arkindex sont à consulter normalement.

 # Relatif à l'usage du dossier pipeline segment #

Nous recommandons d'executer les fichiers dans un environnement virtuel.
Executer la commande :

    pip install -r pipeline_segment/requirements.txt

Dans le même dossier que le notebook pipeline.ipynb doivent se trouver :
- Un modèle Yolo adapté
- Le modèle pero_ocr, disponible ici : https://nextcloud.fit.vutbr.cz/s/NtAbHTNkZFpapdJ?openfile=true
- Des images au format .jpg à traiter, à mettre dans le dossier "images_a_traiter"

Les utilisateurs Linux/Mac devront remplacer les "\\\\" contenus dans les notebooks par un unique "/" pour adapter les chemins. 

# Relatif à l'usage du dossier scrapping #

**Les notebooks sont fonctionnels, mais le premier doit encore être mis en forme**

Ce dossier contient 2 notebooks. 
Le premier, "scrapping_complet_arcade.ipynb" produit les éléments suivant :
Une extraction de l'image correspondante à chaque oeuvre (triées par ordre alphabétique du nom d'auteur) pour une année x. Par exemple l'image de l'oeuvre numérotée Y de l'année X sera trouvable au chemin : "scrapping\albumX\imagehdX\imageY.jpg".
Un fichier csv contenant les informations à propos de chaque oeuvre d'une année x contenues dans la base. Pour la première année, ce csv sera ainsi trouvale au chemin : "scrapping\scrapping_def\scrap_final1\final_v3_1.csv"
Une série de fichiers texte ignorables contenant des liens utilisés pour naviguer au sein du notebook.
Un fichier de coordonnées des images, appellé dans le deuxième notebook pour être mis en forme. On peut y accéder si besoin, pour une année X au chemin "scrapping\resultats_scrapping\anneeX\images_zones_V2_X".
Le deuxième notebook transforme le dit fichier texte en un csv contenant les coordonnées pour chaque image, accessible pour une année X au chemin : "scrapping\coordonnees_completes\tableau_coordonneesX".

Comme pour le pipeline de segmentation il vaut mieux les executer dans un environnement virtuel, pour installer les dépendances, utiliser la commande :

    pip install -r scrapping/requirements.txt

A l'usage nous avons remarqué que les coordonnées n'étaient pas renseignées pour les dernières années de la base, il ne s'agit pas d'un bug du code mais bien d'une absence au sein de la base elle même. Il en va de même pour les métadonnées des oeuvres, dont les catégories sont inégalement remplies selon les oeuvres ou les années.
