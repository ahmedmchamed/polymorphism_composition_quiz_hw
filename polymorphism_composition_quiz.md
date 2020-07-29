# Polymorphism & Composition Homework - Quiz

# Polymorphism

**1. What does the ___word___ 'polymorphism' mean?**

The ability for an object to take on multiple forms.

**2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.**

A derived class type can take the form of its base class type.

```java
class Deer extends Animal implements IRun {}
```
In this case, the derived class type `Deer` can take the form of its base class type `Animal`, or of the interface `IRun`. If it does so however, it will only have the operations available in the `Animal` class or `IRun` interface respectively.

**3. What can we use to implement polymorphism in Java?**

We can use the operations available in a base class via an object of one of its derived classes.

**4. How many 'forms' can an object take when using polymorphism?**

You can only perform single inheritance from another class in Java, but there can be an inheritance chain 
where there are multiple single inheritances. Classes can implement multiple interfaces, however, and also
take on the "form" of that interface type. In that sense, there can be multiple forms that an object can take.

**5. Give an example of when you could use polymorphism.**

In the use of an abstract class that multiple derived classes can inherit a set of common methods and attributes/properties from.

# Composition

**6. What do we mean by 'composition' in reference to object-oriented programming?**

When an class type object is composed of other class type objects as attributes/properties.
Usually when you want to think of what an object *HAS*, rather than what it *IS*.

**7. When would you use composition? Provide a simple example in Java.**

It is not always necessary to inherit from another class to use its specific operations.
If you need a specific behaviour or component from another class, composition would be better suited than
inheritance.
```java
class Brick {
    private int brickSize;
}

class SmallHouse {
    private Brick brick;
}
```

**8. What is/are the advantage(s) of using composition?**

* Makes the program structure and class implementations easier to follow.
* Avoids confusion by limiting number of potential methods that would need to be overridden.

**9. When an object is destroyed, what happens to all the objects it is composed of?**

An object *owns* all of the other objects that form its composition.
When an object is destroyed, all of the objects it is composed of are also destroyed as a result.