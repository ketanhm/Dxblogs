---
layout: page
title: General Posts
permalink: /general/
---

<div class="home">

    <ul class="post-list">
        {% for post in site.categories['General'] %}
                 <li>
                    {%- if post.image - %}      
                       <img src="{{- post.image | relative_url -}}" alt="" class="blog-roll-image">
                    {%- else -%}  
                       {%- assign postImage = "/assets/images/image-default.jpg" -%}  
                       <img src="{{- postImage | relative_url -}}" alt="" class="blog-roll-image">
                    {%- endif -%}

                    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
                    <span class="post-meta">{{ post.date | date: date_format }}</span>
                    <h3> <a class="post-link" href="{{ post.url | relative_url }}"> {{ post.title | escape }} </a> </h3>
        
                    {%- if site.show_excerpts -%}
                       {{ post.excerpt }}
                    {%- endif -%}
                 </li>
        {% endfor %}
    </ul> 
</div>
