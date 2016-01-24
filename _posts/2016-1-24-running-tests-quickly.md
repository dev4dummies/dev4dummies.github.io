---
title:  "Running Tests Quickly"
date:   2016-1-24 12:26:20 -0800
categories: rspec
permalink: running-tests-quickly
image: 
comments: true

---

So I was not having very much fun with Guard.

Having to install the gem. Having to write/alter the watch paths. Then having to put exceptions to tell it when not to run.

Ideally I would double-tap my esc key to run the tests any time I want.
The test would run, and my cursor would never have to leave the code I was writing.

Keyboard Maestro was the answer.

No, it's not free, but I'm glad I bought it. This is just one of hundreds of automations I've created with it.
Yeah there are free copies floating around but you are a well paid developer, right?

Within an hour you should be able to figure it out and build the workflow seen below.

How it works:

1. You double tap the esc key (or choose any other key you like)
2. Focus will shift to the app you have designated as your testing terminal. Terminal, in my case.
    
    A. I use iTerm2 with multiple tabs for my coding tasks. Server, bash, rails console, etc.
    
    B. I chose the default Terminal for running tests, and it displays on a different screen than my iTerm window.
    
    C. With a little more effort, it might be possible for Keyboard Maestro to detect one particular window of iTerm2, and to leave the others alone (AHK can do this on Windows), but choosing a different Terminal app altogether was the simplest solution for now.

3. Command-K clears the testing screen.
4. Your tests are run.
5. Focus is returned to your code.

![](https://dl.dropboxusercontent.com/spa/lkj2dewi3ofvkgc/m3aac7hx.jpg)