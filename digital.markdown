---
layout: page
title: Digital
permalink: /digital/
---
Digital disruption is reshaping entire industries globally. Enterprises need to be agile, innovate by using emerging technologies to grow and be efficient. 

Industry leaders are able to create sticky digital **EXPERIENCES**, powered by **DATA**, and running on optimized **PLATFORMS**.

<div class="home">

    <ul class="post-list">
        {% for post in site.categories['Digital'] %}
                 <li>
                    {%- if post.image - %}      
                       <img src="{{- post.image | relative_url -}}" alt="" class="blog-roll-image">
                    {%- else -%}  
                       {%- assign postImage = "/assets/images/image-default.jpg" -%}  
                       <img src="{{- postImage | relative_url -}}" alt="" class="blog-roll-image">
                    {%- endif -%}
                    
                    {%- assign postImage1 = "/assets/images/image-default1.jpg" -%}  
                     <img src="{{- postImage1 | relative_url -}}" alt="" class="blog-roll-image1">

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