---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Hypa Watering System"
summary: ""
authors: []
tags:
- DIY
categories: []
date: 2020-07-18T12:41:39+02:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.

links:
- name: Reddit Post
  url: https://www.reddit.com/r/raspberry_pi/comments/hz2l00/i_built_a_raspberry_pienabled_watering_system_to/
  icon_pack: fab
  icon: reddit
- name: Gallery
  url: https://photos.app.goo.gl/krmFM83U2x9MB6Q28
  icon_pack: fas
  icon: image

url_code: "https://github.com/g8a9/watering-system"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Hypa is an automated watering system I have built to keep my green friends hydrated.

My PhD working activities are mainly based in Turin. However, I am from [Castrovillari](https://it.wikipedia.org/wiki/Castrovillari), a twenty-thousand people town in southern Italy, where I love to spend my holidays, close to my family. Every time, a problem arises: how do I keep my green friends hydrated?

So, I built Hypa, an automatic watering system featuring some hardware:
- an Ikea trash bin as the water reservoir;
- a cheap plastic tube with holes drilled with a hot solder;
- a single capacitive moisture sensor (yeah, I approximate the global moisture with the one from the first pot);
- a cheap [5V pump](https://www.amazon.it/gp/product/B0811SD7ZS/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- an Arduino Uno to read the analog moisture value and serialized it via USB
- a Raspberry PI 3B+ to orchestrate and expose on the web the system
- (latest extension) a USB web camera to stream and record using [motion](https://motion-project.github.io/index.html)  

The system is entirely handled through a WiFi-enabled Raspberry Pi. It runs several pieces of Python code:
- a script polls the serial USB connection to read moisture values and write them to a CSV file along with a timestamp
- another script can be run asynchronously to power the water pump for a given amount of seconds <-- **here the magic happens!**
- there is also a Dash web UI prototype to display the moisture level over time (I left that as a WIP component, as I don't always use the moisture sensor, especially when the camera is on)

Finally, The raspi is connected to a dedicated ZeroTier One private network to communicate with the Raspi remotely over SSH. Since I'm bad at remembering stuff, there is a scheduled cron job that activates
the pump every Thursday and friday night.

🪴 Back to that day, I was trying to keep alive three varieties of chili pepper: cayenne, jalapeños and habanero chocolate, plus an Orchidea and an Aphelandra (zebra plant).

Feel free to go through the [code](https://github.com/g8a9/watering-system) or the [gallery](https://photos.app.goo.gl/krmFM83U2x9MB6Q28) (I'll try to keep them udpdate with tips and suggestions).