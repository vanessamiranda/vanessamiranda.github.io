---
layout: archive
title: "Machine Learning"
permalink: /machine/
author_profile: true
header:
   image: "/images/ML2.jpg"
---

Need to make predictions based on historical data? Or want to explore your data for certain patterns? Read more!


---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}