Intro to Erlang workshop - A Markov Chain generator in Erlang
=====

This is the Erlang application template that we will fill in as part of the Intro to Erlang workshop.

We will go through the slides covering Erlang, and then fill in the missing methods to complete the application to be able to generate Markov Chains of text.

Setup
------

### Install Erlang

Download Erlang from https://www.erlang-solutions.com/downloads/download-erlang-otp

### Install Rebar3

Download and install rebar3 and ensure it is in your path.

A download of nightly build of rebar3 can be found at: http://www.rebar3.org/

If you are on a Windows machine, the instuctions to bootstrap rebar3 can be found at https://github.com/rebar/rebar3#bootstrapping-rebar3

Build
-----

    $ rebar3 compile

Run
------
To open up an instance of the Erlang shell with the application loaded, run

    $ rebar3 shell

When all of the methods are filled in, we should be able to do a full run of the application in the shell.

```erlang
> TwoCities = "It was the best of times, it was the worst of times, it was
the age of wisdom, it was the age of foolishness, it was the epoch of belief,
it was the epoch of incredulity, it was the season of Light, it was the season
of Darkness, it was the spring of hope, it was the winter of despair, we had
everything before us, we had nothing before us, we were all going direct to
Heaven, we were all going direct the other way--in short, the period was so
far like the present period, that some of its noisiest authorities insisted
on its being received, for good or for evil, in the superlative degree of
comparison only.

There were a king with a large jaw and a queen with a plain face, on the
throne of England; there were a king with a large jaw and a queen with a fair
face, on the throne of France. In both countries it was clearer than crystal
to the lords of the State preserves of loaves and fishes, that things in
general were settled for ever.".

> markov:start().
> markov:prime(TwoCities).
> markov:generate_chain("It", 25).
```

Full Version
-------------

The full version can be found at https://www.github.com/stevenproctor/markov-erlang

Slides
-------

The slides accompaning this workshop can be found at https://github.com/stevenproctor/intro-to-erlang
