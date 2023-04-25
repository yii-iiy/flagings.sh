# flagings.sh

~~~~
🪁 many very useful functions make your shell works have more elegant 🎊
~~~~

----

## Install

In my way, you can just put this file into your `/etc/profile.d`, that's all done.

Or you can copy the code and use them in your way, **just don't forget to comply with *the license* of this project**.

## Use case

If you're installed it in *my way*, you can run this to import the tools while you want to use them:

~~~ sh
Flagings
~~~

Then, all tools will be usable.

There're some use cases for them.

### `raise`

Trans a *line* in to *vertical*.

#### 1. (simple) Basic use case

It makes your args into a %each arg one line* text and you can get this text by its *stdout*.

Such as run:

~~~ sh
raise iroh tauri ⚗elixir duckduckgo qwant vow flower $'Tree\'s leaf' "hoo  oolder" 🥗🥗🥗 smile
~~~

Then it will out:

~~~ text
iroh
tauri
⚗elixir
duckduckgo
qwant
vow
flower
Tree's leaf
hoo  oolder
🥗🥗🥗
smile
~~~

And you can use it like this in your defines (such as *script* or *function* ...):

~~~
raise "$@"
~~~

#### 2. (advance) Give me the first valuable

Sometimes, you only want the first not-empty-value in a list. You can solve your request clearly -- just by call this `raise` command.

~~~ sh
eacher=per raiser='test -n "$per" && { echo "$per" && break ; }' raise "$@"
~~~

The *a list of value* I've told is `"$@"`, and the first value that not empty will be send to the *stdout* of this call.

You can test it by this demo:

~~~ sh
eacher=per raiser='test -n "$per" && { echo "$per" && break ; }' raise '' '' '' "" $'Tree\'s leaf' "hoo  oolder" 🥗🥗🥗 smile
~~~

The out should be:

~~~ text
Tree's leaf
~~~


### `_sign`

This tool's behavior just like the `=`.


