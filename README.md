Lecture de fichiers CSV depuis un ZIP
Description

Ce projet permet de lire automatiquement tous les fichiers CSV contenus dans un fichier ZIP sans les extraire sur le disque. Il est conçu pour traiter des fichiers encodés en cp1252 (Windows-1252), typiques des environnements Windows pour les langues occidentales. Les données sont stockées dans un dictionnaire pour un accès facile et sécurisé.

Fonctionnalités

Lecture directe des fichiers CSV à partir d’un ZIP.

Gestion de l’encodage cp1252 pour les fichiers contenant des caractères spéciaux.

Stockage des fichiers CSV sous forme de DataFrames dans un dictionnaire.

Suivi automatique des noms de fichiers CSV chargés.

Gestion des erreurs pour éviter qu’un fichier corrompu bloque le traitement.

Compatible avec un nombre illimité de fichiers CSV dans un même ZIP.

Prérequis

Python 3.x

Bibliothèque Pandas

Avantages

Sécurisé : un fichier problématique n’interrompt pas la lecture des autres.

Pratique : accès facile à tous les fichiers CSV via un dictionnaire centralisé.

Flexible : applicable à différents ensembles de données et à de multiples fichiers CSV.

Utilisation

L’utilisateur peut charger les CSV et les parcourir facilement en utilisant les noms de fichiers comme clés pour accéder aux DataFrames. Les noms de fichiers sont également conservés dans une liste pour un suivi rapide.

Conseils

Pour un suivi précis des fichiers chargés, il est recommandé de conserver à la fois le dictionnaire de DataFrames et la liste des noms de fichiers.

Évitez de créer dynamiquement des variables pour chaque CSV, car cela complique la gestion des DataFrames.
