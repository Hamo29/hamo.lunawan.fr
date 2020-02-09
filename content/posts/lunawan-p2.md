---
author: "Hamo"
date: 2020-02-09
linktitle: Création du réseau LUNAWAN – Deuxième partie – L’adressage ULA
title: Création du réseau LUNAWAN – Deuxième partie – L’adressage ULA
---

On va utiliser des adresses IPv6 ULA (RFC 4193) pour constituer notre réseau. Les adresses ULA du range fc00::/7 sont des adresses non routées sur internet. Elles ressemblent donc aux adresses IPs privées IPv4 (RFC 1918) mais elles ont un avantage de taille : au vu de l’espace d’adressage permis par le range fd00::/8 (qui est le range utilisé à l’heure actuelle pour les adresses ULA, tiré du range fc00::/7), nous avons des chances d’avoir un préfixe en /48 globalement unique.

Pour tirer son préfixe /48 depuis le fd00::/8, nous allons utiliser le site https://cd34.com/rfc4193/ qui applique les recommandations de l’IETF. Ces recommandations sont sous la forme d’un algorithme.

Dans les grandes lignes :
* On récupère l’heure actuelle au format NTP 64 bits.
* On récupère l’adresse mac d’une de ses interfaces réseaux.
* On concatène l’heure de la journée avec l’adresse mac afin de créer une clé.
* On calcule un condensat SHA-1 sur cette clé.
* On utilise les 40 bits les moins significatifs comme identifiant global.

Pour ma part j’ai obtenu le préfixe ULA fd49:fcca:b672::/48 pour le réseau LUNAWAN

La prochaine partie traitera de la topologie du réseau de LUNAWAN.
