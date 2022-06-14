formal_documentation

## Formal documentation
* `@post`: conditions that are true after execution of the method.
* `@pre`: conditions that need to be true at the start of the execution of a method.
* `@invar`: conditions that need to be true at a certain time
	* Public invariants:
		* Precede the _class_ definition.
		* Conditions on the values which _getters_ can return.
		* Must be true whenever no methods or constructors are being called.
	* Private invariants
		* Precede a _private field_ definition.
		* Conditions on the values of _private fields_.
		* It must always be true, also when a method or constructor is being called.
* `@representationObject`: _objects_ that or needed to represent a class abstract state.
	* If a representation object is mutable, the risk of representation exposure exists. Therefore, the object must be cloned when its getter or setter is used.
* `@mutates`: classes that are mutable and are inspected by a method.
	* Objects which are representationObjects of classes mentioned in the mutates tag are automatically added.
* `@inspects`: classes that are mutable and are inspected by the method.
	* Objects which are representationObjects of classes mentioned in the mutates/inspects tag are automatically added.
* `@peerObjects`: objects of which non-final fields or non-immutable properties are used, which are not representation objects.
	* Must be mentioned:
		* Above the variable definition
		* Above public getters for the peer object

#bioinformatics/semester_2/OOP/summary