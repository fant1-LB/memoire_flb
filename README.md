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
**PAS ENCORE FONCTIONNEL, DOIT ETRE REPRIS**
Ce dossier contient 2 notebooks, qui pour le premier crée un fichier csv contenant les métadonnées de chaque oeuvre, télécharge l'image dans laquelle est contenue chaque oeuvre, et un fichier texte avec les coordonnées de chaque oeuvre sur chaque image.
Le deuxième notebook transforme le dit fichier texte en un csv contenant les coordonnées pour chaque image.
Comme pour le pipeline de segmentation il vaut mieux l'executer dans un environnement virtuel et executer la commande :

    pip install -r scrapping/requirements.txt

