##  ##

<div align="center">
  
# **Macro Start Print** #
  
</div>

##  ##

<br>
Vous devez modifier votre PRINT_START et appeler le Bed_Mesh_Adaptatif.
<br>
Un exemple est fourni au bas de cette section pour vous montrer comment procéder.
<br>
<br>

## ## 

# **Inclure la macros dans le Start_Print** #

<br>
    
## ##
1.Bed Mesh Adaptatif :

```
SETUP_KAMP_MESHING DISPLAY_PARAMETERS=1 LED_ENABLE=1 FUZZ_ENABLE=1
```

<br>

## ##

**Exemples de START_PRINT:**

<br>

```
[gcode_macro PRINT_START]
gcode:
    SETUP_KAMP_MESHING DISPLAY_PARAMETERS=1 LED_ENABLE=1 FUZZ_ENABLE=1 # BED MESH ADAPTATIVE
    .
    M140 S{BED_TEMP}
    M190 S{BED_TEMP}
    M109 S{EXTRUDER_TEMP}
    .
    .
    G28     
    G90     
    M117    
    G92 E0  
    G1 Z10.0 F3000  
    .
    VORON_PURGE     # PURGE ADAPTATIVE 
    .
    G1 Z1.0 F3000   
    M220 S100       
```

<br>

## ## 
<br>

Voici une explication de chacun des paramètres:
<br><br>
-**DISPLAY_PARAMETERS=1:** Ce paramètre permet d'afficher les paramètres de la fonction de maillage de lit sur l'écran de l'imprimante 3D.

-**LED_ENABLE=1:** Ce paramètre permet d'allumer une LED sur l'imprimante 3D lors de la réalisation de la fonction de maillage de lit.

-**FUZZ_ENABLE=1:** Ce paramètre permet de réaliser une fonction de "fuzzing" (approximation) pour compenser les erreurs de mesure et améliorer la précision du maillage de lit.
<br>
<br>

## ##

Il est **très important** que les **SETUP_macros** soient appelées avant la macro réelle **Voron_Purge**, sinon les valeurs par défaut sont utilisées.
<br>

Et voila vous pouvez avoir un Maillage de Lit adaptatif , plus rapide, plus précis sur Klipper.
<br>
Si vous souhaitez mettre en place dans la même idée une **Purge Adaptative** aller voir [ICI](https://github.com/Eloura74/Purge_Adaptive_Klipper)
