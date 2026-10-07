<h2 id="manuscripts">Manuscripts</h2>

<div class="publications">
<ol class="bibliography">


<div style="display:none">
{% for link in site.data.manuscripts.main %}
{% increment manuscript_number %}
{% endfor %}

{% increment manuscript_number %}
</div>

{% for link in site.data.manuscripts.main %}
<li>
<div class="pub-row">
  {% if link.image %} 
  <div class="publication-thumbnail">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="">
   </div>
  {% endif %}
  <div class="publication-content">
      <div class="title"> [ A{% decrement manuscript_number %} ] <a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em><em>{{ link.journal }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
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
