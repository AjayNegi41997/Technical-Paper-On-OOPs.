# Object-Oriented Programming In Java

First of all, we need to know “what does object orientation means?”, we will deal with the programming part later. The object orientation stands for seeing the world as a collection of objects.

## 5 Rules of Object Orientation

1. The whole world is a collection of objects.
2. No object is a useless object. Every object is a useful object.
3. Every object is in constant interaction with each other. The objects are not in isolation.
4. Every object belongs to a type, that type we technically called as a class. A class is a blueprint it doesn't exist in reality, what exists, in reality, are the objects.
5. Every object has some properties and does some behavior.
   
So, when we add the programming part, it means that the developer has to code his program in such a way that it follows all the rules of Object orientation which are stated above. To be precise Object-oriented programming is one of the software design methodologies that helps to make software efficient. In other words, OOP helps a programmer to write a program in such a way that it executes faster and uses memory efficiently.

## Four major blocks of Object-Oriented Programming.

#### Inheritance:

Inheritance refers to writing a program as a hierarchy of classes. Inheritance brings profit to the company as it promotes code reusability and also reduces coding time. Let's understand it by taking an example. First, we will take the example of a scenario where inheritance is not used and then the inheritance one.

### Non-Inheritance

Let's assume that there is a company that has been given a project to make such software which saves the following information of Cricketers along with their tag:- Name, DOB, Weight, Height, runs, catches, strikes. Now assume that they took 6 months to complete this project ( Crazy! right 😆). Now another client came to this company with a request to make a software to save the following information of the footballers along with the tag:- Name, DOB, Weight, Height, Goals, Fouls, Position. They took 6 months to make this software also.

![](https://i.ibb.co/NyNtT5z/1-KFVe-Bmitlsa-XWES-js0-IMw.png)

Did you notice that both of these classes have a lot of information in common(name, dob, weight, height). But they had to code for it all over again for the same thing. This problem can be solved by using Inheritance.

### Using Inheritance

Using inheritance we can use the resources of other classes by using the “extend” keyword. If the above company had used inheritance, they could have saved a lot of time. They should have to make a class which only saves personal details as everyone’s personal detail includes the tag name, dob, weight, height and have the cricketer and football class inherit from it.

![](https://i.ibb.co/B6jBhDr/1-t-VCEubcn-Fmaiou-Mc-Me-P7-Hw.png)

## Encapsulation

Encapsulation refers to the process of providing controlled access to the most important component of an object. For example, an ATM only gives you access to all the details of your account which can be achieved by inserting the card in the machine and entering the 4 digit pin. Similarly, encapsulation can be achieved by using private members, setters, and getters. Let's make a program to hide the details of your dog as you are very possessive of your dog 😵.

    Class Dog{
    private String name;
    private String colour;
    private String cost;
    void setData(String x,String y,int z){
           name=x;
           color=y;
           cost=z;
         }
    String getName(){
            return name;
        }
    String getColour(){
            return colour;
        }
    int getCost{
            return cost;
        }
    }
    Class launch{
    public static void main(String args[]){
        Dog dog=new Dog();
        dog.setData("Rocky","Pink",100000)
        System.out.println(dog.getName());
        System.out.println(dog.getColour());
        System.out.println(dog.getCost());
    }
    }

## Abstraction

Abstract methods are such methods for which the body is not available. Well, we use abstraction to hide the unnecessary details from the user. For example, you are using a mobile or laptop to read this blog, but you are only familiar with its interface, you don’t know what mechanism is going on inside your device.

We can have abstract methods, abstract classes but we cannot have abstract variables. Even if one method in the class is abstract, we should declare the class as abstract.

Rules for Abstraction:

* An abstract class can have all the methods as abstract.
* An abstract method can have few methods as abstract and few methods as concrete.
* A concrete class cannot have any abstract methods.
* We cannot create the object of an abstract class.
* An abstract class and an abstract method cannot be final. An abstract class cannot be final because no class would be able to inherit the abstract class. An abstract method cannot be final because nobody would be able to override the method. In other words, nobody can give the body for that method.
* A constructor can not be abstract because in every constructor we will compulsorily have either a super() method or this() method call.

## Polymorphism

Polymorphism is the property of an object which allows it to take multiple forms. The best example of this is yourself: you are a son/daughter, friend, student, employee, sportsman, etc.

### Types of Polymorphism

1. Compile-Time
2. Run Time
   
### Compile-time Polymorphism:

Compile-time polymorphism or Static polymorphism is resolved during compile time. Overloading is an example of this. This compiler will ensure which method will be executed for which function call.

> Method overloading refers to a virtual polymorphism because a programmer gets an illusion that one method is doing multiple job, which is not true, in reality one method will do only one job.

#### Rules for overloading

1. Overloaded methods must have different argument lists.
2. It can have different return types if the argument list is different.
3. I can throw different exceptions
4. It can have different access modifiers.

### Run time Polymorphism:

Run time polymorphism or Dynamic polymorphism is resolved during run time. Method overriding is an example of this.

>Overridden methods are such methods which are inherited from the parent class into the child class and are modified by the child class to suit its requirement.

#### Rules for overriding
1. The Overriding method argument list must match the overridden method
2. The return type must be the same or subtype of the overridden method.
3. Access level cannot be more restricted than the overridden method.


        
        Class plane{
            void fly(){
                System.out.println("Plane is flying");
            }
        }
        Class cargoPlane extends plane{
            @Override
            void fly{
                System.out.println("Plane is flying low");
            }
        }

## Conclusion

OOP is the backbone of Java. If you understand this concept properly you will be able to write your code efficiently and neatly.

## References

* Herbert Schildt, 2014. Java The Complete Reference, 9th Edition. [Click to read online](https://learning.oreilly.com/library/view/java-the-complete/9780071808552/)
* [JavaTPoint](https://www.javatpoint.com/java-oops-concepts)   

