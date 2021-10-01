---
layout: default
name: 'Serverless'
picture: 'serverless.jpg'
since: 2018
style: projects
description: Serverless é um paradigma de computação que tem o objetivo de otimizar o uso de recursos computacionais através do modelo de funções como serviço, o que pode diminuir a ociosidade de recursos e reduzir o custo de operação. O projeto Serverless envolve a criação e avaliação de soluções para plataformas Serverless, com o objetivo de solucionar problemas como tempo de provisionamento e tempo de resposta.
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
		{% if paper.projects contains 'Serverless' %}
			<li>{{ paper.reference }}</li>
		{% endif %}
	{% endfor %}
</ul>

<div class="title-projects m-5">
  <h1 class="display-4">Membros</h1>
</div>

<div class="row m-4">
	{% for member in site.members %}
		{% if member.projects contains 'Serverless' %}
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