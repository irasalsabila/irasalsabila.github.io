<h2 id="publications" style="margin: 2px 0px -15px;">Selected Publications</h2>

<div class="publications">
<p>Please refer to my <a href="https://scholar.google.com/citations?user=kqXYs4gAAAAJ&hl=en">Google Scholar page</a> for the complete publications.</p>


<ol class="bibliography">

{% for link in site.data.publications.main %}
<li>
  <div class="pub-row">
    <div class="col-sm-3 abbr">
      {% if link.image and link.image != "" %} 
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1">
      {% else %}
      <img src="/assets/img/default-paper.png" class="teaser img-fluid z-depth-1"> <!-- Default placeholder -->
      {% endif %}
      {% if link.conference_short %} 
      <abbr class="badge">{{ link.conference_short }}</abbr>
      {% endif %}
    </div>
    <div class="col-sm-9">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Code</a>
        {% endif %}
        {% if link.dataset %} 
        <a href="{{ link.dataset }}" class="btn btn-sm z-depth-0" role="button" target="_blank">Dataset</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank">BibTeX</a>
        {% endif %}
        {% if link.notes %} 
        <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
      </div>
    </div>
  </div>
</li>
{% endfor %}


</ol>
</div>
