PicoHTTPParser
=============

Copyright (c) 2009-2014 [Kazuho Oku](https://github.com/kazuho), [Tokuhiro Matsuno](https://github.com/tokuhirom), [Daisuke Murase](https://github.com/typester), [Shigeo Mitsunari](https://github.com/herumi)

PicoHTTPParser is a tiny, primitive, fast HTTP request/response parser.

Unlike most parsers, it is stateless and does not allocate memory by itself.
All it does is accept pointer to buffer and the output structure, and setups the pointers in the latter to point at the necessary portions of the buffer.

The code is widely deployed within Perl applications through popular modules that use it, including [Plack](https://metacpan.org/pod/Plack), [Starman](https://metacpan.org/pod/Starman), [Starlet](https://metacpan.org/pod/Starlet), [Furl](https://metacpan.org/pod/Furl).  It is also the HTTP/1 parser of [H2O](https://github.com/h2o/h2o).

Check out [test.c] to find out how to use the parser.

The software is dual-licensed under the Perl License or the MIT License.

Benchmark
---------

![benchmark results](http://i.gyazo.com/0b00867f13c73c2bb4cece3ed341be96.png)

The benchmark code is from [fukamachi/fast-http](https://github.com/fukamachi/fast-http/).

The internals of picohttpparser has been described to some extent in [my blog entry]( http://blog.kazuhooku.com/2014/11/the-internals-h2o-or-how-to-write-fast.html).
