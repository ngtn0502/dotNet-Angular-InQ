Stress-out note

NhanNguyen

some little note by myself to remind how much i suffered

---

# Things worth to review:

| No. | Content                                                               |
| --- | --------------------------------------------------------------------- |
|     |                                                                       |
| 1   | [Angular](#angular)                             |
| 2   | [dotNET](#dotnet)                             |

# Angular

# Difference Shadow DOM and virtual DOM ?

Shadow DOM is a technique using by Angular to enscapsulation the DOM Note - it mean every DOM element is encapsulated by ShadowDom Boundary - It help seperate DOM tree into multiple part - And we just need to updated which part should be updated
The styling or javascript code inside that shadow dom node can not effect to the parent in DOM tree - easy to naming css styling
=> Solve the enscapsulation issue
=> Solve a little performance issue

Virtual DOM is a technique using by ReactJS to increase the perforamance of Application - it create a snapshot of DOM tree - and update changes of our application to the snapshot - after that Virtual DOM will be compare to Original DOM - and just update which the different element
=> Solve the performance issue 

# Ng-container, ng-template ?

# Is it possible to apply multiple directives for an element ?

We canot use multiple structural directive in one element;

Becuase it will conflix and Angular will have no idea to do with this element - walkaround is use <ng-container> to wrap this element

# What are the differences between Angular and AngularJs ?

# What are the differences between Angular and ReactJs ?

# Angular page lifecycle ? Execution flow ?

When Angular create Component in run through couple of differnce phrases in this creation process - and it give us a change to hook into this process to execute some code.

Angular will call some method in each phrases / process.

# What is the Spread operator ?

# What is State Manament Angular?

State is a way we store data member in component in react or angular

There are several way to do state management in Angular

For Example:

    Service

    NgRx

# What's the difference of ASP.Net and .Net Core?

ASP.NET: is a framwork of .NET Core for building web-api

.NET Core: is a open-source platform for building many kind of allication, include web application

# What access modifiers exist in C#?

Public: mean that the type/member is available for all other code in the same assembly 

Private: mean that the type/member are only available in the same class

Protected: mean that the type/member are only available in the same class or in the class derived from this class 

Static: static class can not be instanciated ( cannot use `new operator` to create class) - we access the method of static class by calling class name itself

    ex: Console.Wriline()

# What design patterns and software principles have you worked with?

OOP principle

SOLID principle

Dependency Injection principle

Generic Repository pattern

Specificaiton pattern

Mediator patern

# What is singleton?

Singleton: our dependency will intanciated when our application start and remain/alive whole lifetime of our application

# What is a difference between string and stringbuilder? When would you use over the other?

String: string is immutable - it mean when we save a string in to variable - we save the actual value of string in memory.

> When we change string - it will create new place in memory rather than changing the actual value sit on memory

StringBuilder: is mutable

> When we change stringBuilder -  we change the actual value sit on memory

> StringBuilder helpful when we have to append or concat string, because it do not create new string in memory - do not cause memory leak.

# What memory leaks you are aware of in C#?

If we use string type, whenever we concat or append string, it will create new string variable in memory -> lead to memory leak 

Keeping database connections or result sets open when they are not used. Remember to call Dispose() on all IDisposable objects. Use the using statement.

# What's the purpose of garbage collector?

GC help us to manage memory automatically

- Allocate object on memory heap rather than stack

- Clean variable when it no longer in use -> release memory

# How do you handle errors in C#?

```
try {

}
catch {

}
```
# What is Interceptor?

in Angular, interceptor is a special services . We use to Interceptor to intercep into every HTTP Request and HTTP Respone 

Normally, we use our information into our HTTP headers of HTTP Request or modify/format HTTP Response information before returning services

# What is Reactive Programing?

Reactive Programing is asynchronous data-stream programming

In reactive programing, we use Observable to control data-stream, observable will emit the data for every changes of the state, observer will receive notification if they subscribe to an observable

# What is RxJs?

RxJs is library for reactive programming;

RxJS provide some classes and operator for 


---

---

# dotNET

# How long have you work with .Net Framework ?

I have some previous experience working with .Net Framework, it may around 6 months

# What is the difference between .Net Framework and .Net Core ?

Both: is a free, open-source platform to create web app, web api, mobile app, desktop app...

.Net Framework is a previous version of .Net core

.Net framework:

    Only support in Window 

.Net Core:

    Lightweight, fast.

    Support is cross-platform framework, support in Window, macOS, Linux
    
    Add more features to .Net Framework

> When .Net Framework only support for window, .Net core is new version, so it add some new features, support cross-platform ( window, macos, linux) and also lightweight and fast

# Why we have to use .Net Core ?

> .NET Core support cross-platform

> Lightweight, fast, better perforamance

> Well support for cloud computing eviroment

# What is the Entity Framework ?

Entity Framework is an ORM framework - allow us to work with relational database in Object-oriented programing

ORM (Object-Relational Mapping): is a technique for storing, retrieving, updating and deleting relational database by oriented program

In ORM: 

    it create relational tables based on classes/object - and it called code first

    it create classes/object based on relational table - and it called called database first

It utilizes a "data layer access" to do the translation between Oject-oriented code and relation database table

# Please describe about Asp.Net MVC architecture ?

MVC stand for Model-View-Controller architecture - it help seperate Data access logic part and presentation part of our application

M - Model: the only place responsible for handling data logic, access to database

C - Controller: act like middle man between Model and View - Responsble for taking request from client - pass the request to Model - recive respond data from Model - pass that respond data to View - recive HTML/CSS code from View and sent it back to client

V - View: the only place responsible for taking data from controller - create dynamic data template 

When client request for a web page -> controller will take that request and call the model to retrieve data -> and model will send back the data to controller -> after that controller will sent the data to view -> view will responsible for create HTML code base on the set of this data and sent the HTML code back to controller -> in the end controller will sent the respond to the browser or client

# How can we pass data from Controller to View in Asp.Net MVC?



# How can we pass data from this Controller to another Controller ?



# What is the session in Asp.Net MVC ?



# Have you worked with Unit Test ?

Yes, i have some experiences working with Unit Test

ussually i use Nunit for writing Unit Test for .NET Core, C# application

There are 3 section of Unit Testing: 

    Arrange: where we put all testing data and arrange value we going to use

    Act: where we do actual calculation

    Asert: where we assert something about actual value in Act

# What is the LinQ ?

LinQ is stand for Language Interged Query

> When we fetch data from difference type of data sources, it return multiple kind of datasources -> we need a way to query multiple type of data without knowing what kind of data and the specific syntax

> It enable us to query any type of datasources like sql server, object, list,...

> Allow us to work with difference type of datasources using a similar code style without worries about what kind of this datasources

For Example: 

When we write LinQ query for data comefrom SQL Server database, LinQ Provider will convert LinQ Query to T-SQL Query to do the query in SQL Server Database

# What is Lambda Expression ?

Lambda expression is an anonymoust funciton ( with equal and greater than symbol) - lambda expression is divide into two part left hand side is an input parameters and right hand side is an expression 

> We usually pass the lambda expression into LinQ Query to do the expression of that query

# What is Filter Action is Asp.Net MVC ? ***

`In Controller` - every method is called action method.

Filter Action is an attribute that can applied either on controller aciton method or on a controller, when they are applied in controller - they will be applied for all the aciton method in controller.

> It allow us to run custom code before executing action method

For Example: 

    ValidationInput

    Authorize

    AllowAnonymous

# What is the validation attributes in Asp.Net ?

it is an attributes allow us to specify valiation rules for our class or model properties.

For Example: 

    [Required] Attribute

    [StringLength(100)] Attribute


# What is the middleware in Asp.Net Core ?

Middleware is a pices of software that has access to incoming request and outgoing respond.

Middleware can decide to perform some work after pass the request into next middleware 

For Example:

    Middleware for authenticaiton

    Middleware for handling error

# What is the Dependency Injection in Asp.Net Core ?

It is the way we inject the dependency interface of one class in constructure parameter of other class

And we have to use the help of ASP.NET to register this dependency in ConfigureServices method of Startup.cs class

services.AddSingleton(<IDependency>, Dependency)

> Transient: the services will be instantiate every time we request it

> Scoped: the services will be instantiate and create its scope. Within this scope, it reuses the existing services. Services will be destroy if no one using or reference to it

> Singleton: the services will be instantiate and remain with lifetime of application, and we can use it every where

# What are the Service LifeTimes in Asp.Net Core ?



# What is the asynchronous programming in .Net ?

In C#, we use async-await and Task object to perform asynchronous task - and it follow [Task-based Asynchronous Pattern](https://docs.microsoft.com/en-us/dotnet/standard/asynchronous-programming-patterns/task-based-asynchronous-pattern-tap)

We await to the method that take time or services response for calling external api, it will run in the background and does not affect main thread of out application

# Code first, model fist, database first ?

It is way of approach we use in Entity Framework

> Code frist: means we write .NET Class, entity framework will convert this class into entity of database - control database by code

> Database first: means EF will creates model and class for us based on the existing database

> Model first: means we draw the models first by EF Designer tool and EF will take care about creating database for us

# Controller Action return types in Asp.Net Core ? - [Articles](https://www.c-sharpcorner.com/article/
3-ways-to-return-the-data-from-controller-action-method-in-asp-net-core/)

Return IActionResult Type

Benefit:
> It allow to return multiple type of data along with the status code, this is very important in RESTful API

Drawback:
> Have to define type of data for swagger.

```
[Route("emplpyees/{id}")]
[ProducesResponseType(StatusCodes.Status201Created, Type = typeof(Employee))]  
[ProducesResponseType(StatusCodes.Status400BadRequest, Type = typeof(Employee))]  
public IActionResult GetEmployeeById(int id)  
{  
    if (id == 0)  
    {  
        return NotFound();  
    }  
    var employee = new Employee() { Id = 1, Name = "Nitish" }; // Get the data from db  
    return Ok(employee);  
}  
```

Return ActionResult<T>

Benefit
> It allow to return multiple type of data along with the status code, this is very important in RESTful API, does not need to defiend type of data for swagger

[Route("emplpyees/{id}")]  
[ProducesResponseType(StatusCodes.Status201Created)]  
[ProducesResponseType(StatusCodes.Status400BadRequest)]  
public ActionResult<Employee> GetEmployeeById(int id)  
{  
    if (id == 0)  
    {  
        return NotFound();  
    }  
    var employee = new Employee() { Id = 1, Name = "Nitish" }; // Get the data from db  
    return employee;  
}  

# There are two methods , method1 allows user1 access, method2 allows user2 access. How can we implement that feature ?



# Exception handling in Asp.Net Core ?



# How to define routing in Asp.net Core ?



# Is it possible to keep the same name of action methods ?



# How can you handle exception in .Net ?



# What is RestFul API ?



# What are the differences between methods GET/POST/PUT/DELTE/PATCH ?



# How can we protect Api ?



# Stack and Heap ?



# String is reference type or value type ?



# Can you tell about your experience in Unit Test / Integration Test ?



# What is the Model Binding in Asp.Net ?



# Model binding / Parameter binding types in Asp.Net Core ? FromBody / FromForm / FromQuery / FromRoute / FromHeader



# Difference between Ienumrable and Iqueryable ?



# How can we handle exception in Asp.Net Core ?



# Have you ever analyze and design an application from by your-self ?



# Can you explain about keyword async/await ?



# What is the difference between Task and Thread ?



# What is reflection technique in .Net ?



# What is the memory leak ?



# What tools we can monitor/diagnostic memory leak in Visual Studio ?



# How can we optimize performance for Asp.Net application ?



# Access modifiers in .Net ?



# Difference between reference type and value type ?



# Difference string and stringbuilder ?



# OOP properties ?



# What is inheritance property in OOP ?



# What is encapsulation in OOP ?



# What is abstraction property in OOP ?



# What is polymorphism property in OOP ?



# Do you know any design pattern ?



# What is Singleton design pattern ?



# What is Factory Method design pattern ?



# What is SOLID ?



# What is KISS principle ?



