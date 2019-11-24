```yaml
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site
title: 庭说
subtitle: 保持勃起的好奇心
description: 保持勃起的好奇心（Follow Your Curiosity）。
keywords: 庭说,TingTalk
author: 庭勃士
language: zh-CN
timezone: Asia/Shanghai

# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: https://tingtalk.me
root: /
permalink: :title/
permalink_defaults:
pretty_urls:
  trailing_index: false # Set to false to remove trailing index.html from permalinks

# Directory
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render:

# Writing
new_post_name: :title.md # File name of new posts
default_layout: post
titlecase: false # Transform title into titlecase
external_link:
  enable: true # Open external links in new tab
  field: site # Apply to the whole site
  exclude: ''
filename_case: 0
render_drafts: false
post_asset_folder: false
relative_link: false
future: true
highlight:
  enable: true
  line_number: false
  auto_detect: false
  tab_replace: ''

# Home page setting
# path: Root path for your blogs index page. (default = '')
# per_page: Posts displayed per page. (0 = disable pagination)
# order_by: Posts order. (Order by date descending by default)
index_generator:
  path: ''
  per_page: 10
  order_by: -updated

# Category & Tag
default_category: uncategorized
category_map:
  博客: blog
  工作: work
  教程: tutorials
  科学上网: bypass-gfw
  排版: typography
  其它: others
  人物: people 
  生活: life
  设计: design
  庭勃士: tim
  网站: website
  写作: writing
  外贸: foreign-trade
  外贸英语: foreign-trade-english
  英语: english
  英语口语: spoken-english
  英语语法: english-grammar
  英语风格: english-style-guide
  数字生活: digital-life
  中文: mandarin
  Hexo: hexo
tag_map: 
  阿里巴巴国际站: alibaba
  博客: blog
  标点符号: punctuation
  保险: personal-insurance
  毕业: graduation
  编程: programming
  电动牙刷: electric-toothbrush
  国际物流: shipping
  工作: work
  海贼王: one-piece
  佳句: nice-quote
  驾考: driving-test
  简历: resume
  健康: health
  科学上网: bypass-gfw
  培训: training
  排版: typography
  配色: colour-scheme
  品牌: brand
  人物: people
  日志: diary
  设计: design
  生活: life
  搜索引擎优化: seo
  搜索技巧: search-tips
  数字生活: digital-life
  摄影: photography
  庭勃士: tim
  庭说: tingtalk
  网站: website
  位图矢量化: image-tracing
  外贸: foreign-trade
  外贸英语: foreign-trade-english
  写作: writing
  选品: find-products
  英语: english
  英语口语: spoken-english
  英语语法: english-grammar
  英语发音: english-pronunciation
  英语风格: english-style-guide
  业务: business
  游泳: swim
  中文: mandarin
  字体: fonts
  做菜: cook
  租房: rent-an-apartment
  Apple ID: apple-id
  Blue Fish: blue-fish
  Chrome: chrome
  Dropshipping: dropshipping
  e 邮宝: epacket
  eBay: ebay
  Google: google
  Google Cloud Platform: gcp
  Hexo: hexo
  Illustrator: illustrator
  InDesign: indesign
  Inkscape: inkscape
  Markdown: markdown
  Python: python
  Photoshop: photoshop
  PDF: pdf
  PPT: ppt
  Shadowsocks: shadowsocks
  SwitchyOmega: switchyomega
  Windows: windows

# Metadata elements
## https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
meta_generator: true

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD
time_format: HH:mm:ss
## Use post's date for updated date unless set in front-matter
use_date_for_updated: true

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10
pagination_dir: page

# Include / Exclude file(s)
## include:/exclude: options only apply to the 'source/' folder
include:
exclude:
ignore:

# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
## theme: landscape
theme: next

# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: ''

# Fix issue: halfwidth quotation marks rendered to fullwidth
## Reference: https://github.com/hexojs/hexo/issues/1981#issuecomment-229309844
marked:
  smartypants: false


symbols_count_time:
  symbols: true
  time: true
  total_symbols: false
  total_time: false
  exclude_codeblock: false


search:
  path: search.xml
  field: post
  content: true
  format: html

feed:
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
  content_limit: 140
  content_limit_delim: ' '
  order_by: -date
  icon: icon.png
  autodiscovery: true

sitemap:
    path: sitemap.xml
```

