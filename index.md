 Articles
      </div>
    </div>
    <div class="row">
      <div class="twelve wide column">
{% for post in site.posts reserved limit:3 %}
        <div class="ui segment divided items left aligned">
          <div class="item">
            <div class="content">
              <h3><a href="{{ post.url | prepend: site.baseurl }}" class="header">{{ post.title }}</a></h3>
              <div class="meta">
                <div class="cinema"><i class="fa fa-calendar"></i> {{ post.date | date: "%-d %b %Y" }} <i class="fa fa-clock-o"></i> {{ post.date | date: "%H:%M" }}</div>
              </div>
              <div class="ui horizontal divider"><i class="fa fa-github-square" style="font-size: 2em;"></i></div>
              <div class="description">
                <p>{{ post.excerpt }}</p>
              </div>
              <div class="extra">
                <a href="{{ post.url | prepend: site.baseurl }}" class="ui right floated primary button">
                  Read More <i class="fa fa-chevron-right"></i>
                </a>
                {% for tags in post.tags %}
                <div class="ui label"><i class="fa fa-tag"></i> {{ tags }}</div>
                {% endfor %}
              </div>
            </div>
          </div>
        </div>
{% endfor %}
<a class="huge ui blue button" href="#" target="_blank">See All Articles <i class="fa fa-chevron-right"></i></a>
      </div>
    </div>
  </div>
</div>
