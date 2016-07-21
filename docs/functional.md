# Functional

Without mutable variables, assignment, conditional

# Advantages [^1]

* Most functional languages provide a nice, protected environment, somewhat like JavaLanguage. It's good to be able to catch exceptions instead of having CoreDumps in stability-critical applications.
* FP encourages safe ways of programming. I've never seen an OffByOne mistake in a functional program, for example... I've seen one. Adding two lengths to get an index but one of them was zero-indexed. Easy to discover though. -- AnonymousDonor
* Functional programs tend to be much more terse than their ImperativeLanguage counterparts. Often this leads to enhanced programmer productivity.
* FP encourages quick prototyping. As such, I think it is the best software design paradigm for ExtremeProgrammers... but what do I know.
* FP is modular in the dimension of functionality, where ObjectOrientedProgramming is modular in the dimension of different components.
* Generic routines (also provided by CeePlusPlus) with easy syntax. ParametricPolymorphism
* The ability to have your cake and eat it. Imagine you have a complex OO system processing messages - every component might make state changes depending on the message and then forward the message to some objects it has links to. Wouldn't it be just too cool to be able to easily roll back every change if some object deep in the call hierarchy decided the message is flawed? How about having a history of different states?
* Many housekeeping tasks made for you: deconstructing data structures (PatternMatching), storing variable bindings (LexicalScope with closures), strong typing (TypeInference), * GarbageCollection, storage allocation, whether to use boxed (pointer-to-value) or unboxed (value directly) representation...
* Safe multithreading! Immutable data structures are not subject to data race conditions, and consequently don't have to be protected by locks. If you are always allocating new objects, rather than destructively manipulating existing ones, the locking can be hidden in the allocation and GarbageCollection system.

[^1]: [Advantages Of Functional Programming](http://c2.com/cgi/wiki?AdvantagesOfFunctionalProgramming)

