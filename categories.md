---
layout: page
title: Categories
permalink: /categories/
---

# Categories

{% for category in site.categories %}
  <h2 id="{{ category[0] | slugize }}">{{ category[0] | capitalize }}</h2>
  <ul>
    {% for post in category[1] %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
