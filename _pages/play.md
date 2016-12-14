---
title: Play
layout: page
permalink: "/play/"
---

{% for post in site.categories.Play limit:1 %}
  <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
  <p>{{ post.content }}</p>
{% endfor %}
<hr />
<h3 class="prev_events">Previous LaPorte Service League plays:</h3>
<ul class="posts-list">
  {% for post in site.categories.Play offset:1 %}
    <li>
      <span class="post-date">{{ post.date | date: '%Y' }} -</span> 
      <strong><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></strong>
    </li>
  {% endfor %}
</ul>
{% if forloop.last == false %}<hr />{% endif %}