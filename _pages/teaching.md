---
permalink: /teaching/
excerpt: "teaching"
title: ""
author_profile: true
layout: single
classes: wide
---
Listed below are all courses I have taught and the respective course catalog descriptions from each institution.
<br>
(*) Denotes courses that I designed.

{% for inst in site.data.teaching %}
***

<b>{{ inst.institution }}</b> ({{ inst.role }}, {{ inst.years }})

{% for course in inst.courses %}{% include course.html course=course %}
{% endfor %}
{% endfor %}
***
