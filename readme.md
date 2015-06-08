## Employee Directory ##

### Sample Application built with Backbone.js ###

### 08-07-2015 ###
### Tasks: ###

1.Display list of employees with search form on index page by default.
2. Search input should filter employees by First/Last names or should show message 'No employees found'.
3. Refactoring:

- Rewrite ```model.on``` calls with ```view.listenTo(model, 'event', action);```
>The advantage of using this form, instead of ```model.on(event, callback, object)```, 
>is that *listenTo* allows the object to keep track of the events, and they can be removed all at once later on. 

- Rewrite ```$('selector',  context)``` i.e. ```$('#reports', this.el)``` to ```this.el.find('selector')```
There should not be "global" DOM quering, i.e $('selector'),  view should be responsible only for its own elements.

- Extract rendering subViews to separate method, i.e.

```this.$el.append(new directory.EmployeeListItemView({model:employee}).render().el);```
or
```$('.navbar-search', this.el).append(this.searchresultsView.render().el);```
 should be extracted

- Rewrite fetching with 'success' callbacks to jqXHR Object.  	


<hr />


"Backbone Directory" is a simple Employee Directory application built with [Backbone.js](http://backbonejs.org) and [Twitter Bootstrap] (http://twitter.github.io/bootstrap/).

Refer to [this blog post](http://coenraets.org/blog/2013/04/sample-application-with-backbone-js-and-twitter-bootstrap-updated-and-improved/) for more information about the application.


