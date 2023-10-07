---
excerpt_separator: <!--more-->
---
# it_business_analyza

začátek

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> 
      
    </li>
  {% endfor %}
</ul>

konec
