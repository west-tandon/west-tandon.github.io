---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|phdstudent|masterstudent|visiting|others|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}


<div class="pos_header">
{% if role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif role == 'phdstudent' %}
<h3>PhD Students</h3>
 {% elsif role == 'masterstudent' %}
<h3>Research Staff</h3>
 {% elsif role == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'others' %}
<h3>Honorary Members</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}
<h3>Alumni</h3>
<br>

| Who | What | Where |
| :------------- |:-------------| :-----------|
Josh Attenberg | PhD Student | Detectica
Yen-Yu Chen | PhD Student |Blippar
Maria Christoforaki | PhD Student | Yelp
Konstantinos Dimopoulos | PhD Student | Audible
Shuai Ding | PhD Student | Thumbtack
Qingqing Gan | PhD Student | Microsoft
Shoshana (Bluma) Gelley | PhD Student | American Express
Jinru He | PhD Student | Pinterest
Utku Irmak | PhD Student | Pinterest
Xiaohui Long | PhD Student | Microsoft
Xiang Liu | PhD Student | Spotify
Sergey Nepomnyachiy | PhD Student | Bloomberg
Hao Yan | PhD Student | Uber
Qi Wang | PhD Student | IBM
Jiangong Zhang | PhD Student | Amazon

{% endif %}
{% endfor %}
