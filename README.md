
Thinking Flowbased Programming
==============================
A pratical book for understanding how to program
with flowbased- or dataflow programming,
aimed especially at programmers who have
some experience with imperative programming.

When and when not to use dataflow/FBP
=====================
What is it particularly well suited for
NB: potentially very subjective

Domains where dataflow is commonly used

* image processing
* video compositing
* audio processing



Imperative concepts
====================
What do they map to flowbased ones,
which patterns can be used by each

"variables"
"state"

conditionals (if, else)

loops (for, while)
    reductions to single variable
    mapping set of value to another
    filtering to create new set of values

inheritance
    interfaces
    traits/mixins
    resusing code

member variable
    collecting related state

doing things step by step
"first this, then that

recursion
call/return

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

asyncronous thinking
multiple-entries of functions at later time


Software engineering
====================
* organizing bigger systems
* introducing FBP/dataflow in existing system
* encapsulation
* error handling
* testing, verification
* debugging
* problem decomposition
* general vs. specialized solutions
* managing requirements changes



How to create
===============
Common things that people build

* protocols
* parsers
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


IDEA: verify code examples using tests

* challenge: need to verify both imperative and FBP version
* maybe use https://github.com/flowbased/fbp-spec or variation?

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



