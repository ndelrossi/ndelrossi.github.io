---
layout: post
title: "CoffeeScript vs JavaScript for Beginners"
date: 2015-01-26 15:52:42 -0500
comments: true
categories: [CoffeeScript, JavaScript] 
---
As part of the Ruby community I've seen it recommended in many places that a beginner start with CoffeeScript instead of regular JavaScript. The argument is usually that CoffeeScript is more elegant, more Ruby like, and that you can get more done with less code.

This may all be true. CoffeeScript is better looking than JavaScript and I found it an enjoyable language to write code in. However, I recently decided to give up on it for now and to rewrite an entire app I was working on in vanilla JavaScript. As a relative beginner in both languages I won't try to argue that either is better in a professional setting, but I do think that recommending CoffeeScript for a beginner may not be the best advice.

Here are three reasons based on my own experience:

<!--more-->

<strong>1: Resources</strong><br>

There are way more resources written in JavaScript than there are in CoffeeScript. If a beginner wants to learn how to do something specific with their website they are likely visiting google, stackoverflow, or any number of tutorial websites. Most of the examples will be in JavaScript.

For instance I did a search on Amazon for books about CoffeeScript. I got 74 results. When I change my search to JavaScript the results jump to 6,984. It's a lot easier to learn anything that has more resources available.

This point alone I think is a poor argument. The same logic might suggest a beginner learn PHP over Ruby. On to my next two points.

<strong>2: Debugging</strong><br>

You can write all the beautiful CoffeeScript you want but as soon as you need to start debugging your code, it's all in JavaScript. It also often isn't just a little different. If a beginner writes this function code for rendering a view in backbone:

{% codeblock lang:coffeescript %}
render: ->
  @$el.html(@template())
  this
{% endcodeblock %}

And then goes to debug, they will likely see this:

{% codeblock lang:javascript %}
render: function() {
  this.$el.html(this.template());
  return this;
}
{% endcodeblock %}

Well thats not a big deal. The code is very similar, but how about an entire backbone view class in CoffeeScript:

{% codeblock lang:coffeescript %}
class App.Views.Example extends Backbone.View
  template: JST['example/example']

  render: ->
    @$el.html(@template())
    this
{% endcodeblock %}

That tiny bit of code becomes this when you go to debug:

{% codeblock lang:javascript %}
(function() {
  var __hasProp = {}.hasOwnProperty,
    __extends = function(child, parent) { for (var key in parent) { if (__hasProp.call(parent, key)) child[key] = parent[key]; } function ctor() { this.constructor = child; } ctor.prototype = parent.prototype; child.prototype = new ctor(); child.__super__ = parent.prototype; return child; };

  App.Views.Example = (function(_super) {
    __extends(Example, _super);

    function Example() {
      return Example.__super__.constructor.apply(this, arguments);
    }

    Example.prototype.template = JST['example/example'];

    Example.prototype.render = function() {
      this.$el.html(this.template());
      return this;
    };

    return Example;

  })(Backbone.View);

}).call(this);
{% endcodeblock %}

That is going to be extremely confusing to any beginner. It might be correct, efficient code, but it is also unreadable if you are new.

<strong>3: Extra Complexity</strong><br>

Beginners have a lot of stuff to learn in web development. There are many technologies that go into creating a modern web app so I think it's best to keep things simple and not introduce unnecessary steps. The debugging issue is going to force a beginner to learn JavaScript anyway so this means learning two very similar languages at the same time. I think it might be better to get comfortable with regular JavaScript first and move on to CoffeeScript later.
