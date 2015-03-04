---
layout: page
title: "portfolio"
date: 2015-02-22 14:28
comments: true
sharing: true
footer: true
---
<div class="portfolio-section-title">About</div>
<div class="row project">
  <div class="col-sm-3">
    <img class="img-responsive img-rounded" src="/images/avatar2.jpg" alt="Nick DelRossi">
  </div>
  <div class="col-sm-5">
    <dl>
      <dt>BIO</dt>
      <dd>
        <p>I wrote my first line of code in 1996 when I was 15 years old. 
          The language was QBASIC and I was instantly hooked. 
          I have programmed many things since then but it was in the last couple years that I developed a true passion for software and web development.
        </p>
        <p>
          My goal is to be a great programmer and I intend to reach this goal by being the hardest working guy in the room. 
          I’m really interested in writing well-tested, maintainable code and I look forward to working with other motivated developers to create great products. 
        </p>
      </dd>
      <dt>LINKS</dt>
      <dd>
        <a href="http://www.nickdelrossi.com">Development Blog</a><br>
        <a href="https://github.com/ndelrossi">GitHub Profile</a><br>
        <a href="https://www.linkedin.com/pub/nick-delrossi/7a/76/617">LinkedIn Profile</a><br>
      </dd>
    </dl>
  </div>
  <div class="col-sm-4">
    <dl>
      <dt>PRIMARY SKILLS</dt>
      <dd>
        Ruby<br>
        Ruby on Rails<br>
        RSpec + Capybara<br>
        Javascript<br>
        Backbone.js<br>
        HTML + CSS
        Git
      </dd>
      <dt>EXPERIENCE WITH</dt>
      <dd>Java, Android, Linux, OSX, Agile methodology, Server administration, Bootstrap</dd>
    </dl>
  </div>
</div>
<div class="portfolio-section-title">Projects</div>
<div class="row project">
  <div class="col-sm-5 col-sm-push-7">
    <h4>Vegan Eats Boston</h4>
    <dl>
      <dd>
        <a href="https://www.veganeatsboston.com">Website</a>,
        <a href="https://github.com/ndelrossi/vegan_eats_boston">GitHub</a>
      </dd>
      <dt>DESCRIPTION</dt>
      <dd>A website for finding vegan restaurants in the Boston area.</dd>
      <dt>STATUS</dt>
      <dd class="text-success">Released</dd>
      <dt>ROLE</dt>
      <dd>Full Stack</dd>
      <dt>TECHNOLOGY</dt>
      <dd>Ruby on Rails, Bootstrap</dd>
      <dt>NOTES</dt>
      <dd>Traditional Ruby on Rails website. Connects with Google Maps API. Admin CMS for posts/reviews/places.</dd>
      <dt>CODE SAMPLES</dt>
      <dd>Integration Tests: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/spec/features/visitor_searches_places_spec.rb">Visitor Searches Places</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/spec/features/admin_manages_posts_spec.rb">Admin Manages Posts</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/spec/features/user_updates_profile_spec.rb">User Updates Profile</a> 
      </dd>
      <dd>Unit Tests: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/spec/models/place_spec.rb">Places</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/spec/models/user_spec.rb">Users</a>
      </dd>
      <dd>Controllers: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/controllers/users_controller.rb">Users Controller</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/controllers/reviews_controller.rb">Reviews Controller</a>
      </dd>
      <dd>Custom Controllers for Admin Actions: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/controllers/admins_controller.rb">Parent Admin Controller</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/controllers/admin/places_controller.rb">Subclassed Places Admin Controller</a>
      </dd>
      <dd>Active Record Models: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/models/place.rb">Place</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/models/user.rb">User</a>
      </dd>
      <dd>Non Active Record Models Encapsulating View Logic: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/models/homepage.rb">Homepage</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/models/admin_dashboard.rb">Admin Dashboard</a>
      </dd>
      <dd>Views: 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/views/places/_filters.html.erb">Filters Partial</a>, 
        <a href="https://github.com/ndelrossi/vegan_eats_boston/blob/master/app/views/static_pages/home.html.erb">Homepage</a>
      </dd>
    </dl>
  </div>
  <div class="col-sm-7 col-sm-pull-5">
    <img class="img-responsive" src="/images/vegan_eats_boston1.png" alt="Vegan Eats Boston">
  </div>
</div>
<div class="row project">
  <div class="col-sm-5 col-sm-push-7">
    <h4>Commitwith</h4>
    <dl>
      <dd>
        <a href="http://www.commitwith.com">Website</a>,
        <a href="https://github.com/ndelrossi/commitwith">GitHub</a>
      </dd>
      <dt>DESCRIPTION</dt>
      <dd>A webapp that helps developers find open-source projects.</dd>
      <dt>STATUS</dt>
      <dd class="text-danger">Early Development</dd>
      <dt>ROLE</dt>
      <dd>Full Stack</dd>
      <dt>TECHNOLOGY</dt>
      <dd>backbone.js, Ruby on Rails, Bootstrap</dd>
      <dt>NOTES</dt>
      <dd>Single Page App with backbone.js as the front-end and Ruby on Rails as a back-end API. Connects with Github API. Uses background cronjobs to update project data.</dd>
      <dt>CODE SAMPLES</dt>
      <dd>Integration Tests: 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/spec/features/visitor_adds_project_spec.rb">Visitor Adds Project</a>, 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/spec/features/visitor_filters_projects_spec.rb">Visitor Filters Projects</a> 
      </dd>
      <dd>Rails Controller: 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/app/controllers/projects_controller.rb">Places</a>
      </dd>
      <dd>Rails Model: 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/app/models/project.rb">Place</a>
      </dd>
      <dd>Backbone Views: 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/app/assets/javascripts/views/projects.js">Projects</a>, 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/app/assets/javascripts/views/alerts.js">Alerts</a> 
      </dd>
      <dd>Backbone Collection: 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/app/assets/javascripts/collections/projects.js">Places</a>
      </dd>
      <dd>Backbone Model: 
        <a href="https://github.com/ndelrossi/commitwith/blob/master/app/assets/javascripts/models/project.js">Place</a>
      </dd>
    </dl>
  </div>
  <div class="col-sm-7 col-sm-pull-5">
    <img class="img-responsive" src="/images/commitwith1.png" alt="Commitwith">
  </div>
</div>
