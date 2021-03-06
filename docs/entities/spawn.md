---
layout: documentation
title: "Spawning new entities"
---

New entities can be generated by calling the `ox.spawn` method (shortcut for `ox.entities.spawn`).

----

**Parameters:**

- `type`: a string with the name/type of the entity.
- `options`: an object containing the options for the entity.

**Returns:**

[`entity`: an object]({{site.url}}/docs/entity/overview.html) with [`enable`]({{site.url}}/docs/entity/enable.html) and [`disable`]({{site.url}}/docs/entity/disable.html) methods along with an [`id`]({{site.url}}/docs/entity/id.html) and [`type`](({{site.url}}/docs/entity/type.html)) properties. It also inherits any properties and methods defined in the options object or the original entity file.

----

Each entity you spawn is unique - they have their own id and their own data. Changing the properties of one of them does not affect others.

{% highlight javascript %}
var tinyTimer = ox.spawn('timer', {
    target: 2000,
    callback: function() {
        console.log("Two seconds have elapsed!");
    }
});
{% endhighlight %}
