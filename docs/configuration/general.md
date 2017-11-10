This section provides a complete reference regarding the configuration possibilities of
[modules](./modules/), [components](./components/) and [configurations](./configurations/).
How these configuration possibilities are interpreted by Components.js can be found [here](../../loading/instantiation/).

## Semantic Configuration

Components.js uses _semantic configuration files_.
This means that these files encode their actual meaning by using standard vocabularies
in order to make these files machine-readable.

Configuration files must be defined in an [RDF](https://www.w3.org/RDF/).
Different kinds of RDF serializations exist and are supported by Components.js,
such as JSON-LD, Turtle, TriG, N-Triples or N-Quads.
We recommend using JSON-LD, because it is based on JSON and is easily interactable with JavaScript.

Components.js can understand a certain set of _predicates_ and _types_ in configuration files.
These are used to encode the actual meaning of the contents of these files.
_Predicates_ define the relationship type between two things,
and _types_ define the type of a thing.
For example, a certain predicate can be used to say that a given component is part of a given module.
These _predicates_ and _types_ are defined in _vocabularies_.

!!! note
    RDF allows graph-based datasets to be created by linking _things_ with certain _relationships_.
    These _things_ and _relationships_ are represented by literals or URIs.
    (Standard) **vocabularies** contain reusable _concepts_ and _relationships_.

!!! note
    RDF is a [W3C recommendation](https://www.w3.org/TR/rdf11-concepts/) for data interchange on the Web.

Because configuration files are defined in RDF, all applications that can handle RDF can work with these files and act on it,
such as reasoners, query engines, other dependency injection framework implementations, ...

## Vocabularies

The following vocabularies are (partially) understood by Components.js:

| Prefix | URL |
|--------|-----|
| oo     | https://linkedsoftwaredependencies.org/vocabularies/object-oriented# |
| om     | https://linkedsoftwaredependencies.org/vocabularies/object-mapping# |
| doap   | http://usefulinc.com/ns/doap# |
| rdf    | http://www.w3.org/1999/02/22-rdf-syntax-ns# |
| rdfs   | http://www.w3.org/2000/01/rdf-schema# |
| owl    | http://www.w3.org/2002/07/owl# |
| xsd    | http://www.w3.org/2001/XMLSchema# |

If the JSON-LD serialization is used, shortcuts can be used for most of the URLs using Components.js's context: [https://linkedsoftwaredependencies.org/contexts/components.jsonld](https://linkedsoftwaredependencies.org/contexts/components.jsonld)

These vocabularies will be referenced by their prefix and JSON-LD shortcut in the following sections.