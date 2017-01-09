#HSLIDE
![LOGO](http://emberjs.com/images/brand/ember_Ember-Dark.png)

#### Intro to Ember.js

#HSLIDE

### Components

#VSLIDE

###### A couple of ember components

```
{{my-component title='My Component'}}
{{#my-component title='My Component'}}Some content!{{/my-component}}
```

#VSLIDE

###### Templates

A component's template determines how it is rendered into its surrounding context...

```
<h1>{{title}}</h1>
<p>{{yield}}</p>
```
#VSLIDE

And uses handlebars.js and the keyword `yield` to figure out how to handle data passed in.
```
<h1>My Component</h1>
<p>Some content!</p>
```


#HSLIDE

### <span style="text-transform: none;">handlebars.js</span>

#VSLIDE

handlebars.js is a templating system that links component data with the DOM

#VSLIDE

Let's revisit `my-component`

```
{{my-component title='Some Title' anotherPlaceHolder='Another arbitrary string'}}
```

#VSLIDE

If the template for `my-component` references `title` or `anotherPlaceHolder`, handlebars.js allows us to pass this data through to the DOM like so:

```
<h1>{{title}}<h1>
<p>{{anotherPlaceHolder}}</p>
```

```
<h1>Some Title<h1>
<p>Another arbitrary string</p>
```

#VSLIDE

handlebars.js gives you simple tubes, but also lets you add some control to those tubes with control structures.

#VSLIDE?gist=0eb92e9f73dd373b68a00355cd890b83


#HSLIDE

###### Adding code to components

Components can be _way_ fancier than just simple pass-thru tubes. We can also add code to control the behaviour and logic of components.

#VSLIDE

Adding code to components allows us to make use of Ember's `computed` properties, also known as data binding