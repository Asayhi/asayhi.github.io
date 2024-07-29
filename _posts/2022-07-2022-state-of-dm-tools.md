---
layout: post
title: The State of Dungeon Master Tools
tags: [TheStateOf, Programming]
comments: true
mathjax: true
author: Manuel Amesberger
---

 Das Projekt "Dungeon Master Tools" ist wahrscheinlich mein umfangreichstes, öffentliches Projekt. Die Idee entstammt eigentlich aus einer Phase in meinem Bachelorstudium, in der ich mir nicht sicher war, was ich mit dem ganzen Know-How aus den Vorlesungen anfangen sollte. Ich suchte also nach einem Problem und entschied ein Problem zu schaffen, wo eigentlich keins war, Dungeons & Dragons.

Für die, die nicht wissen was DnD ist, stellt es euch wie ein unglaublich freies Rollenspiel (RPG) vor, bei dem eigentlich der einzige beschränkende Faktor eure Fantasie ist. Obwohl es bereits mehrere Online-Services für das Verwalten, Anlegen und Spielen für alles rund um DnD gab, wollte ich selbst etwas machen um Stats zu speichern, zu würfeln, etc..

So entstand dieses Projekt. Ich begann also damit, die Logik in Python-Code zu gießen. Und hier liegt der Kern des Problems. Operationen über Datenmengen oder ähnliches in Python sind kein Problem. Was sich als die schwierigste Herausforderung für mich darstellte, war es ein GUI zu entwickeln.

Natürlich könnte man das Ganze Commandline basiert aufbauen, doch der durchschnittliche User nimmt das,  was auf der Commandline auftaucht, oftmals als schwarze Magie wahr. Also braucht es ein Interface, wo man sich durchklicken kann.

Diese Projekt hat mir gezeigt, dass tkinter, das bereits in Python enthaltene GUI package, sich gut für kleine GUI-Einsätze eignen. Allerdings hat es die Tendenz das es bei etwas anspruchsvolleren Designansprüchen sehr schnell für viel Code sorgt. Rückblickend hätte ich vermutlich mit QT-Designer oder etwas ähnlichem starten sollen.

Fazit:

GUI-Programmierung und Design liegt mir nicht, ist aber etwas was ich gerne lernen möchte um besere Anwendungen zu bauen.
