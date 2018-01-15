+++
title = "Tactile Wars"
date = "2017-05-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["RapidInnovative Games", "Ankama Games"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
#  publication_types = ["0"]

# Publication name and optional abbreviated version.
# publication = "In *International Conference on Multimedia and Expo Workshops (ICMEW)*, IEEE."
# ublication_short = "WoodenWolf Studio"

abstract_short = "Tactile Wars is a strategy arcade game originally developed by Ankama Games, and was featrued by the Apple App Store in more than 150 contries. The Chinese versrion is geatly re-designed and re-enginered to support MOBA while keeping the core gameplay."

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#projects = ["example-external-project"]

# Links (optional).
# url_pdf = "http://eprints.soton.ac.uk/352095/1/Cushen-IMV2013.pdf"
# url_preprint = "http://eprints.soton.ac.uk/352095/1/Cushen-IMV2013.pdf"
# url_code = "#"
# url_dataset = "#"
# url_project = "#"
# url_slides = "#"
# url_video = "#"
# url_poster = "#"
# url_source = "#"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{name = "Chinese Ver. Official Site", url = "http://zzgc.biligame.com/yuyue/"},
              {name = "Original Ver. IOS", url = "https://itunes.apple.com/us/app/tactile-wars/id892320294?mt=8"},
              {name = "Original Ver. Android", url = "https://play.google.com/store/apps/details?id=com.ankama.tactilwar&hl=en"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "tactile_wars/bk.jpg"
#caption = "My caption :smile:"

+++
<center>
# Introduction
</center>
As the leader of a troop of pigments, draw your orders on the screen and conquer other colors.
Paint enemy camps in your hue and defend your territory during intense and colorful battles. Upgrade your army
and your base's defenses using technological advances in color.

The Chinese version (in development) is greatly re-designed and re-engineered to support MOBA while keeping the core gameplay. You can fight with other players in real-time in a 1v1 or 3v3 mode.

{{< youtube 1J1UXGz_hHo >}}

  <img src="/img/tactile_wars/1.jpg"/>
  <img src="/img/tactile_wars/2.jpg"/> 
  <img src="/img/tactile_wars/3.jpg"/>
  <img src="/img/tactile_wars/4.jpg"/>
  <img src="/img/tactile_wars/t1.png"/>
  <img src="/img/tactile_wars/t2.png"/> 
  <img src="/img/tactile_wars/t3.png"/>
  <img src="/img/tactile_wars/t4.png"/>
  <img src="/img/tactile_wars/t5.png"/>
  <img src="/img/tactile_wars/t6.png"/>
<center>
# Duties

</center>

* Designed and implemented a lockstep system to achieve multiplayer real-time PVP (Player Versus Player), including a two-layer structure to decouple the simulation loop from the rendering loop, a fixed-point math lib to make the game logic fully deterministic across all the machines and a Unity-like Coroutine.
* Developed a replay system based on the lockstep system, which could record a 5-min game battle in a tiny file (less than 10KB).
* Designed and implemented a fast and reliable networking framework with UDP and [KCP](https://github.com/skywind3000/kcp) (an automatic repeat request protocol), supporting smooth real-time PVP in a poor network connection (250ms+ delay, 100ms+ jitter) by combining with client-prediction.
* Designed and implemented a hot update system to allow updating data without re-downloading the client.
* Optimized the performance to support low-end devices to run smoothly in a game battle involving 1000+ entities.
