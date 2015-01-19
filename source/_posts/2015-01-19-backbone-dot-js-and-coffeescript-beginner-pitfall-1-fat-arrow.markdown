---
layout: post
title: "Backbone.js and Coffeescript Beginner Pitfall 1: Fat Arrow"
date: 2015-01-19 14:29:30 -0500
comments: true
categories: backbone coffeescript
---
While learning backbone.js and coffeescript I have run into many beginner issues that have tripped me up. This is the first of several I plan to write about and hopefully save myself and others some trouble.

Inside of a View class you have some very simple code:

{% codeblock lang:coffeescript %}
class App.Views.Example extends Backbone.View
  template: JST['layout/example']

  render: ->
    @$el.html(@template())
    this.changeSomeText()

  changeSomeText: ->
    @$el.text("Changed Text")
{% endcodeblock %}

I am using a very silly example just to keep it simple. Basically you are rendering a view and then calling a method to change the text inside that view right after. This code will work just fine.

But what if you only wanted that text to change after the user hovers over the div. Seems like a simple change:

{% codeblock lang:coffeescript %}
class App.Views.Example extends Backbone.View
  template: JST['layout/example']

  render: ->
    @$el.html(@template())
    @$el.hover ->
      this.changeSomeText()

  changeSomeText: ->
    @$el.text("Changed Text")
{% endcodeblock %}

This won't work. You will get the following error:

<span style="color:red">Uncaught TypeError: undefined is not a function</span>

So what is going on here and how do we get this to work?

<!--more-->

The problem is that you now have a callback and inside a callback the value of `this` has changed. It no longer refers to the View so calling your View method on `this` will not work.

What you could do is bind a variable `self` to `this` before the function:

{% codeblock lang:coffeescript %}
self = this
@$el.hover ->
  self.changeSomeText()
{% endcodeblock %}

It works but coffeescript has an easier way to solve this. You can just use a fat arrow `=>` instead of the thin arrow `->` like so:

{% codeblock lang:coffeescript %}
@$el.hover =>
  self.changeSomeText()
{% endcodeblock %}

Now it works again. After seeing that error many times I now have it engrained in my head to use the fat arrow when using `this` inside callback functions.
