<h3 id="publications" style="margin: 2px 0px -15px;">Journal Articles</h3>
<div class="publications">
  <ol class="bibliography">
    {% for link in site.data.publications.main %}
      <li>
        <div class="pub-row">
          <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
            {% if link.image %} 
              <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=200;height=50%">
            {% endif %}
            {% if link.image2 %} <!-- Add this block for the second image -->
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
            {% endif %}
          </div>
          <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
            <div class="title"><a href="{{ link.site }}">{{ link.title }}</a></div>
            <div class="author">{{ link.authors }}</div>
            {% if link.conference %} 
              <div class="periodical"><em>{{ link.conference }}</em></div>
            {% endif %}
            <div class="description">{{ link.description }}</div> <!-- Add this line for the description -->
            <div class="links">
              {% if link.pdf %} 
                <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
              {% endif %}
              <!-- ... (Other links) ... -->
            </div>
          </div>
        </div>
      </li>

<br>

{% endfor %}

</ol>
</div>
