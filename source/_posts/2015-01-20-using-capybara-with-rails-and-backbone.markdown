---
layout: post
title: "Using Capybara with Rails and Backbone"
date: 2015-01-20 13:45:22 -0500
comments: true
categories: [Ruby On Rails, Backbone, Capybara]
---
This is a quick Rails 4 guide for setting up Capybara to work the backbone-on-rails gem. If you are loading all of your html in backbone views and not from Rails then Capybara will not see it with a test like this:

{% codeblock lang:ruby %}
feature "Visitor visits home page" do
  scenario "vistor visits home page and sees title" do
    visit root_path

    expect(page).to have_content("Foo")
  end
end
{% endcodeblock %}

This will result in:

<span style="color:red">Failure/Error: expect(page).to have content("Foo")<br> 
&nbsp;&nbsp;expected to find text "Foo" in ""</span>

We can get this to work by doing a few simple things:

<!--more-->

First add the capybara-webkit gem to your Gemfile and `bundle install`. You can also use selenium-webdriver but I won't get into that here.

{% codeblock lang:ruby %}
gem 'capybara-webkit'
{% endcodeblock %}


Now create a file called `capybara.rb` inside your `spec/support` folder with this line:

{% codeblock lang:ruby %}
Capybara.javascript driver = :webkit
{% endcodeblock %}


Then uncomment this line from your `rails_helper.rb` file inside the `spec` folder:

{% codeblock lang:ruby %}
Dir[Rails.root.join("spec/support/**/*.rb")].each { |f| require f }
{% endcodeblock %}


Finally add `js: true` to your spec:

{% codeblock lang:ruby %}
feature "Visitor visits home page" do
  scenario "vistor visits home page and sees title", js: true do
    visit root_path

    expect(page).to have_content("Foo")
  end
end
{% endcodeblock %}

Now the test passes. That should get you started with using Capybara with the backbone-on-rails gem.

