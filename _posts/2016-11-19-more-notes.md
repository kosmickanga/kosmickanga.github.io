---
layout: post
title: "And then there were none"
date: 2016-11-19
---

Things to learn:

* Phoenix - and Elixir and Erlang.
* Clojure/ClojureScript. 

The question is, if Clojure offers a platform for both client and server, then do we need to learn Phoenix? I am not sure what exists on the JVM and how it compares to the Erlang platform. 
We have the example of WhatsApp as an indicator of the high performance of Erlang. What do we have for the JVM? And for my purposes, does it matter?

Fun with Clojure in VIM
-----------------------
Using Jessie on a Chromebook with Crouton, Vim is installed with vim-plugin as default. Fortunately there is a file in the .vim directory explaining how it works (almost). Need to run PlugInstall to pull the files off git into the plugged directory. Not the bundles directory, where I had tried to manually install to.

* fireplace - vim plugin. Needs python, and the emacs plugin..
* tmux - may as well learn that as I'm going to need umpteen shells (nRepl, vim, blog to make note).

Fireplace has a Piggieback command which uses Rhino. I have no idea what any of that means.( Update, this is for JavaScript REPLs so not relevant yet!)

Keys to remember
----------------

# tmux

* Ctrl-B 0, 1 etc
* Ctrl-B Up, Down, etc

# fireplace

* K - lookup docs for thing under cursor
* [d or ]d - source for thing under cursor
* same with Ctrl-D - jump to source under cursor
* gf - go to file of thing under cursor
* :Require ns, :Require! ns - load, reload/all for namespace
* ctrl-X ctrl-O - omnicomplete
* ctrl-X ctrl-U - some other thing
* cqp - bring up an eval window

As it's blowing a gale outside, I wrote a powerful weather forecast program:

~~~ clojure

(defn weather-forecast []
  {:temp (- 5 (rand 20))
   :wind (rand 60) 
   :direction (rand-nth [:sw :se :nw :ne :n :w :e :s])
   :outlook (rand-nth [:rain :drizzle :hail :fog :showers :stormy])})

(defn foo
  "I don't do a whole lot."
  [x]
  (println x "Hello, here is the forecast:")
   println (weather-forecast))
~~~
