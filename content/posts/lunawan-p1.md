---
author: "Hamo"
date: 2020-02-09
linktitle: Création du réseau LUNAWAN – Première partie - Lunawan, Késako ?
title: Création du réseau LUNAWAN – Première partie - Lunawan, Késako ?
---

LUNAWAN est le réseau, pour le moment privé, que je vais développer au fur et à mesure des posts publiés sur ce blog. Ce sera un réseau IPv6 Only sur la partie backbone et qui me servira à réaliser des tests sur un réseau un peu sympa. Ce réseau sera hébergé sur une seule machine (un petit raspberry pi 4) sur lequel je vais faire tourner des conteneurs LXC afin de simuler un réseau d’une dizaine de nœuds. Ce sera un réseau assez standard : IS-IS sur une seule aire et iBGP full mesh sur deux RS. Une fois que cette première étape sera passée, je rajouterai un overlay SRv6 afin de mieux appréhender le Segment Routing et probablement de l’EVPN afin d’étendre un L2 entre deux points du backbone.

Ce réseau s’appuiera sur de nombreux logiciels open source : LXC/LXD, Free Range Routing (FRR), Bird, VPP FD.IO, Bind et d’autres.

A terme, j’ai pour projet d’obtenir un numéro d’AS et des ressources UGA IPv6 afin de relier LUNAWAN au reste de l’internet.

Ce sera tout pour cette premier partie, la prochaine traitera de l’adressage ULA de LUNAWAN. 
