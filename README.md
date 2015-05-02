
Thinking Flowbased Programming
==============================
A pratical book for how to program
with flowbased- or dataflow programming.
Aimed especially at programmers who have
some experience with imperative & object-oriented programming.

Focused on general purpose programming,
and independent of a particular FBP implementation.

Intended primarily as an e-book,
but also publishable on dead trees.

When and when not to use dataflow/FBP
=====================
What is it particularly well suited for, which things are tricky.
*NB: potentially very subjective*

Domains where dataflow is commonly used

* image processing
* video processing, compositing
* audio processing

Important to note that dataflow/FBP and imperative/OOP is not
exclusive, but instead complimentary:

* Components are typically implemented in imperative code
* Can send/receive data from FBP network (short- or long-lived) in imperative code
* Can use FBP for parts of problem, communicate using IPC/database


Imperative concepts
====================
What do they map to flowbased ones,
which patterns can be used by each

"variables" & "state"
--------
Used for many different purposes...

Local versus shared/global.
Shared state should be expressed as data in network.
Local state can be done inside components.

conditions (if, else)
----------------------

Maps to routing and/or filtering components.

loops (for, while)
-------------------
Used for several purposes

* *reduce* set of values to single value. Ex: SUM
* *map* set of value to another. Ex: Vector add
* *filter* to create new set of values. Ex: values bigger than threshold

functions
-----------
Used to reuse code in multiple places.

Maps roughly to components.
Functions calling other functions is like a subgraph.

classes, inheritance
------------
Used for:

* interfaces
* traits/mixins
* resusing code

member variable

* collecting related state
* maintaining state over multiple function calls

sequencing
------------
Doing things step by step. "first A, then B, then C"
https://github.com/noflo/noflo/issues/284

* recursion
* call/return

concurrency (threads, mutex, semaphores)
------------------

composite data (structs, objects)
---------------


collections (array, dictionary, sets)
----------------

Dictionaries sometimes used for dynamic dispatch


Flowbased concepts
==================
TODO: refer out to books for source of definitions

Central definitions

* Component: 
* Port:
* Process: Component instance
* Connection: 
* Graph: definition of 
* Network: Graph instance
* Packet:
* IIP:

Common classes of components

* routers
* filters

Firing patterns


Things hard to grasp
================
For those used to imperative programming.
Some of these might not be unique to dataflow/FBP

* asyncronous thinking, multiple-entries of functions (at later time)


Software engineering practices
====================
Things that might go outside a narrow view of programming,
but are essential to programming from a software engineering
perspective.
Or aspects of software design which influences how software
should (as opposed to could) be made.

* organizing bigger systems. Subgraphs, groups
* introducing FBP/dataflow in existing system
* encapsulation
* error handling
* testing, verification. TDD/BDD
* debugging. Breakpoints map to data breakpoints.
* problem decomposition
* general vs. specialized solutions
* managing changes in requirements



How to create
===============
Common things that people build

* protocols
* parsers
* plugin systems
* state machines
* user interfaces
* web services

Book creation process
=====================

IDEA: run a book sprint

* invite a selection of experienced dataflow/FBP practicioners
* invite an experienced booksprint person
* sit together for 3-7 days
* write the book from start to end, publish before leaving

IDEA: use [Stack Overflow](stackoverflow.com)?

* put questions/answers up
* consider the book a curated & editorialized version
* scripts for syncing the
* use SO comments etc to handle errata

Code examples

* should be small program snippets, comparing imperative code and FBP code
* should exist as a full runnable piece of code somewhere
* FBP graph must be rendered to image. Maybe using https://github.com/the-grid/the-graph
* imperative code must be syntax highlighted

IDEA: verify code examples using tests

* challenge: need to verify both imperative and FBP version
* maybe use https://github.com/flowbased/fbp-spec or variation?

IDEA: consider building a "cheat sheet"

* Two-way mapping between concepts/patterns in imperative and FBP
* Must be searchable
* Should fit on couple of pages

References
===========

Literature

* J. Paul Morrison: Flow-based programming
* Matt Charki: Dataflow & Reactive programming
* Paul Tarvydas whitepapers on bmFBP etc, https://bittarvydas.wordpress.com/
TODO: put whitepapers up online
TODO: verify link
* http://scriptogr.am/alfredo
* http://expressionflow.com/

Help/docs for particular dataflow software (could extract general lessons)

* [Pure Data](https://puredata.info/docs/BooksAboutPd/), Max MSP
* LabView
* Blender, Nuke
* Native Instruments
* [NoFlo](http://stackoverflow.com/questions/tagged/noflo)



