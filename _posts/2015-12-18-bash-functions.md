---
title:  "Bash Functions You Need To Use"
date:   2015-12-18 12:26:20 -0800
categories: unix bash
permalink: bash-functions
image: 
comments: true

---

Ever with you could do this to create a file with all the necessary folders?

{% highlight %}
    touch public/views/about.html
{% endhighlight %}

just open up your .bash_profile file and paste in the following function

{% highlight %}
ptouch() {
  for p in "$@"; do
    _dir="$(dirname -- "$p")"
    [ -d "$_dir" ] || mkdir -p -- "$_dir"
    touch -- "$p"
  done
}
{% endhighlight %}

and now (after you reboot your terminal or type

    source ~/.bash_profile
    
you can type
    
    ptouch public/views/about.html

and rejoice.

While we're add it, add

{% highlight %}
mcd() { 
  mkdir -p $1
  cd $1
}
{% endhighlight %}

so you can `mcd myproject`, which creates a directory and puts you inside that directory all in one command.

Yay.