# Design Patterns Interview Questions

In software engineering, a design pattern is a general repeatable solution to a commonly occurring problem in software design. A design pattern isn't a finished design that can be transformed directly into code. It is a description or template for how to solve a problem that can be used in many different situations.

> You could also find all the answers here 👉 https://www.fullstack.cafe/Design%20Patterns


## Q1: What are the main categories of Design Patterns? ⭐

**Answer:**

The Design patterns can be classified into three main categories:

* Creational Patterns
* Behavioral Patterns
* Functional Patterns

🔗 **Source:** [www.educba.com](https://www.educba.com/design-pattern-interview-questions/)


## Q2: What is Design Patterns and why anyone should use them? ⭐

**Answer:**

Design patterns are a well-described solution to the most commonly encountered problems which occur during software development. 

Design pattern represents the best practices evolved over a period of time by experienced software developers. They promote reusability which leads to a more robust and maintainable code.

🔗 **Source:** [www.educba.com](https://www.educba.com/design-pattern-interview-questions/)


## Q3: What is a pattern? ⭐

**Answer:**

*Patterns* in programming are like recipes in cooking. They are not ready dishes, but instructions for slicing and dicing products, cooking them, serving them and so forth.

**Pattern content**
As a rule, a pattern description consists of the following:

* a problem that the pattern solves;
* motivation for solving the the problem using the method suggested by the pattern;
* structures of classes comprising the solution;
* an example in one of the programming languages;
* a description of the nuances of pattern implementation in various contexts;
relations with other patterns.

🔗 **Source:** [refactoring.guru](https://refactoring.guru/design-patterns/what-is-pattern)


## Q4: What is Singleton pattern? ⭐

**Answer:**

**Singleton pattern** comes under *creational* patterns category and introduces a single class which is responsible to create an object while making sure that only single object gets created. This class provides a way to access its only object which can be accessed directly without need to instantiate the object of the class.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Singleton_UML_class_diagram.svg/220px-Singleton_UML_class_diagram.svg.png" class="img-fluid"/>
</div>


🔗 **Source:** [refactoring.guru](https://refactoring.guru/design-patterns/what-is-pattern)


## Q5: What is Dependency Injection? ⭐⭐

**Answer:**

*Dependency injection* makes it easy to create loosely coupled components, which typically means that components consume functionality defined by interfaces without having any first-hand knowledge of which implementation classes are being used.

*Dependency injection* makes it easier to change the behavior of an application by changing the components that implement the interfaces that define application features. It also results in components that are easier to isolate for unit testing.

🔗 **Source:** [Pro ASP.NET Core MVC 2](https://github.com/TechBookHunter/Free-CSharp-Books/blob/master/book/Pro%20ASP.NET%20Core%20MVC%202%20-%20Seventh%20Edition.pdf)


## Q6: What is Inversion of Control? ⭐⭐

**Answer:**


*Inversion of control* is a broad term but for a software developer it's most commonly described as a pattern used for decoupling components and layers in the system. 

For example, say your application has a text editor component and you want to provide spell checking. Your standard code would look something like this:
```js
public class TextEditor {

    private SpellChecker checker;

    public TextEditor() {
        this.checker = new SpellChecker();
    }
}
```
What we've done here creates a dependency between the TextEditor and the SpellChecker. In an IoC scenario we would instead do something like this:
```js
public class TextEditor {

    private IocSpellChecker checker;

    public TextEditor(IocSpellChecker checker) {
        this.checker = checker;
    }
}
```

You have *inverted control* by handing the responsibility of instantiating the spell checker from the TextEditor class to the caller.

```js
SpellChecker sc = new SpellChecker; // dependency
TextEditor textEditor = new TextEditor(sc);
```


🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/3058/what-is-inversion-of-control?page=1&tab=votes#tab-top)


## Q7: Name types of Design Patterns? ⭐⭐

**Answer:**

Design patterns can be classified in three categories: Creational, Structural and Behavioral patterns.

-   Creational Patterns - These design patterns provide a way to create objects while hiding the creation logic, rather than instantiating objects directly using new opreator. This gives program more flexibility in deciding which objects need to be created for a given use case.

-   Structural Patterns - These design patterns concern class and object composition. Concept of inheritance is used to compose interfaces and define ways to compose objects to obtain new functionalities.

-   Behavioral Patterns - These design patterns are specifically concerned with communication between objects.

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q8: What is Factory pattern? ⭐⭐

**Answer:**

**Factory pattern** is one of most used design pattern and comes under *creational* patterns category.

In Factory pattern, we create object without exposing the creation logic to the client and refer to newly created object using a *common interface*.

<div class="text-center">
<img src="https://www.tutorialspoint.com/design_pattern/images/factory_pattern_uml_diagram.jpg" class="img-fluid"/>
</div>

<br/>
**Pro's**:  

*   Allows you to hide implementation of an application seam (the core interfaces that make up your application)
*   Allows you to easily test the seam of an application (that is to mock/stub) certain parts of your application so you can build and test the other parts
*   Allows you to change the design of your application more readily, this is known as loose coupling

**Con's**  

*   Makes code more difficult to read as all of your code is behind an abstraction that may in turn hide abstractions.
*   Can be classed as an anti-pattern when it is incorrectly used, for example some people use it to wire up a whole application when using an IOC container, instead use Dependency Injection.

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q9: Can we create a clone of a singleton object? ⭐⭐

**Answer:**

Yesl, we can but the purpose of Singleton Object creation is to have single instance serving all requests. 

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q10: What is Builder pattern? ⭐⭐

**Answer:**

*Builder pattern* builds a complex object using simple objects and using a step by step approach. This builder is independent of other objects.


<div class="text-center"/>
<img src="https://www.plantuml.com/plantuml/svg/TOux3i8m343tdC9ZE_G234YqIAo86mJ7WqMQLeupS7kSqY90iCJsU_4dtpZDNlm8MU-Hx1L6BMDqHfMHPvyK_12PQio0d-B8GgYJL1M-UgQ4GafzuHXe-O5NvunvfPeYTDtU4jZ14sukh2gy6LXhcset5jIcTG6s_cN7sROVcXP-yVuF7oh75p-HNYYNQDCV" class="img-fluid" style="max-width: 500px" />
</div>

*The Director* class is optional and is used to make sure that the building steps are executed in the *right order* with the right data by the right builder. It's about validation and delegation.

Builder/Director pattern's steps invocations could be semantically presented by *method chaining* or so called *Fluent Interface* syntax. 

```js
Pizza pizza = new Pizza.Builder()
                       .cheese(true)
                       .pepperoni(true)
                       .bacon(true)
                       .build();
```

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q11: What is Filter pattern? ⭐⭐

**Answer:**

**Filter pattern** or **Criteria pattern** is a design pattern that enables developers to filter a set of objects using different criteria and chaining them in a decoupled way through logical operations. This type of design pattern comes under *structural* pattern as this pattern combines multiple criteria to obtain single criteria.

**Filter design pattern** is useful where you want to add filters dynamically or you are implementing multiple functionalities and most of them require different filter criteria to filter something. In that case instead of hard coding the filters inside the functionalities, you can create filter criteria and re-use it wherever required.

```js
List<Laptop> laptops = LaptopFactory.manufactureInBulk();
AndCriteria searchCriteria = new AndCriteria(
  new HardDisk250GBFilter(), 
  new MacintoshFilter(), 
  new I5ProcessorFilter());
List<Laptop> filteredLaptops = searchCriteria.meets(laptops);
```

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q12: What is Proxy pattern? ⭐⭐

**Answer:**

In **proxy pattern**, a class represents functionality of another class. This type of design pattern comes under _structural_ pattern.

In proxy pattern, we create object having original object to interface its functionality to outer world.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Proxy_pattern_diagram.svg/439px-Proxy_pattern_diagram.svg.png" class="img-fluid"/>
</div>

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q13: What is Iterator pattern? ⭐⭐

**Answer:**

**Iterator pattern** is very commonly used design pattern in Java and .Net programming environment. This pattern is used to get a way to access the elements of a collection object in sequential manner without any need to know its underlying representation. Iterator pattern falls under _behavioral_ pattern category.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/c/c5/W3sDesign_Iterator_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q14: What is State pattern? ⭐⭐

**Answer:**

In **State pattern** a class behavior changes based on its state. This type of design pattern comes under _behavior_ pattern. In State pattern, we create objects which represent various states and a context object whose behavior varies as its state object changes.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/W3sDesign_State_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q15: What is Null Object pattern? ⭐⭐

**Answer:**

In **Null Object pattern**, a null object replaces check of NULL object instance. Instead of putting if check for a null value, Null Object reflects a do nothing relationship. Such Null object can also be used to provide default behaviour in case data is not available.

In Null Object pattern, we create an abstract class specifying various operations to be done, concrete classes extending this class and a null object class providing do nothing implementation of this class and will be used seamlessly where we need to check null value.

<div class="text-center">
<img src="https://www.tutorialspoint.com/design_pattern/images/null_pattern_uml_diagram.jpg" class="img-fluid"/>
</div>


🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q16: What is Strategy pattern? ⭐⭐

**Answer:**

In **Strategy pattern**, a class behavior or its algorithm can be changed at run time. This type of design pattern comes under _behavior_ pattern.

In Strategy pattern, we create objects which represent various strategies and a context object whose behavior varies as per its strategy object. The strategy object changes the executing algorithm of the context object.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/4/45/W3sDesign_Strategy_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>



🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q17: What is Template pattern? ⭐⭐

**Answer:**

In **Template pattern**, an abstract class exposes defined way(s)/template(s) to execute its methods. Its subclasses can override the method implementation as per need but the invocation is to be in the same way as defined by an abstract class. This pattern comes under _behavior_ pattern category.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/W3sDesign_Template_Method_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

🔗 **Source:** [tutorialspoint.com](https://www.tutorialspoint.com/design_pattern/design_pattern_interview_questions.htm)


## Q18: What is Memento pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q19: What is Abstract Factory pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q20: What are the difference between a static class and a singleton class? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q21: What is Prototype pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q22: What is Adapter Pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q23: What is Bridge pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q24: When should I use composite design pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q25: What does “program to interfaces, not implementations” mean? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q26: What is Decorator pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q27: What is Facade pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q28: Can you give any good explanation what is the difference between Proxy and Decorator? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q29: What is the Chain of Responsibility pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q30: What is Command pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q31: What is Interpreter pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q32: What is Mediator pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q33: What is Observer pattern? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q34: How is Bridge pattern is different from Adapter pattern? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q35: When would you use the Builder Pattern? Why not just use a Factory Pattern? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q36: What is Flyweight pattern? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q37: Why would I ever use a Chain of Responsibility over a Decorator? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q38: Explain usage of Service Locator Pattern ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q39: What is the difference between Strategy design pattern and State design pattern? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q40: Explain what is Composition over inheritance? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q41: Explain difference between the Facade, Proxy, Adapter and Decorator design patterns? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q42: What's the difference between the Dependency Injection and Service Locator patterns? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q43: Could you explain the difference between Façade vs. Mediator? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q44: What is the difference between the template patterns and the strategy pattern? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**


## Q45: Could you explain what is the "deadly diamond of death"? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Design%20Patterns)**






