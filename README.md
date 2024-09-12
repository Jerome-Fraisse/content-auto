# Projet de Génération Automatique d'Articles et d'Images

Ce projet permet de générer des articles, de mettre en évidence des éléments importants dans le texte, et de créer des images illustratives basées sur le contenu de l'article. Le projet utilise plusieurs bibliothèques Python, ainsi que l'API OpenAI pour la traduction et la génération d'éléments textuels.

## Table des Matières

- [Description](#description)
- [Pré-requis](#pré-requis)
- [Installation](#installation)
- [Configuration de l'API OpenAI](#configuration-de-lapi-openai)
- [Fonctionnalités](#fonctionnalités)
  - [Génération de plans d'articles](#génération-de-plans-darticles)
  - [Rédaction automatique d'articles](#rédaction-automatique-darticles)
  - [Mise en évidence des éléments importants](#mise-en-évidence-des-éléments-importants)
  - [Génération d'images à partir de l'article](#génération-dimages-à-partir-de-larticle)
  - [Sauvegarde en Excel et PDF](#sauvegarde-en-excel-et-pdf)
- [Exécution du projet](#exécution-du-projet)
- [Exemple d'utilisation](#exemple-dutilisation)
- [Contributions](#contributions)

## Description

Ce projet automatisé permet de :
1. Générer des plans pour des articles basés sur un mot-clé donné.
2. Rédiger des articles complets à partir des plans générés.
3. Mettre en évidence les mots ou phrases importants dans le texte.
4. Générer des images illustratives basées sur le contenu des articles.
5. Sauvegarder le contenu final dans des fichiers Excel et PDF.

Le projet utilise les modèles de langage OpenAI ainsi que plusieurs bibliothèques de traitement du langage naturel et de manipulation de données pour automatiser le processus de création de contenu.

## Pré-requis

Avant de commencer, assurez-vous que votre système dispose des éléments suivants :
- Python 3.8 ou supérieur
- Un compte OpenAI et une clé API pour accéder aux modèles GPT-3.5-turbo

### Bibliothèques Python utilisées :

Voici la liste des bibliothèques à installer pour exécuter ce projet :

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg?logo=python&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-%23000000.svg?logo=markdown&logoColor=white)

Voici les principales bibliothèques Python utilisées dans ce projet :

- ![spaCy](https://img.shields.io/badge/spaCy-3.0%2B-blue.svg?logo=spacy) : Traitement du langage naturel
- ![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4.0+-green.svg?logo=beautifulsoup) : Analyse HTML
- ![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg?logo=scikit-learn) : Extraction de caractéristiques textuelles (TF-IDF)
- ![openpyxl](https://img.shields.io/badge/openpyxl-3.0+-yellow.svg?logo=python) : Manipulation de fichiers Excel
- ![xhtml2pdf](https://img.shields.io/badge/xhtml2pdf-0.2.5+-blue.svg?logo=python) : Génération de fichiers PDF
- ![requests](https://img.shields.io/badge/Requests-2.25+-blue.svg?logo=python) : Requêtes HTTP pour générer des images
- ![OpenAI](https://img.shields.io/badge/OpenAI-API-blue.svg?logo=openai) : Utilisation des modèles OpenAI pour la génération de contenu

## Installation

### Étape 1 : Cloner le dépôt GitHub

Clonez ce dépôt sur votre machine locale en exécutant la commande suivante :


Étape 2 : Créer un environnement virtuel

Créez un environnement virtuel pour isoler les dépendances :

bash

python -m venv venv
source venv/bin/activate  # Sous Linux ou Mac
venv\Scripts\activate  # Sous Windows

Étape 3 : Installer les dépendances

Installez toutes les bibliothèques nécessaires via pip :

bash

pip install -r requirements.txt

Étape 4 : Télécharger les modèles spaCy

Téléchargez le modèle de langue français pour spaCy :

bash

python -m spacy download fr_core_news_sm

Configuration de l'API OpenAI
Étape 1 : Obtenir une clé API

Rendez-vous sur OpenAI et créez un compte si vous n'en avez pas. Ensuite, allez dans la section API pour obtenir votre clé API.
Étape 2 : Ajouter votre clé API

Créez un fichier apikey.txt à la racine du projet et ajoutez-y votre clé API OpenAI :

sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Le projet utilisera cette clé pour interagir avec l'API OpenAI.
## Fonctionnalités
Génération de plans d'articles

Le projet commence par générer un plan détaillé pour chaque mot-clé fourni. Le fichier plan_generator.py contient les instructions nécessaires pour structurer le contenu basé sur le mot-clé.
Rédaction automatique d'articles

Le fichier content_writer.py rédige un article complet en suivant le plan généré. Il exploite la puissance des modèles GPT pour générer un contenu structuré et cohérent.
Mise en évidence des éléments importants

Le fichier highlight.py met en évidence les mots et phrases clés dans le texte généré. Il utilise l'analyse TF-IDF pour identifier les bigrams et trigrams importants.
Génération d'images à partir de l'article

Le projet utilise l'API Stability AI pour générer des images basées sur le contenu de l'article. Chaque image est sauvegardée en format .webp dans un répertoire spécifique.
Sauvegarde en Excel et PDF

Le projet sauvegarde l'article final en formats Excel et PDF, avec les images générées associées. Vous pouvez retrouver cette fonctionnalité dans le fichier highlight.py.
Exécution du projet

Pour exécuter le projet, vous devez simplement fournir un ou plusieurs mots-clés, puis lancer le fichier main.py :

bash

python main.py

Le script main.py crée des sous-répertoires pour chaque mot-clé, génère le plan de l'article, rédige l'article, met en évidence les éléments importants, génère des images et sauvegarde le tout dans des fichiers Excel et PDF.
Exemple d'utilisation

Voici un exemple d'exécution du projet avec un mot-clé spécifique :

python

if __name__ == "__main__":
    keywords = ["voiture américaine de collection"]
    main(keywords)

Le projet générera un plan, un article, mettra en évidence les éléments importants et produira des images et fichiers Excel/PDF pour chaque mot-clé dans le répertoire projets.
Contributions

Les contributions sont les bienvenues ! Si vous souhaitez améliorer le projet, n'hésitez pas à soumettre des pull requests ou à signaler des problèmes dans la section issues.

