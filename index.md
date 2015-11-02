---
layout: page
title: Do not stop
tagline: it does not matter how slowly you go 
---
{% include JB/setup %}

{% for post in site.posts limit: 8 %}

<a style="color:black;font-size:160%" href="{{ post.url }}"> {{ post.title }}</a>
<br/>
<small style="color:#4A4A4A"><strong>{{ post.date | date: "%B %e, %Y" }}</strong> . {{ post.categories }}</small>

{{ post.excerpt }}

<ul class="tag_box inline">
    <li><i class="icon-tags"></i></li>
    {% for tag in post.tags %}
    <li><a href="/tags.html#{{ tag }}-ref"> {{ tag }} </a></li>
    {% endfor %}
</ul>

<br/>

{% endfor %}
