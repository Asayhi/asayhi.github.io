---
layout: post
title: What I learned about botnets
subtitle: How we got here?
tags: [IT-Security, Botnet]
thumbnail-img: /assets/img/stock_person_bot.svg.png
comments: true
mathjax: true
author: Manuel Amesberger
---

Let's begin with a typical student story. The new winter semester started with lectures in presence after my first two semesters at the OTH in Regensburg were fully remote. I only knew a few people since they had their face cams on during Zoom lectures. And I needed to do a project to get mandatory credit points.

I overheard someone talking about a project, they were planning. Something about botnets. One thing led to another and I got myself into the (at least for me) unknown territory of IT security and botnet analysis.

To be honest it was pretty overwhelming at first. I had no idea how this stuff worked and what was important and what wasn't. But enough of my own little story and lets jump into the more interesting stuff.

---

## Here starts the interesting stuff

So what are botnets? I like to think of them as a zombie plague that is being controlled by something. In classical botnets there is a master, who gives out orders and servants (i like this term more than slave) who carry out said orders. In the project i mentioned earlier we did not work with this kind of net.  We worked with P2P Botnets. In light of the ever increasing amount of IoT devices and there rather poor security, those get targeted often. But also end user systems and servers can be afflicted. The observation of their corresponding online times can ease the classification of infected devices which in and of itself is an intriguing metric.

We analyzed online times for IP addresses of devices in multiple Botnets. We created sessions for those devices and logged the duration of sessions.

One of the more interesting findings was, that the impact of China's so-called Great Firewall was clearly visible in our data. Peers using Chinese IP addresses would have problems connecting at certain times of the day, which resulted in many small sessions instead of one long session.

Also i got to know multiple different botnets with different goals.

- DDG: a cryptocurrency mining botnet (Monero), mostly aimed at database servers.
- Hajime: IoT botnet, targeting mostly the same unsecured/badly secured IoT devices as Mirai did
- Hide 'n' Seek: IoT devices and misconfigured database servers (e.g. MongoDB), cryptocurrency mining
- Mozi: IoT, DDoS, data exfiltration
- Sality: Windows, file infector, spam, proxy, data exfiltration, DDoS

All in all a very interesting learning experience which led me down the rabbit hole of cyber security and ethical hacking. But thats a stroy for another day...
