---
layout: default
title: Gallery
permlink: gallery/index.html
---

<h3>Create incredible motion graphics and visual effects.</h3>

<div class="gallery">
    {% assign gallery_ordered = site.gallery | sort: "order" %}
    {% for item in gallery_ordered %}
    <a class="gallery-item" href="{{ item.url | relativize_url }}">
        <div class="item-image" style="background-image: url({{ item.image | thumbnail_image: '540x360^' | relativize_url }})"></div>
        <span class="item-description">{{ item.description | markdownify }}</span>
    </a>
    {% endfor %}
</div>