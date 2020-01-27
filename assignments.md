---
layout: page
title: Assignments
permalink: /assignments/
---

assignment1 [here](static_files/materials/digital-HW1-981.pdf)

assignment2 [here](static_files/materials/digital-HW2-981.pdf)

assignment3 [here](static_files/materials/digital-HW3-981.pdf)

assignment4 [here](static_files/materials/digital-HW4-981.pdf)

assignment5 [here](static_files/materials/digital-HW5-981.pdf)

<ul id="archive">
{% for asg in site.assignments reversed %}
      <li class="archiveposturl" style="background: transparent">
        <span><a href="{{ asg.url | prepend: site.baseurl}}">{{ asg.title }}</a></span>
<strong style="font-size:100%; font-family: 'Titillium Web', sans-serif; float:right">
<a title="Download problems (pdf)" href="{{ asg.pdf | prepend: site.baseurl }}"><i class="fas fa-file-pdf"></i></a> 
{% if asg.attachment %}
&nbsp; <a title="Download attachments (zip)" href="{{ asg.attachment | prepend: site.baseurl }}"><i class="fas fa-file-archive"></i></a>
{% endif %}
</strong> 
      </li>
{% endfor %}
</ul>