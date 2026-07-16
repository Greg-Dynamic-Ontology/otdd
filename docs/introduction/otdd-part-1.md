# Ontology Test-Driven Development (OTDD)
*Engineering Knowledge Before Engineering Software*

Part 1, Version 0.1
July 2026

## Motivation

Artificial Intelligence has created unprecedented interest in ontologies. Nearly every 
discussion of improving AI eventually arrives at the conclusion that better structured knowledge 
produces better results.

Surprisingly, little has been written about improving the engineering process used to create 
that knowledge.

Software engineering has evolved from ad hoc programming through structured programming, 
object-oriented design, unit testing, continuous integration, and Test-Driven Development (TDD).
These methods transformed software development from an art into an engineering discipline.

Knowledge engineering deserves the same evolution.

Ontology Test-Driven Development (OTDD) applies the lessons learned from software engineering to 
the creation of ontologies, semantic mappings, validation rules, and other knowledge artifacts.

The objective is simple:

>Knowledge should be engineered with the same rigor that modern software engineering applies to 
> source code.

---
## What is OTDD?

Ontology Test-Driven Development is a **development methodology** in which expected semantic behavior is specified before 
the ontology or knowledge artifact is implemented.

Every increment of knowledge is accompanied by executable tests that demonstrate the intended 
semantic behavior.

Rather than asking
>"Did we build the ontology correctly?

OTDD asks
>"Can the intended knowledge be demonstrated automatically?"
---
## Knowledge and Projection

A recurring mistake in information technology is to confuse a representation with the knowledge 
it represents.

An ontology expressed in OWL is not the knowledge.

An XML document is not the knowledge.

A relational database is not the knowledge.

Each is merely a projection of an underlying body of knowledge into a particular 
representational space.

Every representation emphasizes some aspects of the knowledge while suppressing others. 
XML projects knowledge into a tree. RDF projects it into a graph. 
Relational databases project it into collections of two-dimensional tables. 
Decision matrices project it into two-dimensional grids. 
None of these projections is the knowledge itself.
A projection may preserve some properties perfectly while discarding others. Different 
projections therefore serve different engineering purposes.

The choice of representation should therefore be driven by the purpose for which the projection 
is created rather than by the mistaken belief that one representation is the knowledge.

OTDD begins with the knowledge and treats every formal artifact as a projection of that knowledge rather than as 
the knowledge itself.

An ontology can be thought of as a jewel. A jewel has many facets, each revealing the same 
underlying object from a different perspective. 
**No single facet is the jewel**, and no collection of visible facets completely captures its 
structure. 
Likewise, XML, RDF, OWL, SHACL, relational databases, documentation, and decision 
matrices are facets—projections that reveal particular aspects of an underlying body of 
knowledge. 
Engineering knowledge is therefore not about choosing the "correct" representation. 
It is about ensuring that each projection faithfully represents the underlying knowledge for 
its intended purpose.

The goal of OTDD is not to privilege one representation over another, but to ensure that 
every projection remains faithful to the underlying knowledge.

If representations are merely projections, then as much knowledge as possible should be 
represented explicitly rather than embedded in procedural software.

---
## Knowledge First
OTDD is based upon a simple observation:
> Everything that can reasonably be represented as knowledge should be represented as knowledge.

That includes:
- ontologies
- vocabularies
- mapping rules
- validation rules
- translation profiles
- business rules
- semantic measurements
- documentation relationships

>Software should become an interpreter of knowledge rather than a container for knowledge.

---
## Beyond Test-Driven Development
Traditional Test-Driven Development drives software implementation.

OTDD expands the target.

The artifacts under development may include:
- OWL ontologies
- SKOS vocabularies
- SHACL shapes
- RDF instance data
- translation profiles
- semantic mappings
- controlled vocabularies
- business rules

The implementation language is no longer the primary artifact.

The knowledge is.

---
## A New Example
Consider translating XML Schema (XSD) into RDF.

A conventional implementation embeds the translation rules in Python or Java.

OTDD instead represents the translation profile explicitly as RDF knowledge.

The translation profile itself becomes a first-class knowledge artifact.

For example,
```trig
GRAPH <https://dynamicontology.com/otk/translation-profile/basic-xsd-to-rdf> {

    otk-xsd:complexType
        otk:becomes owl:Class .

    otk-xsd:simpleType
        otk:becomes rdfs:Datatype .

}
```
The software no longer contains the translation policy.

It executes the translation policy.

This allows the translation itself to become a knowledge artifact that can be reviewed, 
versioned, tested, and extended independently of the software that executes it.

---
## Test-Driving Knowledge
OTDD extends the familiar TDD cycle.
```text
Specify expected knowledge
        ↓
Write semantic test
        ↓
Observe failure
        ↓
Create or modify knowledge artifact
        ↓
Observe success
        ↓
Refactor knowledge
```

The cycle is identical in spirit to TDD.

Only the primary artifact has changed.

The tests verify that each projection faithfully represents the intended knowledge.

The remainder of this series develops the following principles, which form the foundation of OTDD.

---
## The Principles
> Principle 1 — Representation Independence

> Principle 2 — Knowledge Transformations are Knowledge

> Principle 3 — Knowledge Before Code

> Principle 4 — Every Projection is Testable

>Principle 5 — Knowledge Has Many Valid Projections

OTDD is not merely a methodology for building ontologies. 
It is a methodology for engineering knowledge itself.
The remainder of this series develops these principles and demonstrates their application to 
ontology development, semantic validation, and knowledge transformation.
