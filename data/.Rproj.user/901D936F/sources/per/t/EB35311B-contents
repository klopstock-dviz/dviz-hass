# 0. Loading packages ---------------------------------------------

library(tidyverse)
library(readxl)
library(jsonlite)

## 1. Lecture ---------------------------------------------------------

annonces_init <- fromJSON("ref_geographique_etendu.json")

## calcul ---------------------------------------------------------

annonces_init %>% 
  filter(typedetransaction == "Vente") %>% 
  group_by(ville) %>% 
  summarise(median = median(`prix_m²`,na.rm=T))

annonces_init %>% 
  filter(typedetransaction == "Vente" & ville == "bordeaux") %>% 
  summary()
