# Étude d’un transect entre Nice et Calvi

## Avant-propos

Les consignes sont reprises dans ce document, ainsi que sous forme de commentaires dans les différents fichiers. Elles sont susceptibles d'évoluer. N'hésitez pas à vérifier le lien suivant afin de voir si des modifications n'y ont pas été apportées : <https://github.com/BioDataScience-Course/B05Ia_ligurian_sea>.

Soyez également bien attentif à la date limite imposée pour finir votre travail dans les temps et vérifiez bien si vous pouvez "kniter" (compiler) votre rapport final sans erreurs avant soumission finale.

## Objectifs

Ce projet GitHub Classroom individuel vous permettra de démontrer que vous avez acquis les compétences suivantes :

- Calculer des matrices de distance avec un indice de distance sélectionné judicieusement dans R

- Réaliser des dendrogrammes avec la méthode de liens la plus adéquates dans R

## Consignes

Complétez le document `docs/marphy.Rmd`. Votre objectif est de réaliser plusieurs dendrogrammes cohérents sur le jeu de données `marphy`. Ce projet est court et cadré. Vous devez le terminer à la fin de ce module 5.

## Quelques informations supplémentaires

Des chercheurs ont réalisé un transect entre Nice et Calvi. Ils ont échantillonné 68 stations entre ces deux villes afin de prélever des échantillons d'organismes planctoniques et de mesurer les paramètres physico-chimiques de l'eau au niveau de ces stations.

Vous pouvez donc retrouver dans le package {pastecs} le jeu de données `marphy` (ainsi que `marbio` qui lui est associé). Pour plus d'information, faites :

```
library(pastecs)
?marphy
```

La page d'aide comprend de nombreuses informations qui peuvent vous aider. Vous avez des détails, des sources et des références sur le jeu de données.
