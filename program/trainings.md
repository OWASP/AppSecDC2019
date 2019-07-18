---
title: Conference Program
---
<section class="training">
<h2>Training Classes</h2>
<!--
{% for training_type in site.data.trainings %}
    <h3>{{ training_type.title }}</h3>
    <div style="overflow-x:auto;">
    <table class="tr-standard-table">
        <thead>
            <tr><th>Class</th><th>Decription</th><th>Trainer</th><th>Days</th></tr>
        </thead>
        <tbody>
        {% for class in training_type.classes %}
        <tr>
          <td>{{ class.title }}</td>
          <td>{{ class.description }}</td>
          <td>{{ class.trainer }}</td>
          <td>{{ class.days }}</td>
        </tr>
        {% endfor %}
        </tbody>
    </table>
    </div>
{% endfor %}
-->
{% for training_type in site.data.trainings %}
<h3 style="background-color: #{{ training_type.color }};">{{ training_type.title }}</h3>
<div class="tr-mobile-table" style="border-left-color: #{{ training_type.color }} !important;">
    {% for class in training_type.classes %}
    <div class="class-container">
        <div class="class-title"><a href="{{ class.url }}">{{ class.title }}</a></div>
        <div><strong>Days</strong>: {{ class.days }}</div>
        <div><strong>Instructors</strong>: {{ class.trainer }}</div>
        <div class="class-description">{{ class.description }}</div>
    </div>
    <hr>
    {% endfor %}
</div>
{% endfor %}

</section>
<!--
<a id="sched-embed" href="https://globalappsecdc2019.sched.com/">View the Global AppSec DC 2019 program.</a><script type="text/javascript" src="https://globalappsecdc2019.sched.com/js/embed.js"></script>
-->
