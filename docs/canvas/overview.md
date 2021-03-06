---
layout: documentation
title: "Canvas overview"
---

Ox by default exposes the canvas API through `ox.context` and the canvas itself through `ox.canvas`, meaning you can enjoy all the niceties that come from it.

----

**Methods**

- [`ox.context`]({{site.url}}/docs/canvas/methods.html)

**Properties**

- [`width`]({{site.url}}/docs/canvas/properties.html), [`height`]({{site.url}}/docs/canvas/properties.html)

----

### Pong example

Imagine we want to create the paddle that is going to be used for the game. Our paddle entity could be like this:

{% highlight javascript %}
module.exports = {
    init: function() {
        this.y = ox.canvas.height/2; //Vertically center the entity
    },
    
    draw: function() {
        ox.context.fillStyle = "grey";
        ox.context.fillRect(this.x, this.y, 20, 80);
    }
};
{% endhighlight %}

Done!