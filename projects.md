---
layout: page
title: Projects
subtitle: My own protfolio of cool coding stuff
---

<div class="github-widget" data-username="Asayhi">
</div>
<script src="https://unpkg.com/github-card@1.2.1/dist/widget.js"></script>

Eine Galerie mit meinen bisherigen Erfahrungen im Programmierungsumfeld entsteht hier. Es hat keinen Anspruch auf Vollständigkeit oder dass die Projekte einen höheren Sinn oder Zweck haben. Oftmals sind es einfach Spaß-Projekte.

----

## Machine Learning und KI

- Super Mario World "KI"
Ein Studienprojekt um zu ermitteln, wie man mit Reinforcement Learning Super Mario lösen kann. Ziel des Projektes war es mittels eines zielbasierten Agenten ein Level des Spiels Super Mario World erfolgreich abzuschließen. Das Level, welches von dem Agenten abgeschlossen werden soll heißt „Yoshi`s Island 2“, da dieses eines der einfacheren Level ist. Um dies umzusetzen wurde „OpenAI Gym“ und „Gym Retro“ benutzt. Für die Verhaltensweisen der Agenten wird der evolutionary Algorithmus NEAT (NeuroEveolution of Augmenting Topologies) verwendet, um so  Unterschiede in den Generationen zu erzeugen und die am besten performenden Agenten als Basis für eine nächste Generation genommen werden.

- Autoencoders für Image Tracing Preproccessing
Um zu testen, ob sich der Einsatz eines Autoencoders zur Verbesserung von Objekterkennungsproblemen lohnen kann, wird ein Programm in einer virtuellen Umgebung implementiert, das einen Autoencoder trainiert. Der Autoencoder übergibt die reduzierte Darstellung der Grafik an einen modernen Vektorisierungsalgorithmus. Das Ergebnis wird dann in ein Rasterformat umgewandelt und mit dem Originalbild verglichen. Anhand der Differenz zwischen der ursprünglichen und der gerasterten Darstellung der vektorisierten Grafik wird ermittelt, wie erfolgreich dieses Verfahren ist. Darüber hinaus werden die Ergebnisse dieses Verfahrens mit denen einer Hauptkomponentenanalyse (PCA) und einer reinen Vektorisierung verglichen. Dieses Experiment zeigt, dass durch die Verwendung eines Autoencoders als Vorverarbeitungsprozess vor der Anwendung eines Image Tracing Algorithmus die Komplexität des Graphen reduziert werden kann, aber die Genauigkeit der Abbildung im Vergleich zu einer reinen Vektorisierung abnimmt. Im Vergleich zu den Ergebnissen einer PCA werden die Bilder jedoch mit höherer Genauigkeit und Originaltreue rekonstruiert. Daher kann diese Methode in speziellen Fällen eingesetzt werden, in denen der Schwerpunkt auf der Extraktion von Merkmalen liegt.

- Einbindung von Machine Learning-basierter KI in das blocklib-Framework
Diese Projektarbeit beschäftigt sich mit der Implementation einer Agenten-basierten State Machine für den von der OTH entwickelten "Minecraftklon" blocklib. Diese State Machine soll das Verhalten eines "Jägers" darstellen, der einer Entität hinterherjagt und diese angreift, wenn er nahe genug an ihr ist. Es wurden mehrere verschieden Ansätze für die Wegfindung getestet. Aufgrund der Schwierigkeit, eine Spielfigur in einem 3D-Raum um Hindernisse herum zu manövrieren und die größten Probleme durch unterschiedliche Elevation entstanden sind wird bei einer Vorwärtsbewegung der Figur auch gleichzeitig gesprungen. Alles in allem zeigte diese Projekt, dass mittels Machine Learning in Python die Abläufe einer Java-Anwendung gesteuert werden können.

----

## Automatisierung

- **SunBot**
SunBot ist ein Python-Skript, das die Twitter-API verwendet. Der Hauptzweck von SunBot war ein grundlegendes Verständnis dafür zu entwickeln, wie konstant laufende bzw. regelmäßig aufgerufene Programme zu handhaben sind. Außerdem trug das Projekt dazu bei sich etwas mit öffentlich zugänglichen APIs zu beschäftigen. Hierbei wird zu bestimmten Zeiten (Sonnenauf- und Sonnenuntergang geholt durch astropy) ein Tweet erstellt und dieser mit dem aktuellen Wetter versehen.

----

## Webdevelopment

- **Augmented Reality mit AR.js**
Eine Web-basierte Anwendung, die die Kamera des Gerätes auf dem die Website aufgerufen wurde verwendet. Es wird darauf gewartet, dass ein HIRO Marker von der Kamera erkannt wird. Danach werden mithilfe von THREE.js 3D Modelle von Pfeilen erzeugt, die ein Magnetfeld darstellen sollen. Je nach der vom Hauptserver berechneten Feldstärke und -form des Magnetfeldes werden unterschiedlich lange und anders gefärbte Pfeile dargestellt.

- **Cobra Race**
Ein JavaScript-basiertes Spiel, das ein rudimentärer Klon eines Endlosrunners ist. Die Spielerfigur wird durch klicken auf die jeweilige Spur gestuert. Diese Webapplikation wird mittels cordova-Wrapper in eine Andorid-App gepackt. Aus diesem Grund auch die Steuerung per Touch

----

## IT-Security

- **P2P-Botnetzerkennung mit simulierten Daten**
Diese Arbeit beschäftigt sich mit der Frage, ob sich simulierte Daten dafür eignen P2P-Erkennungsmechanismen zu verbessern. Hierfür werden zunächst bekannte P2P-Botnetze anhand der für sie typischen Parameter rekonstruiert und mittels eines Frameworks simuliert. Die so entstandenen Botnetz-Traces werden danach gefiltert und in einen Mitschnitt eines Netzwerkes injiziert. Diese Netzwerk-Capture wird dann verwendet um die P2P-Botnetzerkennungsalgorithmen zu trainieren und zu testen. Hierbei werden drei verschiedene Erkennungsmethoden (PeerRush, PeerShark, PeerDigger) verwendet. Außerdem finden drei
unterschiedliche Szenarien zur Bewertung der Erkennungsmethoden Anwendung. Dabei werden die simulierte Daten in einem Szenario für das Anlernen der Erkennungsalgorithmen verwendet. In einem anderen Szenario werden die Simulationsdaten als Input für bereits auf realen Daten trainierten Erkennungsmechanismen verwendet.
Die Auswertung zeigt, dass ein reines Verwenden von simulierten Daten für die Botnetzerkennung sich noch als schwierig darstellt, vor allem dann, wenn nur simulierte Botnet-Daten für ein Training der Erkennungsmechanismen verwendet werden. Jedoch zeigt sich auch, dass bei einer Mischung aus realen und simulierten Daten auch abgeänderte Botnetze detektiert werden könne. Daraus lässt sich folgern, dass die in Simulationen generierten Daten dazu beitragen können die Botnetzerkennung zu verbessern.
