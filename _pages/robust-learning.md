---
layout: single
title: Robust Learning
permalink: /robust-learning/
excerpt: Robust Learning teams at Solarillion Foundation.
---
<div style="margin-top: 2rem;">
<h2>What is Robust Learning?</h2>
<p>There are two broad sub-categories that our teams are divided into in Robust Learning
<p>
The <b>Adversarial Attacks</b> team works on making Deep Learning models robust to adversarial attacks. They previously worked on defending against physically plausible adversarial patch attacks.
</p>
<p>
The <b>Federated Learning</b> team trains models across different data sites holding local data samples, and makes their models gain experience from various datasets without sharing the training data.
</p>
<h2>Publications</h2>
{% for year in (2000..2100) reversed %}
{% assign y = year | downcase %}
{% assign current = site.data.publications | where: "year", y | where_exp: "item", "item.team contains 'RL'" %}
{% if current.size > 0 %}
<h3>{{ y }}</h3>
{% for publication_id in current %}
    {% include publication.html publication=publication_id %}
{% endfor %}
{% endif %}
{% endfor %}
</div>