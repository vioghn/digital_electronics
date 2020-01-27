---
layout: page
title: Lectures
permalink: /lectures/
---

Designing MOS circuits [slides] (static_files/lectures/NM-Digital1-MOS.pdf)

Traditional design of MOS circuits [slides](static_files/lectures/NM-Digital2-NMOS.pdf)

CMOS inverter [slides] (static_files/lectures/NM-Digital3-CMOS.pdf)

MOS transition gates [slides](static_files/lectures/NM-Digital4-MOS-Xgates.pdf)

MOS dynamic gate [slides] (static_files/lectures/NM-Digital5-Dynamic.pdf)

<ul id="archive">
{% for lecture in site.lectures reversed %}
<li class="archiveposturl" style="background: transparent">
<div class="lecture-container">
    {% if lecture.thumbnail %}
    <div class="thumbnail">
      <div class="center-cropped" style="margin-top:5px;margin-bottom:5px;background-image: url('{{ lecture.thumbnail | prepend: site.baseurl }}');">
        <img src="{{ lecture.thumbnail | prepend: site.baseurl }}"/>
      </div>
    </div>
    {% endif %}
    <div class="content">
        <span><a href="
            {% if lecture.slides contains '://' %}
              {{ lecture.slides }} 
            {% else %}
              {{ lecture.slides | prepend: site.baseurl }} 
            {% endif %}">{{ lecture.title }}</a>
        </span><br>

        {% if lecture.tldr %}
            <strong>tl;dr:</strong> 
            {{ lecture.tldr }}
            <br/>
        {% endif %}

        <strong>
            {% include lecture_links.html lecture=lecture %}
        </strong>
    </div>
</div>
</li>
{% endfor %}
</ul>