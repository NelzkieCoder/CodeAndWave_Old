---
layout: tag_layout
tagtitle: Fundamentals
tagline: Let's start with the basic
---


<h1>Posts</h1>

<link rel="icon"  type="image/png"    href="{{site.baseurl}}/assets/image/sample.jpeg">
{% for post in site.tags.Fundamentals limit:10 %}

  <ul class="post-list">
  
{% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% if current_year != previous_year %}
    {% unless forloop.first %}
      </ul>
    {% endunless %}
    <h2>{{ current_year }}</h2>
    <ul>
    {% assign previous_year = current_year %}
  {% endif %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>

  {% if forloop.last %}
    </ul>
  {% endif %}




<!-- 
   <div class="post-preview">
   <h3><a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></h3>
   <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
   {{ post.content | split:'<!--break-->' | first }}
   {% if post.content contains '<!--break-->' %}
      <a href="{{site.baseurl}}{{ post.url }}" style="font-size:10pt;">Read more...</a>
   {% endif %}
   </div>
   <hr> -->

 
  </ul>

<!-- <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ site.baseurl }}{{post.url}}">{{ post.title }}</a></li> -->

{% endfor %}


