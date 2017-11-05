---
layout: tag_layout
title: Android
tagtitle: Android Development
tagline: All about Android stuff
---


<h1>Posts</h1>

<link rel="icon"  type="image/png"    href="{{site.baseurl}}/assets/image/paris.jpeg">
{% for post in site.tags.Android %}

  <ul class="post-list">
        <!-- <li>
          {% assign date_format = site.cayman-blog.date_format | default: "%b %-d, %Y" %}
            <span class="post-meta">{{ post.date | date: date_format }}</span>
            <h2>
                <a class="post-link" href="{{ post.url | relative_url }}" title="{{ post.title }}">{{ post.title | escape }}</a>
            </h2>
        </li> -->


 
  </ul>

  {% for post in site.tags.Android limit:10 %}
   <div class="post-preview">
   <h3><a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></h3>
   <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
   {{ post.content | split:'<!--break-->' | first }}
   {% if post.content contains '<!--break-->' %}
      <a href="{{site.baseurl}}{{ post.url }}" style="font-size:10pt;">read more</a>
   {% endif %}
   </div>
   <hr>
{% endfor %}

<!-- <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ site.baseurl }}{{post.url}}">{{ post.title }}</a></li> -->

{% endfor %}


