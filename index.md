---
layout: default
---


<style>
.horizontal-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-wrap: wrap;
}

.horizontal-list li {
    margin-right: 15px;
}
</style>

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
