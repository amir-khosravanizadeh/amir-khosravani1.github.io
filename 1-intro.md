---
title: Intro
nav: true
---

<!DOCTYPE html>
<html>
  <body>
    <div class="container">

      {% assign rows = content | split:"@row" %}
      {% for row in rows %}
        <div class="row" id="row-{{ forloop.index }}">

          {% assign columns = row | split:"@column" %}
          {% for column in columns %}
            <div class="col-sm-{{ 12 | divided_by:forloop.length }}">
              {{ column }}
            </div>
          {% endfor %}

        </div>
      {% endfor %}

    </div>
  </body>
</html>
