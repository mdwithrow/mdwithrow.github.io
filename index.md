---
layout: default
---

## Categories

<ul>
{% for tag in site.tags %}
  <li>
    <a href="{{ site.baseurl }}/tags/{{ tag[0] | slugify }}/">
      {{ tag[0] }}
    </a> ({{ tag[1].size }})
  </li>
{% endfor %}
</ul>

## Recent Posts

{% for post in site.posts %}
- [**{{ post.title }}**]({{ post.url | relative_url }})  
  *{{ post.date | date: "%B %d, %Y" }}*  
  {{ post.excerpt }}
{% endfor %}
