-----

# MapCreator 🗺️

[](https://opensource.org/licenses/MIT)
[](https://www.google.com/search?q=https://github.com/Autodiagbin/MapCreator/issues)
[](https://www.google.com/search?q=https://github.com/Autodiagbin/MapCreator/pulls)

**MapCreator** est un logiciel open source conçu pour générer des cartes interactives et personnalisées à partir de données de transport. Visualisez facilement vos flux logistiques par localisation, transporteur et volume de produits.

*(Pensez à remplacer cette image par une capture d'écran de votre logiciel)*

## 📖 Table des matières

  - [À propos du projet](https://www.google.com/search?q=%23-%C3%A0-propos-du-projet)
  - [Fonctionnalités principales](https://www.google.com/search?q=%23-fonctionnalit%C3%A9s-principales)
  - [Technologies utilisées](https://www.google.com/search?q=%23-technologies-utilis%C3%A9es)
  - [Comment démarrer](https://www.google.com/search?q=%23-comment-d%C3%A9marrer)
      - [Prérequis](https://www.google.com/search?q=%23pr%C3%A9requis)
      - [Installation](https://www.google.com/search?q=%23installation)
  - [Utilisation](https://www.google.com/search?q=%23-utilisation)
      - [Étape 1 : Préparation des données](https://www.google.com/search?q=%23%C3%A9tape-1--pr%C3%A9paration-des-donn%C3%A9es)
      - [Étape 2 : Génération de la carte](https://www.google.com/search?q=%23%C3%A9tape-2--g%C3%A9n%C3%A9ration-de-la-carte)
  - [Contribuer](https://www.google.com/search?q=%23-contribuer)
  - [Licence](https://www.google.com/search?q=%23-licence)
  - [Contact](https://www.google.com/search?q=%23-contact)

## 📍 À propos du projet

Ce projet a pour but de fournir un outil simple et efficace pour de la logistique ou toute personne souhaitant cartographier des données de flux. Le processus se déroule en deux temps :

1.  **Préparation des données** : Une macro Excel permet de formater vos données brutes (adresses, transporteurs, volumes) en un fichier exploitable par le logiciel.
2.  **Génération de la carte** : Le logiciel utilise ce fichier pour géolocaliser les adresses et générer une carte HTML interactive, que vous pouvez filtrer et personnaliser.

## ✨ Fonctionnalités principales

  - **Détection des villes introuvables** : Le logiciel identifie et vous signale les localisations qui n'ont pas pu être géocodées.
  - **Personnalisation des couleurs** : Modifiez les couleurs des marqueurs et des tracés pour une meilleure lisibilité.
  - **Filtres dynamiques** : Filtrez les données affichées sur la carte en temps réel (par transporteur, par volume, etc.).
  - **Personnalisation de la vue** : Ajustez le zoom, le fond de carte et les informations affichées dans les pop-ups.

## 🛠️ Technologies utilisées

  - **Interface utilisateur** : [PyQt6](https://www.riverbankcomputing.com/software/pyqt/)
  - **Génération de cartes** : [Folium](https://python-visualization.github.io/folium/) (basé sur Leaflet.js)
  - **Géocodage** : [Geopy](https://geopy.readthedocs.io/en/stable/)
  - **Fond de carte** : [OpenStreetMap](https://www.openstreetmap.org/)

## 🚀 Comment démarrer

Suivez ces étapes pour installer et lancer le projet sur votre machine locale.

### Prérequis

Assurez-vous d'avoir Python et pip installés sur votre système.

  - **Python 3.x** : [python.org](https://www.python.org/downloads/)

### Installation

1.  **Clonez le dépôt Git**
    ```sh
    git clone https://github.com/Autodiagbin/MapCreator.git
    ```
2.  **Accédez au répertoire du projet**
    ```sh
    cd MapCreator
    ```
3.  **Installez les dépendances**
    (Créez un fichier `requirements.txt` s'il n'existe pas déjà avec les bibliothèques `PyQt6`, `folium`, `geopy`)
    ```sh
    pip install -r requirements.txt
    ```

## ⚙️ Utilisation

### Étape 1 : Préparation des données

Avant de lancer le logiciel, vous devez formater vos données à l'aide de la macro Excel fournie.

1.  Ouvrez le fichier `Phase1-Créerlesdonnées.xlsm` (ou nom similaire).
2.  Suivez les instructions détaillées disponibles sur cette page Notion pour importer et traiter vos données :
    > **[➡️ Guide de préparation des données sur Notion](https://tricky-olive-f4a.notion.site/269b6c1f7118803ca106fe4bf14ea769?v=269b6c1f7118805587ee000c15406210&p=269b6c1f711880beb4cae3e9586d62f6&pm=c)**
3.  Une fois la macro exécutée, un fichier de données (par exemple `donnees_pour_carte.csv`) sera généré. Conservez-le pour l'étape suivante.

### Étape 2 : Génération de la carte

1.  **Lancez l'application**

    ```sh
    python main.py 
    ```

    *(Adaptez le nom `main.py` si le fichier principal de votre application a un autre nom)*

2.  **Importez votre fichier de données** via l'interface du logiciel.

3.  **Personnalisez votre carte** à l'aide des options disponibles (couleurs, filtres, etc.).

4.  **Générez le fichier HTML** de la carte interactive.
