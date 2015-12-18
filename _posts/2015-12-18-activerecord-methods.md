---
title:  "Rails - Adding ActiveRecord Methods To Your Non-ActiveRecord Models"
date:   2015-12-18 12:26:20 -0800
categories: rails
permalink: activerecord-methods
image: 
comments: true

---

Creating a Class that isn't in your database, yet you still want to use your favorite methods from ActiveRecord?

just add the following lines to your class definitions

##In Rails 3
{% highlight ruby %}
class Contact
    extend ActiveModel::Naming
    include ActiveModel::Conversion
    include ActiveModel::Validations	
{% endhighlight %}


##In Rails 4
{% highlight ruby %}
class Contact
    include ActiveModel::Model
{% endhighlight %}
