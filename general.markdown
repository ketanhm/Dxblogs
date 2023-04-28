---
layout: page
title: General
permalink: /general/
---
Blogs on strategies and tactics of digital Information Technology Leaders and trusted Consulting Advisors. 

CIO & IT Leaders are leading the effort to digitally transform their function and make their enterprise digital at warp speed.

Trusted digital Consulting Advisor are helping IT Leaders in scaling up **Digitization**, **Cloud Transformation**, **Technology Cost Optimization**, and **Accelerate Value Realization**. 

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
