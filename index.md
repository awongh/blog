---
layout: page
title: awongh blog
tagline: programming and stuff
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
      <span>{{ post.date | date_to_string }}</span>

      {% assign content_size = post.content.size %}

      {% if content_size  > 150 %}
        <p>{{ post.content | strip_html | truncatewords:75}}
          <a href="{{ post.url }}">Read more...</a>
        </p>
      {% else %}
        <h1>hello</h1>
        <p>{{ post.content}}</p>

      {% endif %}
    </li>
  {% endfor %}
</ul>
