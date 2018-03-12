---
layout: page
permalink: /orgs/
title: organizations
description: clubs and organizations that I have been affiliated with
---

{% assign sorted_orgs = (site.orgs | sort: 'date') | reverse %}
{% for org in sorted_orgs %}

<h3>{{ org.title }}</h3>
<h4>({{ org.dates-active }})</h4>
<p>
{{ org.short-desc }}
{% if org.website %}
    Learn more on their website
    <a href="{{ org.website }}"><i class="fa fa-external-link"></i></a>.
{% endif %}
</p>
<hr>

{% endfor %}
