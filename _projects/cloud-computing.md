---
layout: default
name: 'Computação em Nuvem'
picture: 'cloud-computing.jpg'
since: 2013
style: projects
description: Computação em Nuvem é um modelo que provê acesso a recursos computacionais de forma transparente e sob-demanda. O projeto Computação em Nuvem é voltado ao desenvolvimento de soluções para otimizar o desempenho de aplicações em ambientes de nuvem. Dentre os assuntos envolvidos, destaca-se gerenciamento de recursos através de técnicas de virtualização e consolidação de recursos.
---

<div class="title-projects m-5">
  <h1 class="display-4">{{ page.name }}</h1>
</div>

<div class="lead">
  <p>{{ page.description }}</p>
</div>

<div class="title-projects m-5">
	<h1 class="display-4">Artigos Publicados</h1>
</div>

<ul class="m-4" style="text-align: justify">
	{% for paper in site.papers %}
		{% if paper.projects contains 'Cloud Computing' %}
			<li>{{ paper.reference }}</li>
		{% endif %}
	{% endfor %}
</ul>

<div class="title-projects m-5">
  <h1 class="display-4">Membros</h1>
</div>

<div class="row m-4">
	{% for member in site.members %}
		{% if member.projects contains 'Cloud Computing' %}
    	<div class="col-lg-3 col-md-4 col-sm-6">
        <div class="team-member">
          <img class="mx-auto rounded-circle" src="{{ member.picture }}">
          <h4>{{ member.name }}</h4>
          <p class="text-muted">{{ member.role }}</p>
        </div>
      </div>     
		{% endif %}
	{% endfor %}
</div>
<hr>