Concepts of Object Oriented Programming - Summary
=================================================
Pascal Spörri <pascal@spoerri.io>

## Subtyping

### Behavioral Subtyping

Subtype objects must *fullfill contracts* of supertypes but:

* Subtypes can have *stronger invariants*
* Subtypes can have *stronger history invariants*
* Overriding methods of subtypes can have 

	_weaker preconditions_ and _stronger postconditions_

	than corresponding supertype methods

## Inheritance

_Subtyping_ expresses _classification_:

* Substitution principle
* Subtype polymorphism

_Inheritances_ is a means of _code reuse_:

* Specialization

Inheritance is _usually coupled_ with subtyping. 

### Subclassing

_Subclassing_ = Subtyping + Inheritance

* Can be simulated by a combination of subtyping and aggregation. 
* OO-programming can do without inheritance, but not without subtyping. 
* Only use subclassing if there is an _"is-a" relation_

### Dynamic Method Binding

* Static  Binding:
	
	_At compile time_, a method declaration is select for each call _based on the static type_ of the receiver expression.

	Languages: C++, C#

* Dynamic Binding:

	_At run time_, a method declaration is selected for each call _based on the dynamic type_ of the receiver object.

	Languages: Eiffel, Java, Scala, dynamically-typed languages

	
### Multiple Inheritance


