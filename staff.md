---
layout: page
title: Staff
description: A listing of all the course staff members.
---

# Staff

Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`.

## Faculty Sponsor

{% assign faculty_sponsors = site.staffers | where: 'role', 'Faculty Sponsor' %}
{% for staffer in faculty_sponsors %}
{{ staffer }}
{% endfor %}

{% assign facilitators = site.staffers | where: 'role', 'Facilitator' %}
{% assign num_facilitators = facilitators | size %}
{% if num_facilitators != 0 %}
## Facilitators

{% for staffer in facilitators %}
{{ staffer }}<br>
{% endfor %}
{% endif %}
