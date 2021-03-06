# Fichiers de style pour QGIS

Pour charger un style dans QGIS :

1. Clic droit sur la couche.
2. Ouvrir les propriétés de la couche.
3. Se placer sur l'onglet : "Style".
4. Pour terminer : "Charger le style..." au format qml.  

**Les styles disponibles :**
- [Corine Land Cover] (http://www.statistiques.developpement-durable.gouv.fr/donnees-ligne/li/1825.html) :
  Fichiers de style créés pour QGIS 2.6 (Attention à la compatibilité)

  Pour la France métropolitaine :
    - [CLC Niveau 1] (styles/clc/clc_niveau1.qml)
    - [CLC Niveau 2] (styles/clc/clc_niveau2.qml)
    - [CLC Niveau 3] (styles/clc/clc_niveau3.qml)

  Pour les départements d'outre-mer (DOM) :
    - [CLC DOM Niveau 1] (styles/clc/clc_dom_niveau1.qml)
    - [CLC DOM Niveau 2] (styles/clc/clc_dom_niveau2.qml)
    - [CLC DOM Niveau 3] (styles/clc/clc_dom_niveau3.qml)

# Modèles pour QGIS

Voici plusieurs modèles créés à partir du modeleur graphique de QGIS

**Les modèles disponibles :**
- Indice de forme : Modèles créés pour QGIS 2.6 (Attention à la compatibilité)

  - Indice d'élongation : Rapport entre la longueur et largeur de l'entité.
  - [Indice de Gravelius] (models/Indice_gravellius.model) : Rapport du périmètre de l'entité, à celui du cercle de même superficie (Non borné, supérieur ou égale à 1).
  - [Indice de Miller] (models/Indice_miller.model) : Rapport de la superficie d'une entité, à celle d'un cercle de même périmètre (Vaut 1 si le polygone est un cercle, 0 s'il est de surface nulle).
  - Indice de Morton : Rapport de la superficie d'une entité, à celle d'un cercle de même périmètre (Vaut 1 si le polygone est un cercle, 0 s'il est de surface nulle).
  - [Indice de Solidité] (models/Indice_solidite.model): Rapport de la superficie d'une entité, à celle de son enveloppe convexe. (Vaut 1 pour un objet convexe, nettement < 1 si fortes concavités(forme complexe))
  - [Indice de Concavité] (models/Indice_concavite.model): Rapport du périmètre de l'entité, à celui de son enveloppe convexe. (Vaut 1 pour un objet convexe ou > 1 si fortes concavités (forme complexe))

En lien, avec une discussion sur [Georezo : "elongation, formes des polygones"] (http://georezo.net/forum/viewtopic.php?pid=143436#p143436)

#Scripts pour le processing de QGIS

Pour ajouter un script dans QGIS :

1. Ouvrir la boite à outils de traitement
2. Aller dans Scripts/Outils/Ajouter un script depuis le fichier

Documentation QGIS : [Créer des scripts et les exécuter depuis la boîte à outils] (http://docs.qgis.org/2.6/fr/docs/user_manual/processing/console.html)

**Les scripts disponibles :**

- Style : Testé sur QGIS 2.6 (Attention à la compatibilité)

  - [CSV R-G-B to categorized style] (scripts/CSV_R-G-B_to_categorized_style.py) : Permet de créer une symbologie catégorisée à partir de champs séparés Red, Green et Blue contenu dans un fichier CSV
  - [CSV RGB or HEX to categorized style] (scripts/CSV_RGB_or_HEX_to_categorized_style.py) : Permet de créer une symbologie catégorisée à partir d'un champ R,G,B ou hexadécimal contenu dans un fichier CSV

# Flux

**Flux WMS et WFS**

Vous trouverez [ici](flux/QGIS_WMS.xml) une liste de flux WMS et [ici](flux/QGIS_WFS.xml) une liste de flux WFS pour QGIS. N'hésitez pas à compléter ces listes.

Pour ajouter des flux dans QGIS depuis un fichier xml :

  1. Menu "Couche" / Ajouter une couche / Ajouter une couche WMS ou WFS
  2. Cliquer sur charger et sélectionner le xml
  3. Sélectionner les flux à importer
  4. Importer
