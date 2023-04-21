# Bed_Mesh_Adaptatif_Klipper


##  ##

<div align="center">
  
![image](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/image/Readme.png)
  
</div>

##  ##

<div align="center">
  
# **Bed Mesh Adaptatif Klipper** #
  
</div>

##  ##

Ce projet, appelé **KAMP** (KlipperAdaptiveMeshingPurging), a été créé pour simplifier l'utilisation du maillage adaptatif sur Klipper. 
<br><br>

Le maillage adaptatif permet d'utiliser les valeurs d'un fichier Gcode pour définir les dimensions d'un maillage.
<br><br>

# **But:** #
<br>

Avoir les avantages d'un maillage de lit sans gaspiller du temps et des matériaux. KAMP a été conçu pour être simple et efficace.
<br><br>

# **Pourquoi utiliser le maillage adaptatif?** #
<br>
Construire un maillage de lit peut prendre du temps et gaspiller des matériaux si la taille du maillage ne correspond pas à la zone d'impression réelle.
<br>

Le maillage adaptatif permet de construire un maillage de lit plus efficace et adapté à la zone réellement utilisée lors de l'impression.
<br>
Cela permet d'améliorer la qualité de la première couche et de réduire le gaspillage de matériaux.
<br><br>

# **Comment fonctionne le maillage adaptatif?** #
<br>

Grâce au travail de [kageurufu](https://github.com/kageurufu) sur [[exclude_object]](https://github.com/kageurufu/preprocess_cancellation) dans le firmware Klipper, il est possible d'extraire la taille d'un objet tranché et de l'adapter à la taille d'un maillage de lit.
<br>
En analysant plusieurs objets dans le fichier Gcode, la densité du maillage peut s'adapter à n'importe quel nombre d'objets tant qu'ils s'adaptent à la plaque de construction. 
<br>
Les valeurs minimales et maximales d'un maillage de lit peuvent ainsi être facilement modifiées pour chaque objet tranché.

De plus, ces valeurs peuvent également être utilisées pour créer des [lignes de purge localisées](https://github.com/Eloura74/Purge_Adaptive_Klipper), ce qui permet d'éviter les longues promenades du plateau d'impression à la première ligne extrudée.
<br><br>

# **À quoi ressemble un maillage adaptatif?** #
<br>

![image](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/image/Exemple_BedMesh.png)

Un maillage adaptatif est créé à partir des valeurs extraites du fichier Gcode et est adapté à la zone réellement utilisée lors de l'impression.
<br>
Cela permet d'obtenir un maillage de lit plus efficace et une meilleure qualité d'impression.
<br><br>
Aller, nous allons voir comment [Installer ceci](https://github.com/Eloura74/Bed_Mesh_Adaptatif_Klipper/blob/main/Installation.md)
