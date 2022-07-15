---
 
layout: blog
course_data: ENTC
semister_data: 5
course_code_data: 304183
unit_data: 2

#--- 
#layout: blog
#course_data: ENTC
#semister_data: 5
#course_code_data: 304181
#unit_data: 1

subtopics:
    - number: 1
      name: subtopic 1
    - number: 2
      name: subtopic 2
    - number: 3
      name: subtopic 3
---



{% for course_data in site.data.directory_structure.courses%}
    {% if course_data.name == page.course_data %} 
        {% for semister_data in course_data.semister %}
            {% if semister_data.number == page.semister_data %}
                {% for course_code_data in semister_data.subject %}
                    {% assign Subject_name = course_code_data %}
                    {% if course_code_data.code == page.course_code_data %}
                        {% for unit_data in course_code_data.units %}
                            {% assign all_units_data = course_code_data %}
                            {% if unit_data.number == page.unit_data %}
                                {% assign unit_complete_data = unit_data %}
                            {% endif %}
                        {% endfor %}
                    {% endif %}
                {% endfor %}
            {% endif %}
        {% endfor %}
    {% endif %}
{% endfor %}

<span class="sub-name"> {{ Subject_name.name }} [{{Subject_name.code}}] </span>

<span class="unit-name">Unit {{ unit_complete_data.number }} : {{unit_complete_data.name}} </span>
{% for sub_topics in page.subtopics %}
- [{{sub_topics.name}}](#{{ sub_topics.name | replace: ' ', '-' }})
{: .subtopic-reduce }
{% endfor %}

{% for units in all_units_data.units %}
{% if units.number != page.unit_data %}
<a href="{{site.url}}{{ site.baseurl }}{{site.parent_blog_dir}}/{{page.course_data}}/{{page.semister_data}}/{{page.course_code_data}}/{{page.unit_data}}/ " markdown="1" > **Unit {{units.number}}** : {{units.name}} </a>
{% endif %}
{% endfor %}

## {{page.subtopics[0].name}}
{: .mini-appendix}

- this is really a great topix. cjvbdkfjbhn xcvgbdbhdf fgdf ghdfhgfdhftgh hfdtgh fgh fh gh h h h hh h h h fhghjgfjh  fghfgh jfg gh hgf hfh 
it is awesome o like it.

- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.

## {{page.subtopics[1].name}}
{: .mini-appendix}
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
    - this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.

## {{page.subtopics[2].name}}
{: .mini-appendix}
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
    - this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.
- this is really a great topix.
it is awesome o like it.
- this is second really a great topix.
it is awesome o like it.
this is really a great topix.
it is awesome o like it.
this is second really a great topix.
it is awesome o like it.