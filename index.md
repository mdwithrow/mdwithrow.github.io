---
layout: default
---

<link rel="stylesheet" href="/assets/css/style.scss">

## Categories

<ul class="horizontal-list">
{% for category in site.categories %}
  <li>
    <a href="{{ site.baseurl }}/site.categories/{{ category[0] | slugify }}/">
      {{ category[0] }}
    </a> ({{ category[1].size }})
  </li>
{% endfor %}
</ul>

## Recent Posts

{% for post in site.posts %}
- [**{{ post.title }}**]({{ post.url | relative_url }})  
  *{{ post.date | date: "%B %d, %Y" }}*  
  {{ post.excerpt }}
{% endfor %}
