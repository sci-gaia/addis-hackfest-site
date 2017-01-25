---
layout: page
title: Updates
permalink: updates/
octocat: filmtocat.png
---

<div class="row"></div>
<div class="col col-sm-8">
These are the stories from the hack so far.
<ul>
{% for post in site.posts %}
<li><a href="{{site.url }}{{ post.url }}">{{post.title}}</a>
{{ post.description | strip_html }}
</li>
{% endfor %}
</ul>
</div>


<div class="col col-sm4">
<h3>Hack Board</h3>
<a href="https://waffle.io/sci-gaia/LagosHackfest"><img class="team-image"  src="{{site.url}}/images/waffle-black.png">


</div>
