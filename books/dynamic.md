---
layout: empty
published: true
---

<!-- <table>
  {% for row in site.data.books-sample %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table> -->

<div class ="image-gallery">
{% for row in site.data.books-sample %}
{% if row["Re-read?"] == "FALSE" and row["Status"] == nil %}
<div class="box">
<a href="{{row["Google Books"] }}"> <img src="{{ row["Img link"] }}" alt="test" width="128" height="200" class="img-gallery"> </a>
</div>
{% endif %}
{% endfor %}
</div>