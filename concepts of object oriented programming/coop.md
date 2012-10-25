Concepts of Object Oriented Programming - Summary
=================================================
Pascal Spörri <pascal@spoerri.io>

## Types and Subtyping

### Types

Definition Type System: 
> A type system is a tractable syntactic method for proving absence of certain program behaviors by classifying phrases according to the kinds of values they compute.

>* Syntactic: Rules are based on form and not behavior
>* Phrases: Expressions, methods, etc. of a program
>* Kinds of values: Types

#### Type systems

Untyped languages:

* Do not classify values into types
* Example: Assembler

Weakly-typed languages:

* Classify values into types, but do not strictly enforce additional restrictions
* Examples: C, C++

Strongly-typed languages:

* Enforce that all operations are applied to arguments of the appropriate types.
* Examples: C#, Eiffel, Java, Python, Scala, Smalltalk


Definition Type:
> A type is a set of values sharing some properties. A value v has type T if v is an element of T.

##### Nominal Types
The type is based on the type name. Examples:
>	C++, Eiffel, Java, Scala

##### Structural Types
The type is based on the _availability of methods and fields_. Examples:
> Python, Ruby, Smalltalk

#### Type Checking

##### Static Type Checking

* Each expression of a program has a type (Java):

		"A string"
		5 + 7

* Types of variables and methods are declared explicitly or inferred (Java):

		int a;
		boolean equals(Object o)

* Types of expressions can be derived from the types of their constituents (Java):

		a + 7
		"A number: " + 7
		"A string".equals( null )

* Type rules are used at compile time to check whether a program is correctly typed. 

##### Dynamic Type Checking

* Variables, methods, and expressions of a program are typically not typed (Python): 

		"A string"
		5 + 7
		a = 42;
		def foo (o): …

* Every object and value has a type (Python):

		a + 7
		"A number: " * 7
		foo(none)

		a = "A String"
		a = 7

* Run-time system checks that operations are applied to expected arguments


### Subtyping

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
* Inheritance is _usually coupled_ with subtyping. 

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

All object-oriented languages support multiple subtyping:

* One type can have several supertypes 
* Subtype relation forms a DAG.

