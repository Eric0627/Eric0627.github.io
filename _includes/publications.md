<h2 id="publications" class="publications-heading">Selected Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="publication-thumbnail abbr">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser" alt="" width="270" height="123" loading="lazy" decoding="async">
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="publication-details">
      <div class="title"><a href="{{ link.paper }}" target="_blank" rel="noopener">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.paper %} 
      <a href="{{ link.paper }}" class="btn" target="_blank" rel="noopener">Paper</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn" target="_blank" rel="noopener">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn" target="_blank" rel="noopener">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn" target="_blank" rel="noopener">BibTeX</a>
      {% endif %}
      {% if link.notes %} 
      <strong class="publication-note"><i>{{ link.notes }}</i></strong>
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
