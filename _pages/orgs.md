---
layout: page
permalink: /orgs/
title: organizations
description: clubs and organizations that I have been affiliated with
---

{% assign sorted_orgs = (site.orgs | sort: 'date') | reverse %}
{% for org in sorted_orgs %}

<h2>{{ org.title }}</h2>
<h3>({{ org.dates-active }})</h3>
<p>
{{ org.short-desc }}
{% if org.website %}
    Learn more on their website
    <a href="{{ org.website }}"><i class="fa fa-external-link-alt"></i></a>.
{% endif %}
</p>
<hr>

{% endfor %}
