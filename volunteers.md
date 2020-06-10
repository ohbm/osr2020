---
layout: page
title: Volunteers
---

<html>

{% assign volunteers = site.volunteers %}

{% assign n_rows = volunteers.size | divided_by:2 | minus:1 %}
<table class="people">
{% for row in (0..n_rows) %}
    <tr class="people">
    {% for col in (0..1) %}
        <td class="people">

        {% assign idx = row | times:2 | plus:col %}
        {% assign person = volunteers[idx] %}
        {% if person %}

            {% assign img_path = nil %}
            {% assign names = person.Name | downcase | split: " " %}
            {% for file in site.static_files %}                
                {% if file.path contains names.first and file.path contains names.last %}
                    {% assign img_path = file.path %}
                {% endif %}
            {% endfor %}

            <a style="display:block; color:#05323F" href="{{ site.baseurl }}{{person.url}}">
            <aside class="speaker-card {% if speaker.column %} {{ speaker.column }}{% endif %}">
            <header>
                <h3>{{ person.Name }}</h3>
                <img src="{{ site.baseurl }}{{ img_path }}" class="person">
                <h6>{{ person.Affiliation }}</h6>
                <h4>
                {% if person.Twitter %} <a href="https://twitter.com/{{ person.Twitter }}"><i class="fa fa-twitter" style="position: relative; top: -5px;text-indent:0px;  vertical-align: middle;"></i></a> {% endif %}
                {% if person.Github %} <a href="https://github.com/{{ person.Github }}"><i class="fa fa-github" style="position: relative; top: -5px; text-indent:0px;  "></i></a>{% endif %}
                {% if person.Website %} <a href="{{ person.Website }}"> <i class="ai ai-website fa-vc" style="  margin-bottom: -50px;position: relative; top: -5px;text-indent:0px;"  ></i></a>{% endif %} 
                </h4>
            </header>
            </aside>
            </a>
        {% endif %}
        </td>
    {% endfor %}
    </tr>
{% endfor %}
</table>

</html>