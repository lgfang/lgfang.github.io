---
layout: page
title: Lungang's blog
tagline: 
---
{% include JB/setup %}

{% for post in site.posts limit: 8 %}

<div class="article-delem">
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
</div>
<br/>

{% endfor %}
