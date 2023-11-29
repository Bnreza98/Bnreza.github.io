<h3 id="publications" style="margin: 2px 0px -15px;">Journal Articles</h3>
<div class="publications" style="text-align: justify;">
  <ol class="bibliography">
    {% for link in site.data.publications.main %}
      <li>
        <div class="pub-row" style="display: block;">
          <div class="pub-info" style="padding-right: 15px; padding-left: 15px;">
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
          {% if link.image %} 
            <div class="image-container" style="margin-top: 15px;">
              <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%;">
            </div>
          {% endif %}
          {% if link.image2 %}
            <div class="image-container" style="margin-top: 15px;">
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%;">
            </div>
          {% endif %}
        </div>
      </li>
      <br>
    {% endfor %}
  </ol>
</div>
