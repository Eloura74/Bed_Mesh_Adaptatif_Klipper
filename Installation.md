

##  ##


<div align="center">
  
# **Installation** #
  
</div>

##  ##
<br>
<br>

## ## 
# **Marquer les Objets** #
##  ##

<br>

Vous devez tout d'abord définir **exclude_object** dans votre fichier **printer.cfg**.
<br>
Assurez-vous d'avoir **enable_object_processing: True** sous **[file_manager]** dans votre fichier **moonraker.conf**.
<br>
Cela permettra à Klipper de traiter les fichiers Gcode entrants pour marquer les objets.
<br>

Cela doit ressebmbler à ceci:
<br>

Moonraker.conf
<br>
```
[file_manager]
enable_object_processing: True
```
<br>

Et vous devez aussi dans votre **Slicer** (Superslicer pour ma part) **activer** le marquage des objets.
<br>

![image](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/image/Objet_PrusaSlicer.png)

<br>

## ## 
# **Mise à jour avec Moonraker** #
##  ##

<br>

Le but de cette configuration est d'activer la mise à jour de **KAMP** en utilisant le gestionnaire de plugins de Moonraker.

<br><br>
## ##
1.Connecter vous vous en SSH à votre Raspberry pour installer **KAMP** et ses fichiers avec ceci : 
<br>

```
cd
git clone https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging.git
ln -s ~/Klipper-Adaptive-Meshing-Purging/Configuration printer_data/config/KAMP
```

<br>

## ##
2.Veillez vous rendres dans votre fichier Moonraker.conf et ajouter ceci :
<br>

```
[update_manager Klipper-Adaptive-Meshing-Purging]
type: git_repo
channel: dev
path: ~/Klipper-Adaptive-Meshing-Purging
origin: https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging.git
managed_services: klipper
primary_branch: main
```

<br>

## ##
3.Ajouter ensuite les fichiers dans votre printer.cfg comme ceci:
<br>

```
[include KAMP/Adaptive_Mesh.cfg]
```
<br>

## ##
Vous devez maintenant redemarrer klipper.
<br>
Puis vous pouvez passer à la [suite](https://github.com/Eloura74/Bed_Mesh_Adaptatif_Klipper/blob/main/Macro.md)




