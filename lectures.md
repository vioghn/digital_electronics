---
layout: page
title: Lectures
permalink: /lectures/
---
<th>
<body>
  <style>
  table, td, th {
    border: 1px solid black;
  }

  table {
    border-collapse: collapse;
    width: 100%;
  }

  th {
    text-align: left;
  }
  
  </style>
  <table >
    <tr> 
    <th>orders</th>
    <th>subjects and descriptions</th>
    </tr>
    <tr>
    <th> #1</th>
    <th> Designing MOS circuits  <p> pdf slides</p> <a href= "static_files/lectures/NM-Digital1-MOS.pdf">pdf file</a>  </th>
    </tr>
    <tr>
    <th>#2 </th>
    <th> Traditional design of MOS circuits <a href = "static_files/lectures/NM-Digital2-NMOS.pdf"> pdf files</a></th>
    </tr>
    <tr>
    <th>#3 </th>
    <th> CMOS inverter <a href ="static_files/lectures/NM-Digital3-CMOS.pdf">pdf files</a></th>
    </tr>
    <tr>
    <th>#4 </th>
    <th> MOS transition gates <a href = "static_files/lectures/NM-Digital4-MOS-Xgates.pdf">pdf files</a></th>
    </tr>
    <tr>
    <th>#5<tr> 
    <th>MOS dynamic gate <a href = "static_files/lectures/NM-Digital5-Dynamic.pdf">pdf files</a> </th>
    </tr>
  </table>
  </body>
</th>









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