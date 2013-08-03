---
layout: post
title: Backbone + Django Rest Framework (part 1)
---

### Setting up a backbone app
{% highlight js %}
/* config.js */
// Namespace
var App = App || {};
App.Models = {};
App.Views = {};
App.Collections = {};
App.Routers = {};

/* <APP>/models.js */
App.Models.PageModel = Backbone.Model.extend({});

{% endhighlight %}

