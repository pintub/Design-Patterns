##### Template Method Pattern
- **Naming** `Template=Skeleton of a algorithm with overridable intermediate Steps`
- **When To Use**
    - When you have algorithm with a Step which invokes sequence of other steps (let's call it parentStep and should be final)
    , few steps are overridable in different classes (concreteStep)
    , few steps should be overridable in different classes (abstractStep),
    Use TEMPLATE METHOD Pattern.
- **Brute Force Programming**
    - Multiple class with redundant coding for repeated steps 
- **Intuitive Example**
    - Building House with buildHouse() Step(final method defining sequence of otherSteps , yes self-use , But no use as this method is final ) ,  abstract steps , and concrete Steps
- **UML**
    - [UML](UML.puml)
- [**Code Example**](https://www.journaldev.com/1763/template-method-design-pattern-in-java#template-method-abstract-class)
- **Pros** 
    - Code Re-usability achieved because of inheritance
- **Cons**
    - ???
- **Comparision with Other Patterns**
- **Additional Note**
    - [Discussed in Effective Java Item-20, Combination of Interface + Abstract class is preferred , as >Java8 Interface can have default method implementation](https://github.com/pintub/EffectiveJava-Summary/blob/master/EffectiveJavaSummary/ClassesAndInterfaces.todo) . If abstract class not required , can be avoided and Interface alone can be used. Need of Abstract Class is only when state field, private methods or Object class method implementation is required. In-case of private method step , we can't use Interface (Check the Code-example fot that) 