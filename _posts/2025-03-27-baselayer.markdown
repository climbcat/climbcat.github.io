---
layout: post
title:  "Baselayer"
date:   2025-03-25 10:59:15 +0100
categories: code project
---

Have you ever written a pointer-hash map? It is surprisingly fun.

At some point I discovered the existence of custom memory allocators, custom buffers and length-based strings.
I started writing my own versions and collected some of the code in homebrew libraries ([baselayer] and [cbui]).

The libraries provide many of the basic tools for effectively writing programs in a small language like C, and explore new techniques.
It feels luxurious to not have to worry about gigabytes of helper libraries, and reading monolithic APIs, just to do relatively basic 
and normal things in C.

The concept of header-only libraries seemed well worth copying. Using "unity build", the entire program is statically compiled from source.
Code is organized in .h files, meaning the headers and implementations are found in the same place. This is already standard practice in 
most languages - so why not?

A rudimentary CMake config file in included, for convenience and for seamless integration with certain tools.

[baselayer]: https://github.com/climbcat/baselayer
[cbui]: https://github.com/climbcat/cbui
