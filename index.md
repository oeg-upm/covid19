---
layout: page
title: IA & COVID-19
subtitle: Aplicando técnicas de Inteligencia Artificial sobre artículos científicos relacionados con el COVID-19
use-site-title: true
---
###English Below
### En este site queremos centralizar todos los esfuerzos que podamos realizar para aplicar técnicas de Inteligencia Artificial sobre el corpus abierto de literatura científica que se ha publicado sobre el COVID-19 (CORD-19)

Desde mediados de marzo, el Allen Institute for Artificial Intelligence mantiene un [corpus actualizado de artículos científicos sobre COVID-19](https://pages.semanticscholar.org/coronavirus-research). A 27 de marzo de 2020 este corpus contiene más de 44.000 artículos en inglés, con el texto completo de más de 29.000 artículos.

Esta ingente cantidad de literatura científica que se ha generado en apenas unos meses desde la aparición del virus demuestra la gran actividad que se ha generado desde el punto de vista científico para su estudio. Pero al mismo tiempo, es tan grande que se ha convertido en un problema para poder encontrar información específica sobre un tipo de tratamiento que se ha probado en algún grupo específico de la población, relaciones entre tratamientos, resultados obtenidos, etc. Esto es lo que normalmente se conoce como sobrecarga de información.

El 16 de marzo del 2020, la Oficina de Política Científica y Tecnológica de la Casa Blanca realizó un llamamiento a la comunidad internacional de Inteligencia Artificial para el desarrollo de técnicas de procesamiento de lenguaje natural y minería de textos que permitieran resolver [preguntas que la comunidad científica se está realizando sobre el COVID-19](https://www.whitehouse.gov/briefings-statements/call-action-tech-community-new-machine-readable-covid-19-dataset/). Muchas de estas preguntas están recogidas como [tareas en la plataforma Kaggle](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge/tasks)). 

En nuestro grupo llevamos trabajando varios años en el procesamiento de grandes corpus de textos, así que también nos hemos puesto a trabajar para intentar aportar nuestro grano de arena en la solución de estos problemas y por eso lanzamos esta [iniciativa abierta](https://oeg-upm.github.io/covid19/colabora/). 

### Nuestra pregunta: ¿es posible relacionar de algún modo principios activos, grupos terapéuticos, pruebas, tratamientos y diagnósticos que se están reportando en la literatura científica?

La pregunta con la que hemos comenzado a trabajar es esta. Queremos ser capaces de ofrecer herramientas a la comunidad científica, así como a responsables de la gestión de la epidemia, que faciliten la navegación por el corpus para poder entender mejor qué tipos de tratamientos se han probado según lo reportado en la documentación científica, y así permitir entender mejor qué combinaciones de principios activos han sido probadas, lo que podría servir, por ejemplo, para definir nuevos protocolos clínicos de tratamiento para pacientes con algunas condiciones específicas.

Los servicios que hemos construido son la base sobre la que esperamos que este tipo de preguntas se puedan resolver. Aún queda mucho trabajo por hacer, sobre todo para proporcionar unas herramientas más cercanas a los usuarios finales. Por el momento nos hemos centrado en proporcionar las herramientas que otros desarrolladores también pueden utilizar para poder partir de un corpus ya refinado y anotado con una variedad de herramientas.

### On this site we want to centralize all the efforts that we can make to apply Artificial Intelligence techniques to the open corpus of scientific literature that has been published on COVID-19 (CORD-19)

Since mid-March, the Allen Institute for Artificial Intelligence maintains an [updated corpus of scientific articles on COVID-19](https://pages.semanticscholar.org/coronavirus-research). As of March 27, 2020, this corpus contains more than 44,000 articles in English, with the full text of more than 29,000 articles.

This huge amount of scientific literature that has been generated in just a few months since the virus appeared shows the great activity that has been generated from the scientific point of view for its study. But at the same time, it is so big that it has become a problem to be able to find specific information about a type of treatment that has been tested in some specific group of the population, relationships between treatments, results obtained, etc. This is what is normally known as information overload.

On March 16, 2020, the White House Office of Scientific and Technological Policy called on the international Artificial Intelligence community to develop natural language processing techniques and text mining that would help resolve [questions that the community Scientific work on COVID-19](https://www.whitehouse.gov/briefings-statements/call-action-tech-community-new-machine-readable-covid-19-dataset/). Many of these questions are collected as [tasks on the Kaggle platform](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge/tasks)).

In our group we have been working for several years in the processing of large bodies of texts, so we have also started to work on contributing our grain of sand in solving these problems and that is why we launched this [open initiative](https://oeg-upm.github.io/covid19/colabora/).

### Our question: is it possible to relate in any way active ingredients, therapeutic groups, tests, treatments and diagnoses that are being reported in the scientific literature?

The question we have started working with is this. We want to be able to offer tools to the scientific community, as well as to those responsible for the management of the epidemic, that facilitate navigation through the corpus in order to better understand what types of treatments have been tested as reported in the scientific documentation, and thus to better understand what combinations of active ingredients have been tested, which could serve, for example, to define new clinical treatment protocols for patients with some specific conditions.

The services we have built are the foundation on which we hope that these types of questions can be resolved. Much work remains to be done, especially to provide closer tools to end users. For now we have focused on providing tools that other developers can also use to build on an already refined corpus and annotated with a variety of tools.


<!--<div class="posts-list">
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | relative_url }}">
	  <h2 class="post-title">{{ post.title }}</h2>

	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: site.date_format }}
    </p>

    <div class="post-entry-container">
      {% if post.image %}
      <div class="post-image">
        <a href="{{ post.url | relative_url }}">
          <img src="{{ post.image | relative_url }}">
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }}
        {% assign excerpt_word_count = post.excerpt | number_of_words %}
        {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
          <a href="{{ post.url | relative_url }}" class="post-read-more">[Read&nbsp;More]</a>
        {% endif %}
      </div>
    </div>

    {% if post.tags.size > 0 %}
    <div class="blog-tags">
      Tags:
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ '/tags' | relative_url }}#{{- tag -}}">{{- tag -}}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    </div>
    {% endif %}

   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | relative_url }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | relative_url }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}-->
