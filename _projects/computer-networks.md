---
layout: default
name: 'Redes de Computadores'
picture: 'computer-networks.jpg'
since: 2013
style: projects
description: Redes de computadores constituem a base para grande parte das aplicações conhecidas atualmente, permitindo a comunicação entre múltiplos dispositivos de forma simultânea. O projeto Redes de Computadores envolve o estudo em tecnologias como redes definidas por software e funções de rede virtualizadas para otimizar o tráfego de aplicações. 
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
		{% if paper.projects contains 'Computer Networks' %}
			<li>{{ paper.reference }}</li>
		{% endif %}
	{% endfor %}
</ul>

<div class="title-projects m-5">
  <h1 class="display-4">Membros</h1>
</div>

<div class="row m-4">
	{% for member in site.members %}
		{% if member.projects contains 'Computer Networks' %}
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