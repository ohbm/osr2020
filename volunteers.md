---
layout: page
title: Volunteers
---

The core OSR team were elected into these roles in July 2019, as part of the [OHBM Open Science Special Interest Group](https://ossig.netlify.app/) (OS-SIG).

<br>


<table class="people">
    <tr class="people">
        <td class="people">
            <a style="display:block; color:#05323F" href="../cassandra_gould_van_praag">
            <aside>
            <header>
                <img src="../img/team/cassandra_gould_van_praag.jpg" style="height:200px; border-radius:50%;">
                <h3>Cassandra Gould van Praag</h3>
                <h4>OSR Co-chair</h4>
                <h6>Wellcome Centre for Integrative Neuroimaging, University of Oxford</h6>
                <h4>
                <a target="_blank" href="https://twitter.com/cassgvp"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://github.com/cassgvp"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                </h4>
                <br>
            </header>
            </aside>
            </a>
        </td>
        <td class="people">
            <a style="display:block; color:#05323F" href="../stephan_heunis">
            <aside>
            <header>
                <img src="../img/team/stephan_heunis.jpg" style="height:200px; border-radius:50%;">
                <h3>Stephan Heunis</h3>
                <h4>OSR Co-chair</h4>
                <h6>Eindhoven University of Technology, The Netherlands</h6>
                <h4>
                <a target="_blank" href="https://twitter.com/fmrwhy"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://github.com/jsheunis"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://jsheunis.github.io/"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                </h4>
                <br>
            </header>
            </aside>
            </a>
        </td>
    </tr>
</table>

<table class="people">
    <tr class="people">
        <td class="people">
            <a style="display:block; color:#05323F" href="../camille_maumet">
            <aside>
            <header>
                <img src="../img/team/camille_maumet.jpg" style="height:200px; border-radius:50%;">
                <h3>Camille Maumet</h3>
                <h4>OS-SIG Chair</h4>
                <h6>Inria, Univ Rennes, CNRS, Inserm</h6>
                <h4>
                <a target="_blank" href="https://twitter.com/cmaumet"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="https://github.com/cmaumet"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                <a target="_blank" href="http://camillemaumet.com/"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>
                </h4>
                <br>
            </header>
            </aside>
            </a>
        </td>
    </tr>
</table>

Together with the OSR team, the wonderfully talented and hard-working volunteers below made significant contributions to the Open Science Room. We have greatly enjoyed working with them, and proud to have them in our community.
Have a look at their contact links and bios below, and give them a virtual high-five in the OSR!

<br>


<html>

{% assign volunteers = site.volunteers %}

{% assign n_rows = volunteers.size | divided_by:2 %}
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
            {% assign img_path = site.baseurl | append: "/img/person_default.jpg" %}
            {% for file in site.static_files %}                
                {% if file.path contains names.first and file.path contains names[1] %}
                    {% assign img_path = file.path %}
                {% endif %}
            {% endfor %}

            <a style="display:block; color:#05323F" href="{{ site.baseurl }}{{person.url}}">
            <aside class="speaker-card {% if speaker.column %} {{ speaker.column }}{% endif %}">
            <header>
                <img src="{{ site.baseurl }}{{ img_path }}" style="height:200px; border-radius:50%;">

                <h3>{{ person.Name }}</h3>

                <h6>{{ person.Affiliation }}</h6>

                <h4>
                {% if person.Twitter %} <a target="_blank" href="https://twitter.com/{{ person.Twitter }}"><i class="fa fa-twitter fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a> {% endif %}
                {% if person.Github %} <a target="_blank" href="https://github.com/{{ person.Github }}"><i class="fa fa-github fa-2x" style="position: relative; top: 0px; text-indent:0px; vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>{% endif %}
                {% if person.Website %} <a target="_blank" href="{{ person.Website }}"><i class="fa fa-external-link-square fa-2x" style="position: relative; top: 0px;text-indent:0px;  vertical-align: middle; margin-left:4px; margin-right:4px;"></i></a>{% endif %}
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
