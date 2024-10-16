---
layout:       post
title:        "multilingual test"
subtitle:     ""
date:         2024-10-16 12:00:00
author:       "Whitney"
header-img:   "img/test.jpg"
header-mask:  0.3
catalog:      true
multilingual: true
tags:
    - test
---

<!-- Chinese Version -->
<div class="zh post-container">
    {% capture about_zh %}{% include posts/multilingual-test/zh.md %}{% endcapture %}
    {{ about_zh | markdownify }}
</div>

<!-- English Version -->
<div class="en post-container">
    {% capture about_en %}{% include posts/multilingual-test/en.md %}{% endcapture %}
    {{ about_en | markdownify }}
</div>