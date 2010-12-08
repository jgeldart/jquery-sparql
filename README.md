# jQuery SPARQL
## An idiomatic DSL for SPARQL queries 

[SPARQL] is to linked data as SQL is to relational databases. It is a query
language for semi-structured, open-ended data. SPARQL is also an 
increasingly popular way of exposing large datasets, such as those provided
by the [UK government].

jQuery SPARQL provides a DSL for programmatically constructing SPARQL queries
against some endpoint. It uses the same 'monadic' style that is used by [jQuery],
[Raphael], [Protovis] and other popular Javascript libraries to allow queries to 
be manipulated as first-class objects. The main aim of the library is to
eliminate messy string manipulations to produce and execute well-formed
queries.

Currently, the only substantial bit of jQuery used is its abstraction for
JSON-P. This may change as we look to concrete application use-cases. Beyond
jQuery, the library uses Yahoo!'s [YQL] service, specifically [Dave Beckett]'s 
Triplr table, to wrap around arbitrary SPARQL endpoints (which often don't
support either CORS or JSON-P). It is hoped that this part of the library can
be abstracted out soon.

## To Do

There are many things left to do with this library, including but not limited to:

- Abstracting out the execution system to support different endpoints and (maybe)
  any local SPARQL implementations.
- Support for more sorts of query than just SELECT (including update operators).
- Support for automatic coercion of RDF data types to Javascript ones.
- Integration with follow-on processing, such as DOM population, data analysis,
  summarisation and visualisation.
- Production of detailed documentation.
- Lots and lots of tests.

If you have any ideas about these things, or need to solve them for your work,
please get in touch and contribute to the project!  

[SPARQL]:http://www.w3.org/TR/rdf-sparql-query/
[jQuery]:http://jquery.com/
[Raphael]:http://raphaeljs.com/
[Protovis]:http://vis.stanford.edu/protovis/
[Dave Beckett]:http://www.dajobe.org/
[YQL]:http://developer.yahoo.com/yql/
[UK government]:http://data.gov.uk/
