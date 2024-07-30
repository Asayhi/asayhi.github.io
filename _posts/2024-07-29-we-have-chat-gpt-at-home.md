---
layout: post
title: Ollama - We have Chat-GPT at home
subtitle: LLMs @home
tags: [IT-Fluff, Guide, KI]
thumbnail-img: /assets/img/ollama.png
comments: true
mathjax: true
author: Manuel Amesberger
---

Wie, man kann Large Language Models auf seinem eigenen kleinen Rechner von vor 5 Jahren laufen lassen? Yes, mit Ollama und ein paar anderen tollen Projekten sieht das ganze auch (fast) professionell aus!

## Primer

LLMs (Large Language Modells) sind maschinelle Lernmodelle, die auf großen Mengen an Textdaten trainiert wurden. Sie können verwendet werden, um Texte zu verstehen, zu generieren und zu transformieren. Beispiele für solche Modelle sind BERT (Bidirectional Encoder Representations from Transformers) und transformer-basierte Modell wie XLNet und RoBERTa.

LLMs zu hosten und zu trainieren birgt allerdings einige Herausforderungen.

- **Hoher Rechenbedarf**: Die Trainingsprozesse für LLMs sind computationally aufwendig und benötigen große Ressourcen.
- **Kosten**: Das Deployment eines LLMs auf einem eigenen Server kann teuer sein, insbesondere wenn ein großes Modell trainiert wird.
- **Komplexität**: Der Prozess des Selbsthostens kann komplex sein, insbesondere für Unternehmen ohne Erfahrung in Machine Learning.

### Ollama: Eine Lösung für das Selbsthosten von LLMs

Ollama ermöglicht es, bereits trainierte Large Language Modells zu laden und mit ihnen zu interagieren. Man muss kein eigenes Modell trainieren, sondern kann stattdessen die Vorteile eines etablierten LLM nutzen.

## How to: Setup Ollama

Schnappt euch als erstes einen Linuxrechner (vorzugsweise mit GPU) und (falls nicht getan) updated und upgraded zunächst eure Package-Liste damit euer Linuxrechner up to date ist. Nächster Schritt ist dann [Ollama](https://ollama.com/) herunterzuladen.

```shell
sudo apt update && sudo apt upgrade
curl -fsSL https://ollama.com/install.sh | sh
```

Dieses Script downloaded und installiert Ollama und startet den Ollama System Service. Um zu überprüfen ob alles gut gelaufen ist kann man einfach den Localhost der Linux-Maschine auf Port 11434 aufrufen. Folgendes sollte auf dieser Website zu sehen sein:

![image](../assets/img/ollama-check.png)

So, da Ollama jetzt am Laufen ist kann man doch gleich loslegen, oder? Nicht ganz, Ollama ist nur eine Art Framework und kein eigenes LLM. Ich stelle es mir gerne so vor wie Docker. Docker allein kann eigentlich nichts. Es wird erst dann richtig mächtig wenn man verschiedene Container lädt und laufen lässt. Genau so oder ähnlich verhält es sich mit Ollama.

Wir könen uns (ähnlich wie bei Docker) einfach ein LLM pullen. Ein beliebtes Modell ist z.B. llama3, welches von Meta stammt.

```shell
ollama pull  llama3
ollama run  llama3
```

Mit `ollama run` starten wir das LLM und können nach einer (mehr oder weniger) kurzen Wartezeit anfangen mit dem Chat Bot zu interagieren.

```shell
ollama run llama3
>>> Introduce yourself
Nice to meet you!

My name is LLaMA, I'm a large language model trained by a team of researcher at Meta AI. My primary function is to
understand and generate human-like text based on the input I receive.

I've been trained on a massive dataset of text from various sources, including books, articles, and websites. This
training enables me to recognize patterns, relationships, and nuances in language, allowing me to respond to
questions and engage in conversations with users like you.

I'm designed to be helpful, informative, and entertaining! I can assist with a wide range of topics, from general
knowledge and history to science, technology, and entertainment. I can also generate creative content, such as
stories, poems, or even dialogues for characters.

Feel free to ask me anything, and I'll do my best to provide a helpful and engaging response. What would you like
to talk about?

>>> Send a message (/? for help)

```

## How to: Setup Open WebUI

Nun haben wir eine LLM am laufen, aber die Art und Weise wie man mit ihm interagiert könnte noch durchaus comfortabler gestaltet werden. Hier kommte [Open WebUI](https://github.com/open-webui/open-webui) ins Spiel.
Open WebUI ist ein extensible, feature-rich und nutzerfreundliches, self-hosted WebUI, welches komplett offline betrieben werden kann. Es unterstützt verschiedene LLM-Runner, einschließlich Ollama und OpenAI-kompatible APIs. Außerdem bringt es den Look and Feel der Chat-GPT Seite.

Open WebUI kann man sehr einfach mit Docker betreiben. Hierfür reicht eigentlich folgender Befehl:

```shell
docker run -d --network=host -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

Open WebUI ist auf der IP-Adresse eueres Linuxrechners unter Port 8080 verfügbar.
Beim Aufrufen der Seite wird man mit einem Anmeldeformular begrüßt. Hier ist es so, dass der erste erstellte User automatisch als Admin eingetragen wird. Standardmäßig müssen weitere User die sich anmelden wollen erst vom Admin freigeschalten werden.

Im Administrationsbereich, der über das Menü unten rechts erreicht werden kann, kann unter Einstellungen > Verbindungen der Zugriff auf ollama bzw. die Verbindung zum Service überprüft werden.

Es gibt noch soviele andere Spielereien und Features die man mit ollama und OpenWebUI umsetzen kann. Fürs erste sollte das allerdings genügen...

## Fazit

{: .box-note}
**Notice**: Ich bin bisher noch nie sehr tief in die LLM und generative AI Thematik eingetaucht. Ich hate erst berührungen mit agentenbasierten Systemen und neuronalen Netzen für Bilderkennung/bearbeitung.

Mich persönlich hat es überrauscht, dass relative mächtige LLMs auch auf Consumer hardware von vor 5-7 Jahren einigermaßen performant betrieben werden können. Ich wäre ansonsten davon ausgegangen, dass die bloße Interaktion mit einem solchen Chat-Bot LLM zumindest eine dediziete GPU einer aktuellen Generation mit TensorCores oder ähnlichem braucht. Aber die Praxis hat mir gezeigt das auch AMD Vega 56 GPUs ausreichend sind um einen angenehmen Betrieb zu ermöglichen.

Ich für meinen Teil kann nur sagen, für die die es interessiert und sich einen Chat-Bot wünschen, ohne von den Onlinediensten (z.B. OpenAI) abhängig zu sein kann dies vielleicht eine echte Alternative sein.
