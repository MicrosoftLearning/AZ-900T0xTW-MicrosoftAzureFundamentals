---
title: 線上託管說明
permalink: index.html
layout: home
---

# 內容目錄

指向每個逐步解說的超連結。講師可以選擇將逐步解說用作示範或學生實驗室。 

## 逐步解說

{% assign wts = site.pages | where_exp:"page", "page.url contains '/Instructions/Walkthroughs'" %}
| 模組 | 逐步解說 |
| --- | --- | 
{% for activity in wts %}| {{ activity.wts.module }} | [{{ activity.wts.title }}{% if activity.wts.type %} - {{ activity.wts.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

