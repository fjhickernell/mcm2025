---
title: "MCM 2025 - Program"
layout: gridlay
excerpt: "MCM 2025 -- Program."
sitemap: false
permalink: /program/
---

{% for day in (1..5) %} 
## Day {{ day }}

<table>
<colgroup>
<col width="10%" />
<col width="70%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Time</th>
<th></th>
<th>Room</th>
</tr>
</thead>
<tbody>
  {% for event in site.data.program -%}
  {% if event.day == day %}
  <tr>
  <td markdown="span"> {{ event.time }} </td> 
  <td markdown="span"> {{ event.title }} </td> 
  <td markdown="span"> {{ event.room }} </td> 
  </tr>
  {% endif %}
  {% endfor %}
</tbody>
</table>
{% endfor %}
