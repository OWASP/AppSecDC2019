---
title: Training Program
---
<section class="training">
<div>
<h2>Training Classes</h2>
<h4>Training subject to change based on trainer availability.</h4>
</div>
<br/>
<div class="prices">
    <table class="price-table">
        <caption>Training Prices</caption>
        <tr>
            <td>3 days:</td>
            <td> $2550.00</td>
        </tr>
        <tr>
            <td>2 days:</td><td>$1700.00</td>
        </tr>
        <tr>
            <td>1 day:</td><td>$850.00</td>
        </tr>
    </table>
</div>
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

