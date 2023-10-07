---
excerpt_separator: <!--more-->
---
# it_business_analyza



začátek

## články

### funkční

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>  {{ post.number }} {{ post.source }}
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

## tagy 

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href=".{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

## další

konec
