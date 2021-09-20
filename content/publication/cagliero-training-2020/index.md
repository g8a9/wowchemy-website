---
# Documentation: https://wowchemy.com/docs/managing-content/

title: Training ensembles of faceted classification models for quantitative stock
  trading
subtitle: ''
summary: ''
authors:
- Luca Cagliero
- Paolo Garza
- Giuseppe Attanasio
- Elena Baralis
tags: []
categories: []
date: '2020-01-01'
lastmod: 2021-08-16T15:44:19+02:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2021-08-16T13:44:18.737337Z'
publication_types:
- '2'
abstract: Forecasting the stock markets is among the most popular research challenges
  in finance. Several quantitative trading systems based on supervised machine learning
  approaches have been presented in literature. Recently proposed solutions train
  classification models on historical stock-related datasets. Training data include
  a variety of features related to different facets (e.g., stock price trends, exchange
  volumes, price volatility, news and public mood). To increase the accuracy of the
  predictions, multiple models are often combined together using ensemble methods.
  However, understanding which models should be combined together and how to effectively
  handle features related to different facets within different models are still open
  research questions. In this paper we investigate the use of ensemble methods to
  combine faceted classification models for supporting stock trading. To this aim,
  separate classification models are trained on each subset of features belonging
  to the same facet. They produce trading signals tailored to a specific facet. Signals
  are then combined together and filtered to generate a unified, multi-faceted recommendation.
  The experimental validation, performed on different markets and in different conditions,
  shows that, in many cases, some of the faceted models perform as good as or better
  than models trained on a mix of different features. An ensemble of the faceted recommendations
  makes the generated trading signals more profitable yet robust to draw-down periods.
publication: '*Computing*'
url_pdf: https://iris.polito.it/retrieve/handle/11583/2782915/516991/postprint_noneditorial_version.pdf
doi: 10.1007/s00607-019-00776-7
---
