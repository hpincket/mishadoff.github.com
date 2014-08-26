---
layout: page
title: Categories
permalink: /categories/
header: Posts By Category
sharing: false
group: navigation
---
{% include JB/setup %}

<div>
<ul class="tag_box inline">
  {% assign categories_list = site.categories %}
  {% include JB/categories_list %}
</ul>
</div>

<div id="categories">
{% for category in site.categories %} 
  <h2 id="{{ category[0] }}-ref">{{ category[0] | join: "/" }}</h2>
  <ul>
    {% assign pages_list = category[1] %}  
    {% include JB/pages_list %}
  </ul>
{% endfor %}
</div>

