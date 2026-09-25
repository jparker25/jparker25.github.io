---
permalink: /students/
title: ""
excerpt: "Student"
author_profile: true
layout: single
classes: wide
---
If you are a student and are interested in working with me in some capacity, please contact me at my MCLA email address.

{% for g in site.data.students %}
***

<details><summary>{{ g.group }}</summary>
<ul>
{% for s in g.students %}<li>{{ s.name }} {{ s.year }}, <i>{% if s.honors %}{{ s.honors }}{% else %}{{ s.term }}{% endif %}</i>
<ul><li>{{ s.project }}</li></ul></li>
{% endfor %}</ul>
</details>
{% endfor %}
***
