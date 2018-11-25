---
published: true
layout: post
category: Scripting
title: MsDOS - Récupérer la date courante au format YYYYMMDD
---
Il est parfois utile de récupérer la date au format YYYYMMDD, cela permet par exemple de nommer des fichier de façon à pouvoir les trier aisément. Voici le code:
```
echo off
FOR /F "TOKENS=1 DELIMS=/ " %%A IN ('DATE /T') DO SET dd=%%A
FOR /F "TOKENS=2 DELIMS=/ " %%A IN ('DATE /T') DO SET mm=%%A
FOR /F "TOKENS=3 DELIMS=/ " %%A IN ('DATE /T') DO SET yyyy=%%A
set DATE_YYYYMMDD %yyyy%%mm%%dd%
echo DATE_YYYYMMDD = %DATE_YYYYMMDD%
```
