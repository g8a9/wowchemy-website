---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Squeeze and Learn: Compressing Long Sequences with Fourier Transformers for Gene Expression Prediction"
authors: ["Vittorio Pipoli", "Giuseppe Attanasio", "Marta Lovino", "Elisa Ficarra"]
date: 2023-03-06
doi:

# Schedule page publish date (NOT publication's date).
publishDate: 2023-03-16

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "Genes regulate fundamental processes in living cells, such as the synthesis of proteins or other functional molecules. Studying gene expression is hence crucial for both diagnostic and therapeutic purposes. State-of-the-art Deep Learning techniques such as Xpresso have proposed to predict gene expression from raw DNA sequences. However, DNA sequences challenge computational approaches because of their length, typically in the order of the thousands, and sparsity, requiring models to capture both short- and long-range dependencies. Indeed, the application of recent techniques like transformers is prohibitive with common hardware resources. This paper proposes FNetCompression, a novel gene-expression prediction method. Crucially, FNetCompression combines Convolutional encoders and memory-efficient Transformers to compress the sequence up to 95% with minimal performance tradeoff. Experiments on the Xpresso dataset show that FNetCompression outscores our baselines and the margin is statistically significant. Moreover, FNetCompression is 88% faster than a classical transformer-based architecture with minimal performance tradeoff."
# Summary. An optional shortened abstract.
summary: ""


tags: ["Gene Expression", "Fourier", "Transformers", "Computational", "Biology"]
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf:
url_code: https://github.com/vittoriopipoli/FNetCompression
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
  caption: ''
  focal_point: "Center"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
