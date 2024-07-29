---
layout: post
title: Why? Botnetdetection mit simulierten Daten
subtitle: Why should I care?
tags: [IT-Security, Botnet]
comments: true
mathjax: true
author: Manuel Amesberger
---

Dieser Beitrag beschäftigt sich mit dem Thema meiner Masterarbeit. Aus (hoffentlich) verständlichen Gründen wird es an einigen Stellen verkürzt

## Why should I care?

Das Rückgrat im Arsenal von Cyberkriminellen bilden vor allem Botnets. Diese verteilten Systeme bestehen aus infizierten Geräten, wie Servers, PCs und auch IoT-Geräten. Sie können von einem Botmaster kontrolliert und so beispielsweise für Distributed-Denail-of-Service-Attacken, Phishing, Cryptomining etc. ausgenutzt werden. Dadurch können auch gezielte Angriffe auf kritische Infrastruktur durchgeführt werden.

Eine frühzeitige Erkennung von Botnetzen ist deshalb wichtig. Auch das Beispiel des Mirai Botnets, dass mit seinen DDoS-Attacken 2016 Teile des Internets lahm gelegt hat [4], zeigt, wie wichtig es ist, solche Netzwerke zu erkennen bevor sie zu solchen Größen anwachsen. Durch die steigende Anzahl an IoT-Devices, vermehren sich für P2P-Botnetze wie Hajime oder Mozi die potentiellen Hosts.

Es wurden bereits verschiedene Ansätze zur Erkennung von P2PBotnetzen vorgeschlagen. Hierbei benötigen viele dieser Algorithmen gelabelte Datensätze zum Trainieren und Testen. Sie benutzen beispielsweise statistische Auswertungen des Netzwerkverkehrs oder greifen auf maschinelles Lernen
oder Deep Learning zurück. Im Allgemeinen verbindet sie jedoch, dass sie präzisere Aussagen treffen können, wenn mehr Beispieldaten verfügbar sind.

Botnetzdaten können einerseits aus einem aktiven, überwachten Botnet erzeugt werden. Hierbei sind jedoch Menge und Qualität der Daten stark von den Entscheidungen der Botmaster und möglicherweise anderer Cybersicherheitsforscher abhängig, allerdings erhält man realistische Kommunikation. Eine sehr viel interessantere und unabhängigere Methode, um Botnetzdaten zu erzeugen, ist jedoch P2P-Botnetze zu simulieren. Durch Simulation kann eine (nahezu) beliebige
Menge an Datenverkehr generiert werden
