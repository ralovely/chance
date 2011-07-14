Chance
=========

Chance is a little Ruby library for expressing uncertainty in your code. Maybe you always wanted to program with probability?

The idea originated with Numeric#percent and Kernel#maybe, which Marcel Molina posted to Projectionist, a tumblelog.  This led to various snippets for executing code in a fuzzier way than usual.  You get such handy, wishy-washy methods as:

Date#at_some_point rather than Date#midnight
Array#pick(percentage) rather than iterating over every element

"maybe" is a Kernel method that randomly evaluates to true or false when it is called.

`@bob.lucky_winner? = maybe`
# => true
`@chauncey.lucky_winner? = maybe`
# => false

When supplied with a block, it will call it. Or not. Half of the time it just returns nil. For example

`maybe {rotate_logs}`

By default, maybe is 50/50.  You can also use "probably", "rarely" and "almost_never", or just create your own Chance object like so:

`30.percent.chance.of { "rain" }`

Running examples
----------------
Make sure you have Bundler installed- then run  `bundle exec rake`.