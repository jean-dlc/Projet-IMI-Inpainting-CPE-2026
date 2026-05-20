# Projet-IMI-Inpainting-CPE-2026
auteurs : Jean de La Chapelle, Arthus Lucic
date : 2026/05/21

Ce projet regroupe plusieurs approches algorithmiques de restauration d'images (Inpainting) pour reconstruire des zones manquantes ou détériorées à partir de masques binaires.

## Algorithmes Implémentés

### 1. Oliveira
* **Version Originale** : Implémentation classique basée sur la diffusion locale.
* **Version Optimisée en Temps** : Version accélérée pour réduire le temps de calcul mais qui ne ressemble plus à de la diffusion locale, avec des résultats moins satisfaisants.
oliveira.ipynb

### 2. Bertalmio
* Approche basée sur les équations aux dérivées partielles (EDP) pour propager les lignes d'isophotes (lignes de même intensité lumineuse) à l'intérieur de la zone à masquer.
bertalmio.ipynb

### 3. Criminisi
* **Version Non Optimisée** : Version classique à double boucle effectuant une recherche globale du meilleur patch sur l'ensemble des zones saines de l'image. 
criminisi.ipynb

* **Version Optimisée Locale** : Version accélérée restreignant la recherche du patch similaire à un voisinage local défini autour de la frontière, limitant l'explosion du temps de calcul sur les grandes résolutions. 
criminisi_local.ipynb

Il y a aussi un test d'une commande openCV d'inpainting 
test_version_opencv.ipynb

## data
* Contient les images d'entrée, les masques binaires et les résultats obtenus pour chaque algorithme.

## Résultats
* resultats de chaque algorithme dans les fichiers correspondants.


## Prérequis

```bash
pip install numpy opencv-python plotly