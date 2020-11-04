# ---
title: "TAREA_3"
author: "Fernando Bermúdez-Kuminev"
date: "3/11/2020"
output: html_document
---

```{r setup, include=FALSE}
library(leaflet)
library(tidyr)
library(dplyr)
knitr::opts_chunk$set(echo = TRUE)
```

# Mapa de Capas base

## Tres capas:

```{r echo=TRUE, message=FALSE, warning=FALSE, eval=FALSE}
mapa_1 <- leaflet() %>%
  addTiles() %>% 
  addProviderTiles(providers$OpenTopoMap, group = "Topografia") %>%
  addProviderTiles(providers$Thunderforest.OpenCycleMap, group = "Caminos") %>% 
  addProviderTiles(providers$Esri.WorldImagery, group = "Imagen satelital")  %>%  
  addLayersControl(
    baseGroups = c("Topografia", "Caminos", "Imagen satelital")
  )

mapa_1

```
