---
layout: page
title: Tags
permalink: /tags/
---

{%- for tag in site.tags -%}
  <a style="font-size: {{ tag | last | size  |  times: 40 | plus: 60  }}%">{{ tag[0] | append: " "}}</a>
{%- endfor -%}

<br/>

---

{% for tag in site.tags %}
  <h3 style="font-size: {{ tag | last | size  |  times: 15 | plus: 80  }}%" id={{tag[0]}}>{{ tag[0] }} ({{ tag[1] | size }} posts)</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

---