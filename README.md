# Projet API Météo

Ce projet a pour objectif de manipuler des API et de récupérer des données en ligne. En utilisant la librairie Requests, il s'agit d'interagir avec l'API OpenWeatherMap pour récupérer et analyser les données météorologiques des 20 plus grandes villes de France.  

## Détails du projet  

Dans le notebook __decouverte-request.ipynb__, nous récupérons les informations suivantes pour chaque ville :  

    * Température actuelle  
    * Température ressentie  
    * Température minimale et maximale  
    * Pression atmosphérique  
    * Humidité  
    * Vitesse du vent  
    * Direction du vent  
    * Lever du soleil   
    * Coucher du soleil   

Les informations sont stockées dans un DataFrame pandas et exportées dans un fichier CSV. Nous créons également une base de données SQLite.  

Le notebook __coord_villes__.ipynb utilise une API de géocodage pour ajouter les colonnes de latitude et de longitude au DataFrame créé précédemment.  

Le fichier __app1.py__ contient une application Streamlit pour afficher les informations météorologiques des 20 villes. Elle permet de sélectionner une ville dans une liste déroulante et affiche les informations météorologiques pour cette ville. La page comprend également une carte de France avec des marqueurs pour chaque ville.  

Le fichier __app2.py__ contient une autre application Streamlit qui permet à l'utilisateur d'entrer le nom d'une ville et d'afficher les informations météorologiques pour cette ville. La page comprend également une carte du monde avec des marqueurs pour les 20 villes.  

## Installation

Pour exécuter ce projet, vous aurez besoin des librairies suivantes :  

    * Pandas  
    * Streamlit  
    * Folium  
    * Streamlit-folium  
    * Requests  
    * Dotenv  

Vous pouvez les installer avec la commande suivante :  

pip install pandas streamlit folium streamlit-folium requests python-dotenv  

Vous aurez également besoin d'une clé API pour accéder à l'API OpenWeatherMap. Cette clé doit être stockée dans un fichier .env à la racine du projet.

## Utilisation  

Pour exécuter l'application, exécutez la commande suivante à la racine du projet :  

streamlit run app1.py  ou   streamlit run app2.py  

Cela ouvrira l'application dans votre navigateur par défaut.  