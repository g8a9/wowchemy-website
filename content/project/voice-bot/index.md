---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Voice Bot"
summary: "A Telegram bot to transcribe any voice note with speech AI models."
authors: ["Giuseppe Attanasio"]
tags: ["software"]
categories: []
date: 2023-10-04T00:10:36+02:00

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
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: "https://github.com/g8a9/speech-models-on-telegram.git"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

draft: false
---

We all receive hundreds of voice notes every year. However, listening to some of them, at particular moments and times, might violate good social norms and manners.

The main goal of Voice Bot is to transcribe Telegram voice notes using AI. The logic is simple: you receive a note you want to read in plain text and forward it to the bot to get the transcript back.

The bot is currently running at [https://telegram.me/the_whisper_bot](https://telegram.me/the_whisper_bot) -- feel free to try it!

Things I've learned along the way:
- Implementing and deploying the full stack takes half a day if you are familiar with Python and REST APIs, which is remarkably fast.
- OpenAI's Whisper is better than Meta's SeamlessM4T (ehm, no scientific evaluation here; Whisper just gives transcripts back that seem *on average* more reasonable).
- Both Whisper and SeamlessM4T are some pieces of fantastic tech.
- Both Whisper and SeamlessM4T generate noisy outputs, especially if my senders talk fast, trim spoken words, and are in a noisy environment.

### Components

- A [Beam](https://www.beam.cloud/) App to serve a serverless inference REST endpoint for speech models. Roughly, it receives a voice note's bytes and returns a transcript text.
- A Python Bot to let people send or forward voice notes and forward them in turn to the Beam App. The bot is implemented with [python-telegram-bot](https://python-telegram-bot.org/).

The app does not log, save, preprocess, or post-process any user data, except for each user's preferred language and model preference.

### Models

[SeamlessM4T](https://ai.meta.com/blog/seamless-m4t/) is a multilingual and multi-task model that translates and transcribes across speech and text.

[Whisper](https://github.com/openai/whisper) is a general-purpose speech recognition model. In this project, it is used for multilingual speech recognition and speech translation.

**Useful Links**

- SeamlessM4T Demo on HF: https://huggingface.co/spaces/facebook/seamless_m4t 
- OpenAI's Whisper Demo on Beam: https://github.com/slai-labs/get-beam/blob/main/examples/whisper-tutorial/app.py

### Limitations

- We trim voice notes to a maximum of 60 seconds for SeamlessM4T and 240 seconds for Whisper.
- The app gets suspended if not invoked for over 120 seconds. If that happens, you'll cold start it and wait ~60 seconds to get your transcript.
- This is a side project, so
    - code is not nice and tidy
    - I can't guarantee 24/7 assistance
    - I can't guarantee it'll be up forever