# NAME

App::Benchmark::Accessors - Benchmark accessor generators

# DESCRIPTION

This distribution runs benchmarks on various accessor generators. The
following generators are being benchmarked:

- Moose

    mutable and immutable

- Mouse

    mutable and immutable

- Class::Accessor
- Class::Accessor::Fast
- Class::Accessor::Fast::XS
- Class::XSAccessor::Compat
- Class::Accessor::Complex
- Class::Accessor::Constructor
- Class::Accessor::Classy
- Class::Accessor::Lite
- Mojo::Base
- Class::MethodMaker
- Object::Tiny
- Spiffy
- Class::Spiffy
- `accessors`
- Class::XSAccessor
- Class::XSAccessor::Array
- Object::Tiny
- Rose
- Rubyish::Attribute

The benchmarks are being run as part of the test suite; see [App::Benchmark](https://metacpan.org/pod/App::Benchmark).
This way you can look at this distribution's CPAN testers page to see the
benchmark results on many different platforms and for many different perl
versions.

The `t/construction.t` file benchmarks object creation, `t/get.t` benchmarks
getter methods and `t/set.t` benchmarks setter methods.

Not every benchmark is run on every module; for example, [Object::Tiny](https://metacpan.org/pod/Object::Tiny)
doesn't create setter methods, and [accessors](https://metacpan.org/pod/accessors) doesn't generate constructors.

Each benchmark test file takes an optional numeric parameter that is used as
the number of iterations.

It's probably a good idea not to read too much into these benchmarks; they
could be seen as micro-optimization. However, if you have a complex object
hierarchy and create lots of objects and run many many getters/setters on
them, they could help to save some time. But be sure to use [Devel::NYTProf](https://metacpan.org/pod/Devel::NYTProf)
first to see where your real bottlenecks are.

# AUTHORS

The following person is the author of all the files provided in
this distribution unless explicitly noted otherwise.

Marcel Gruenauer `<marcel@cpan.org>`, [http://marcelgruenauer.com](http://marcelgruenauer.com)

# COPYRIGHT AND LICENSE

The following copyright notice applies to all the files provided in
this distribution, including binary files, unless explicitly noted
otherwise.

This software is copyright (c) 2008 by Marcel Gruenauer.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
