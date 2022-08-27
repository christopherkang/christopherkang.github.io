---
layout: empty
published: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Crimson+Text:ital,wght@1,600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Crimson+Text&display=swap');
</style>


<center>
<span style="font-family:Crimson Text; font-size: 30pt; text-align:center">
<strong>
<i>
“The good life is one inspired by love and guided by knowledge.” 
</i>
</strong>

<div>
<span style="font-size: 20pt"> Bertrand Russell </span>
</div>
</span> 
</center>


<center>
<div class ="image-gallery">
{% for row in site.data.books-sample %}
{% if row["Re-read?"] == "FALSE" and row["Status"] == nil %}
<div class="box">
<a href="{{row["Google Books"] }}"> <img src="{{ row["Img link"] }}" alt="test" width="128" height="200" class="img-gallery"> </a>
</div>
{% endif %}
{% endfor %}
</div>

<table  style="font-family:Crimson Text; font-size: 15pt;">
  {% for row in site.data.books-sample %}
    {% if forloop.first %}
    <tr>
      {% for pair in row limit: 5 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row limit: 4 %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
</center>