* Hello World This is testing article.

![Java Statments]({{ "https://i.postimg.cc/fW9B6qD6/factfor-Orio-01.jpg" | absolute_url }})

Abstract class achieves partial abstraction whereas interface achieves fully abstraction.

An abstract class’s purpose is to provide an appropriate superclass from which other classes can inherit and thus share a common design.

An interface describes a set of methods that can be called on an object but does not provide concrete implementations for all the methods. Once a class implements an interface, all objects of that class have an is-a relationship with the interface type, and all objects of the class are guaranteed to provide the functionality described by the interface. This is true of all subclasses of that class as well. Interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler

![Java Statments]({{ "https://i.postimg.cc/pTNCsGBH/banner-ad-online-shopping-html5-google-banner-ad-23-0efforttheme.jpg" | absolute_url }})

Use abstract classes and inheritance if you can make the statement “A is a B”. Use interfaces if you can make the statement “A is capable of [doing] as”, or also, abstract for what a class is, interface for what a class can do. We can say a triangle is a polygon but it makes no sense to say a triangle is capable of being a polygon

Consider using abstract classes if any of these statements apply to your situation:

You want to share code among several closely related classes.
You expect that classes that extend your abstract class have many common methods or fields or require access modifiers other than public (such as protected and private).
You want to declare non-static or non-final fields. This enables you to define methods that can access and modify the state of the object to which they belong.
Consider using interfaces if any of these statements apply to your situation:

<iframe width="560" height="315" src="https://www.youtube.com/embed/2nY2BoXNQoA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

You expect that unrelated classes would implement your interface. For example, the interfaces Comparable and Cloneable are implemented by many unrelated classes.
You want to specify the behavior of a particular data type, but not concerned about who implements its behavior.
You want to take advantage of multiple inheritances.
