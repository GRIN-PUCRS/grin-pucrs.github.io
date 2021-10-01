---
layout: default
name: 'Computação na Borda'
picture: 'edge-computing.jpg'
since: 2017
style: projects
description: A Computação na Borda visa superar problemas como latência e instabilidade na conectividade através da provisão de recursos computacionais mais próximo dos usuários finais. O projeto Computação na borda consiste no desenvolvimento de modelagem de estratégias para melhorar a qualidade de serviço através do gerenciamento de recursos baseado em características como mobilidade dos usuários.
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
		{% if paper.projects contains 'Edge Computing' %}
			<li>{{ paper.reference }}</li>
		{% endif %}
	{% endfor %}
</ul>

<div class="title-projects m-5">
  <h1 class="display-4">Membros</h1>
</div>

<div class="row m-4">
	{% for member in site.members %}
		{% if member.projects contains 'Edge Computing' %}
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