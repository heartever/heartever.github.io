<h2 id="selected-publications">Selected Publications <span class="section-link">(<a href="https://scholar.google.com/citations?user=9WkYf5wAAAAJ&hl=en">Full list on Google Scholar</a>)</span></h2>
<p class="publication-legend">* Corresponding authors; [ ] Equal Contributions; <span class="advised-marker" aria-hidden="true"></span> Advised by me</p>

<div class="publications">
<ol class="bibliography">

<div style="display:none">
{% for link in site.data.publications.main %}
{% if link.conference %} {% increment conference_number %}{% else %} {% increment journal_number %}{% endif %}
{% endfor %}

{% increment conference_number %}
{% increment journal_number %}
</div>

{% for link in site.data.publications.main %}
<li>
<div class="pub-row">
  {% if link.image %} 
  <div class="publication-thumbnail">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="">
   </div>
  {% endif %}
  <div class="publication-content">
      <div class="title"> [ {% if link.conference %}C{% decrement conference_number %}{% else %}J{% decrement journal_number %}{% endif %} ] <a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em><em>{{ link.journal }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.slides %} 
      <a href="{{ link.slides }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Slides</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>
