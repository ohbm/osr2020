---
layout: page
title: Speakers
---

<html>

{% assign n_rows = site.speakers.size | divided_by:2 | minus:1 %}
<table style>
{% for row in (0..n_rows) %}
    <tr>
    {% for col in (0..1) %}
        <td>

        {% assign idx = row | times:2 | plus:col %}
        {% assign speaker = site.speakers[idx] %}
        {% if speaker %}
            <a style="display:block; color:#05323F" href="{{speaker.url}}">
            <aside class="speaker-card {% if speaker.column %} {{ speaker.column }}{% endif %}">
            <header>
                <h3>{{ speaker.Name }}</h3>
                <img src="/img/speakers/{{ speaker.avatarurl }}">
                <h4>
                {% if speaker.Twitter %} <a href="https://twitter.com/{{ speaker.Twitter }}"><i class="fa fa-twitter" style="position: relative; top: -5px;text-indent:0px;  vertical-align: middle;"></i></a> {% endif %}
                {% if speaker.Github %} <a href="https://github.com/{{ speaker.Github }}"><i class="fa fa-github" style="position: relative; top: -5px; text-indent:0px;  "></i></a>{% endif %}
                {% if speaker.Website %} <a href="{{ speaker.Website }}"> <i class="ai ai-website fa-vc" style="  margin-bottom: -50px;position: relative; top: -5px;text-indent:0px;"  ></i></a>{% endif %} 
                </h4>
                <h6>{{ speaker.Affiliation }}</h6>
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
