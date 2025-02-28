<h2 id="publications" style="margin: 2px 0px -15px;">Selected Publications</h2>

<div class="publications">
<p>Please refer to my <a href="https://scholar.google.com/citations?user=kqXYs4gAAAAJ&hl=en" target="_blank">Google Scholar page</a> for the complete list of publications.</p>

<ol class="bibliography">

{% for link in site.data.publications.main %}
<li>
  <div class="pub-row">
    <!-- Left Column: Image -->
    <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
      {% if link.image and link.image != "" %} 
      <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 120px; height: auto; max-height: 100px; object-fit: contain;">
      {% else %}
      <img src="/assets/img/default-paper.png" class="teaser img-fluid z-depth-1" style="width:100%; height:auto;"> <!-- Default placeholder -->
      {% endif %}
      {% if link.conference_short %} 
      <abbr class="badge">{{ link.conference_short }}</abbr>
      {% endif %}
    </div>
    <!-- Right Column: Publication Info -->
    <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
      <div class="title">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" target="_blank">{{ link.title }}</a>
        {% else %}
        {{ link.title }}
        {% endif %}
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <!-- Links -->
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.dataset %} 
        <a href="{{ link.dataset }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Dataset</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTeX</a>
        {% endif %}
        {% if link.notes %} 
        <strong><i style="color:#e74d3c;">{{ link.notes }}</i></strong>
        {% endif %}
      </div>
    </div>
  </div>
</li>
{% endfor %}

</ol>
</div>
