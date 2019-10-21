---
layout: page
title: Archive
permalink: /archive/
---

<div class="archive post-list">

	{% for post in site.posts %}
	  {% capture month %}{{ post.date | date: '%m%Y' }}{% endcapture %}
	  {% capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}
	    {% if month != nmonth %}
	      {% if forloop.index != 1 %}</ul>{% endif %}
	      <h3 class="sub-header">{{ post.date | date: '%B %Y' }}</h3><ul>
	    {% endif %}
	  <li><span class="time">{{ post.date | date: "%B %-d" }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}


</div>

