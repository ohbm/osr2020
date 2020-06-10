---
layout: page
title: Speakers
---

<html>

{% assign n_rows = site.speakers.size | divided_by:2 | minus:1 %}
<table class="people">
{% for row in (0..n_rows) %}
    <tr class="people">
    {% for col in (0..1) %}
        <td class="people">

        {% assign idx = row | times:2 | plus:col %}
        {% assign speaker = site.speakers[idx] %}
        {% if speaker.Name %}

            {% assign img_path = nil %}
            {% assign names = speaker.Name | downcase | split: " " %}
            {% for file in site.static_files %}                
                {% if file.path contains names.first and file.path contains names.last %}
                    {% assign img_path = file.path %}
                {% endif %}
            {% endfor %}

            <a style="display:block; color:#05323F" href="{{ site.baseurl }}{{speaker.url}}">
            <aside class="speaker-card {% if speaker.column %} {{ speaker.column }}{% endif %}">
            <header>
                <img src="{{ site.baseurl }}{{ img_path }}" style="height:200px; border-radius:50%;">
                
                <h3>{{ speaker.Name }}</h3>
                
                <h6>{{ speaker.Affiliation }}</h6>
                
                <h4>
                {% if speaker.Twitter %} <a href="https://twitter.com/{{ speaker.Twitter }}"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle;"></i></a> {% endif %}
                {% if speaker.Github %} <a href="https://github.com/{{ speaker.Github }}"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px;  "></i></a>{% endif %}
                {% if speaker.Website %} <a href="{{ speaker.Website }}"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle;"></i></a>{% endif %}
                </h4>
                <br>
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
