Etude d’un transect entre Nice et Calvi
================

## Avant-propos

Les consignes sont reprises dans ce document, ainsi que sous forme de commentaires dans les différents fichiers. Elles sont susceptibles d'évoluer. N'hésitez pas à vérifier le lien suivant afin de voir si des modifications n'y ont pas été apportées : <https://github.com/BioDataScience-Course/B05Ia_ligurian_sea>.

## Objectifs

Cette assignation individuelle vous permettra de nous démontrer que vous avez acquis les compétences suivantes :

- Réaliser des matrices de distance avec un indice de distance sélectionné judicieusement dans R

- Réaliser des dendrogrammes avec la méthode de liens la plus adéquates dans R

## Consignes

Complétez le carnet de notes `cah.Rmd`. Votre objectif est réaliser plusieurs dendrogrammes cohérents sur le jeu de données marphy.  

## Quelques informations supplémentaires

Des chercheurs ont réalisé un transect entre Nice et Calvi. Ils ont échantillonné 68 stations entre ces deux villes afin de prélever des échantillons d'organismes planctoniques et de mesurer les paramètres physico-chimiques de ces stations.

Vous pouvez donc retrouver dans le package {pastecs} le jeu de données `marphy` et `marbio`. Rappelez vous que l'aide est toujours disponibles

```{r}
library(pastecs)
?marphy
```

Cette page d'aide comprend de nombreuses informations qui peuvent vous aider. Vous avez des détails, des sources et des références sur le jeu de données. 



## Contexte

``` r
knitr::opts_chunk$set(echo = TRUE, message=FALSE, warning=FALSE)
# packages
SciViews::R
library(pastecs)
```

Des chercheurs ont réalisé un transect entre Nice et Calvi. Ils ont
décidé de 68 stations entre ces deux villes afin de prélever des
échantillons d’organismes planctoniques et de mesurer les paramètres
physico-chimiques de ces stations.

``` r
ggplot(map_data("france"), aes(long, lat, group = group)) +
  geom_polygon(fill= "white", color = "black") +
  geom_segment(
    aes(y = 43.7 , x = 7.25, yend = 42.56, xend= 8.75, color = "red"), 
    size = 1, show.legend = FALSE) +
  coord_quickmap() +
  theme_minimal() +
  labs( x = "Longitude", y = "Latitude")
```

![](README_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

## Jeux de données

Deux jeux de données sont mis à votre disposition :

  - **marphy** comprend les mesures de température, de salinité, de
    fluorescence et de densité sur les 68 stations étudiées.

<!-- end list -->

``` r
marphy <- read("marphy", package = "pastecs", lang = "fr")
```

  - **marbio** comprend le dénombrement de différents groupes au sein du
    zooplancton sur les 68 stations étudiées.

<!-- end list -->

``` r
marbio <- read("marbio", package = "pastecs", lang = "fr")
```

## Objectif à la fin des modules

### Module 5

A la fin de ce module, vous devez avoir réalisé un document R Markdown
comme un carnet de notes (Notebook) qui comprend au minimum les parties
suivantes:

  - un but qui présente l’objectif de ce carnet de notes

  - une introduction qui présente le sujet biologique de votre carnet de
    notes.

  - une section résultat

La section résultat doit comprendre la réalisation de plusieurs matrice
de distance cohérentes et des dendrogrammes sur les jeux de données
`marphy` et `marbio`.

Si nous devions résumer la procédure de traitement des données, les
étapes sont les suivantes :

  - Transformation des données si nécéssaire

  - Choix de l’indice pour la matrice de distance

  - Choix de la méthode de regroupement pour le dendrogramme

  - Choix du nombre de classe ou du niveau de coupure dans le
    dendrogramme

### Module 6

A la fin de ce module, vous devez avoir ajouté une section à votre
document R Markdown (comme un carnet de notes (Notebook)) débuté lors du
module 5.

Utilisez le regroupement des stations avec la méthode des K-moyennes.
Comparez ensuite le regroupement obtenu avec K-moyennes et avec le CAH

Utilisez le positionnement multidimensionnel sur ce projet. Comparez vos
résultats avec les analyses multivariées précédentes (k-moyennes, CAH).

Utilisez les cartes auto-adaptatives(SOM) dans ce projet. Comparez vos
résultats avec les analyses multivariées précédentes (MDS, k-moyennes,
CAH).

### Module 7

A la fin de ce module, vous devez avoir ajouté une section à votre
document R Markdown (comme un carnet de notes (Notebook)) débuté lors du
module 5 portant sur la méthode des K-moyennes.

Utilisez l’ACP et l'AFC dans ce projet. Comparez vos résultats avec les analyses
multivariées précédentes

Au cours des modules précédents, vous avez réalisé un notebook qui
comprend les différentes méthodes multivariées. Vous avez pris le temps
de critiquer et comparer les méthodes entre elles. Il est temps
d’extraire de ce notebook l’information la plus pertinente en un
rapport structuré. Créez un nouveau document au format `.Rmd` (le format
de sortie doit être en `html`).

Pour rappel, un rapport de synthèse comprend une section introduction, une section but, une section M&M, une section résultats, une section discussion, une section conclusion. Vous devez concevoir ce document comme un rapport scientifique structuré, synthétique et court. Vous ne devez y intégrer que les analyses les plus pertinentes. Vous devez limiter vos graphiques aux graphiques les plus informatifs. Chacune des méthodes ne doit pas figurer dans ce rapport de synthèse. Il faut employer les méthodes les plus pertinentes.

### Module 8

A la fin de ce module, vous devez avoir ajouté une section à votre
document R Markdown (comme un carnet de notes (Notebook)) débuté lors du
module 5 portant sur la méthode des K-moyennes.

Utilisez les indices de diversité dans ce projet.
Utilisez l'AFM dans ce projet.

Continuez à rédiger votre rapport structuré et de synthèse débuté au
cours du module 7.
