---
layout: page
permalink: /presentations/
title: Presentations
---
Selected presentations from peer-reviewed conferences (see my <a href="/cv/OzgeBakay_CV.pdf">CV</a> for the full list)
<ul>
{% assign sorted = site.presentations | sort: "year" | reverse %}
{% for p in sorted %}
	<li>
		{% for author in p.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}
		({{ p.year }}). <a href="{{ p.url }}">{{ p.title }}</a>. <i>{{ p.venue }}</i>.
		{% if p.pdf %}<a href="{{ p.pdf }}">{{ p.link_label }}</a>{% endif %}
	</li>
	<br>
{% endfor %}
</ul>
