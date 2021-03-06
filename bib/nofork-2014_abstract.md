---
layout: page
title: 'There is No Fork: An Abstraction for Efficient, Concurrent, and Concise Data Access'
description: ""
category: publications
tags: []
---
(Simon Marlow, Louis Brandy, Jonathan Coens, Jon Purdy) *Proceedings of the 19th ACM SIGPLAN International Conference on Functional Programming*, pages 325--337, Gothenburg, Sweden, ACM, 2014

<a href="http://simonmar.github.io/bib/papers/haxl-icfp14.pdf">Full Paper</a> | <a href="nofork-2014.bib">BibTeX</a>

We describe a new programming idiom for concurrency, based on
Applicative Functors, where concurrency is implicit in the Applicative
<*> operator. The result is that concurrent programs can be written in
a natural applicative style, and they retain a high degree of clarity
and modularity while executing with maximal concurrency. This idiom
is particularly useful for programming against external data sources,
where the application code is written without the use of explicit
concurrency constructs, while the implementation is able to batch
together multiple requests for data from the same source, and fetch
data from multiple sources concurrently.  Our abstraction uses a cache
to ensure that multiple requests for the same data return the same
result, which frees the programmer from having to arrange to fetch
data only once, which in turn leads to greater modularity.

While it is generally applicable, our technique was designed
with a particular application in mind: an internal service at Face-
book that identifies particular types of content and takes actions
based on it. Our application has a large body of business logic that
fetches data from several different external sources. The framework
described in this paper enables the business logic to execute ef-
ficiently by automatically fetching data concurrently; we present
some preliminary results.
