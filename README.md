## Objectif de site
L'objectif de notre application météo est de fournir une visualisation claire  des conditions météorologiques actuelles et prévues pour la région de Montpellier sur une période d'une semaine. L'application affiche des informations telles que la température maximale et minimale, l'humidité, la vitesse du vent, les précipitations, ainsi que des icônes météo représentant le code météo quotidien.

## Website
Le site internet est disponible à l'adresse suivante:[https://hamomi-majda.github.io/meteo/](https://hamomi-majda.github.io/meteo/)


## La technologie utilisée
La technologie principale que j'ai utilisée pour le développement de mon projet est le langage de programmation Python. En plus du langage lui-même, j'ai utilisé plusieurs bibliothèques et modules qui sont couramment utilisés en Python. Ces bibliothèques incluent  NumPy,Statistics et d'autres qui sont spécifiées dans le fichier 'requirements.txt'.
J'ai utilisé d'autre modules intégrés tels que Datetime, Requests qui sont utilisés pour des tâches spécifiques liées à la manipulation des données, aux requêtes HTTP et à la gestion des dates et heures. En outre, le module IPython.display est utilisé pour afficher des tables HTML dans un environnement Quarto Markdown.

## La méthodologie

Voici une méthodologie pour comprendre le fonctionnement de notre application :

Initialisation des Dates :
On définit une date de début (date_debut) deux jours avant la date actuelle et une date de fin (date_fin) six jours après la date de début. On a formaté ces dates pour les utiliser dans l'URL de l'API.

Requête à l'API :
On construit l'URL de l'API open-meteo en fonction des coordonnées de Montpellier et des dates de début et de fin. On utilise la bibliothèque requests pour récupérer les données météorologiques au format JSON à partir de cet URL.

Traitement des Données :
On extrait différentes variables météorologiques telles que l'humidité, les précipitations, la vitesse du vent, la température maximale et minimale, ainsi que le code météo quotidien.

Calcul de la Moyenne d'Humidité :
On crée un tableau bidimensionnel (tab) pour stocker les valeurs d'humidité pour chaque heure sur chaque jour. On calcule la moyenne d'humidité pour chaque jour.

Définition de Fonctions pour l'Affichage :
On définit plusieurs fonctions (date, index, iconkey, iconrain) qui sont utilisées pour formater les dates, jours de la semaine, icônes météo, et les images de précipitations.

Génération du Tableau HTML :
On utilise la bibliothèque tabulate pour générer un tableau HTML à partir des données extraites. Les données météorologiques pour chaque jour sont organisées dans un tableau avec des colonnes pour les jours, les icônes météo, les températures maximales et minimales, l'humidité, la vitesse du vent, et les précipitations.

Affichage du Tableau :
On utilise la bibliothèque IPython.display pour afficher le tableau HTML généré dans un environnement Quarto Markdown.

Intégration d'Icônes Météo :
Pour ce projet, on a intégré des icônes météo au format SVG provenant du dépôt GitHub suivant : [github.com/erikflowers/weather-icons](https://github.com/erikflowers/weather-icons). Ces icônes météo ont été utilisées pour représenter visuellement les conditions météorologiques dans l'interface ou les visualisations générées par le code. Le choix de ces icônes météo provenant de ce dépôt particulier peut ajouter une dimension visuelle attrayante et informatique au projet.