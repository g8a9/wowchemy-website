---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Benchmarking Post-Hoc Interpretability Approaches for Transformer-based Misogyny Detection"
authors: ["Giuseppe Attanasio" ,"Debora Nozza", "Eliana Pastor", "Dirk Hovy"]
date: 2022-04-12
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2022-04-12T14:48:20+01:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "[First Workshop on Efficient Benchmarking in NLP](https://nlp-power.github.io/)"
publication_short: "First Workshop on Efficient Benchmarking in NLP at ACL 2022"

abstract: "Transformer-based Natural Language Processing models have become the standard for hate speech detection. However, the unconscious use of these techniques for such a critical task comes with negative consequences. Various works have demonstrated that hate speech classifiers are biased. 
These findings have prompted efforts to explain classifiers, mainly using attribution methods. 
In this paper, **we provide the first benchmark study of interpretability approaches for hate speech detection**. We cover four post-hoc token attribution approaches to explain the predictions of Transformer-based misogyny classifiers in English and Italian. Further, we compare generated attributions to attention analysis.  We find that only two algorithms provide faithful explanations aligned with human expectations. Gradient-based methods and attention, however, show inconsistent outputs, making their value for explanations questionable for hate speech detection tasks."

# Summary. An optional shortened abstract.
summary: ""


tags: ["Hate Speech","BERT","NLP"]
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

# Custom links (uncomment lines below)

url_pdf:
url_code: https://github.com/MilaNLProc/benchmarking-xai-misogyny
url_dataset:
url_poster: 
url_project:
url_slides: 
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: 'Examples of generated explanation'
  focal_point: "Center"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects: [integrator]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
