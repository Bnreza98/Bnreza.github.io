{% for link in site.data.publications.main %}
<li>
  <div class="pub-row">
    <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
      {% if link.image1 %} 
        <img src="{{ link.image1 }}" class="teaser img-fluid z-depth-1" style="width:100%; height:40%">
      {% endif %}
      {% if link.image2 %} 
        <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width:100%; height:40%">
      {% endif %}
    </div>
    <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.site }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      {% if link.conference %} 
        <div class="periodical"><em>{{ link.conference }}</em></div>
      {% endif %}
      <div class="description">
        {{ link.description }}
      </div>
      <div class="links">
        {% if link.pdf %} 
          <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
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
