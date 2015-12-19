---
title:  "Bash Functions You Need To Use"
date:   2015-12-18 12:26:20 -0800
categories: unix bash
permalink: bash-functions
image: 
comments: true

---

Ever wish you could type this to create a file along with any necessary folders?

    touch public/views/about.html


Just open up your .bash_profile file and paste in the following function

    ptouch() {
      for p in "$@"; do
        _dir="$(dirname -- "$p")"
        [ -d "$_dir" ] || mkdir -p -- "$_dir"
        touch -- "$p"
      done
    }

and now (after you either reboot your terminal or type)

    source ~/.bash_profile
    
you can type
    
    ptouch public/views/about.html

and rejoice.

While we're add it, add

    mcd() { 
      mkdir -p $1
      cd $1
    }


so you can `mcd myproject`, which creates a directory and puts you inside that directory all in one command.

Yay.