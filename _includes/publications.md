<style>
  .pub-row {
    display: flex;
    justify-content: space-between;
  }

  .col-sm-3.abbr {
    flex: 0 0 30%; /* Adjust the width of the image column as needed */
    margin-right: 20px;
  }

  .col-sm-9 {
    flex: 1;
  }

  .title {
    font-size: 1.5em;
    margin-bottom: 5px;
  }

  .author {
    font-style: italic;
    margin-bottom: 10px;
  }

  .periodical {
    font-style: italic;
    margin-bottom: 10px;
  }

  .description {
    text-align: justify;
    margin-bottom: 10px;
  }
</style>

<h3 id="publications" style="margin: 2px 0px -15px;">Journal Articles</h3>

<div class="publications">
  <ol class="bibliography">
    {% for link in site.data.publications.main %}
      <li>
        <div class="pub-row">
          <div class="col-sm-3 abbr">
            {% if link.image %}
              <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;">
            {% endif %}
            {% if link.image2 %}
              <img src="{{ link.image2 }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;">
            {% endif %}
          </div>
          <div class="col-sm-9">
            <div class="title"><a href="{{ link.site }}">{{ link.title }}</a></div>
            <div class="author">{{ link.authors }}</div>
            {% if link.conference %}
              <div class="periodical"><em>{{ link.conference }}</em></div>
            {% endif %}
            <div class="description">{{ link.description }}</div>
            <div class="links">
              {% if link.pdf %}
                <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px;">PDF</a>
              {% endif %}
            </div>
          </div>
        </div>
      </li>
    {% endfor %}
  </ol>
</div>
