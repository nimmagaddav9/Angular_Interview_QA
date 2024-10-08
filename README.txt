1. What is Angular? Why? Client-side structuring
Angular is a component-based framework for building structured, scalable(open and flexible) and single page web applications for client side.
SPA: Loading 1 component to another component without refreshing the whole project.

2. What are Angular advantages? building SPA.
It is Relatively simple to build Single Page Applications(Components).
To make flexible and structured applications(OOPS friendly)
It is Cross platform and Open Source(Free)
Reusable Code(Services)
Testability(Unit testing spec.ts file)

3. What is the difference between AngularJS and Angular?
Google Angular JS 2010 --> Angular 2, 4,

Angular JS                                    Angular
1. It only supports JavaScript.           1. It supports both JavaScript and Typescript.
2. This framework has MVC architecture.   2. This framework has a component based architecture.
3. It does not have CLI tool.             3. It has CLI Tool.
4. It does not use Dependency Injection.  4. It uses Dependency Injection.
5. It does not support mobile browsers.   5. It also support mobile browsers.
6. It is not so fast.                     6. It is very fast(Data binding and Component based architecture).

4. What is NPM?
Node Package Manager. Node.js --> NPM. google developed Node and Angular.
NPM/Node Package Manager is a Online repository from where you can get thousands of free libraries which can be used in your angular project.
The node_modules folder is used to save all downloaded packages from npm in your computer.


5. What is CLI tool?
CLI is command-line interface tool that you use to initialize and develop Angular applications.
Ex: ng generate component TestComponent

Components & Modules

6. What are Components in Angular?
Components are the most basic UI building block of an Angular app.
Ex: Inside src --> app --> app.component.css(CSS code), app.component.html(html template), app.component.spec.ts(Unit tests), app.component.ts(link css, html)

7. What is a Selector and Template?
A selector is used to identify each component uniquely into the component tree.
A template is a HTML view of an Angular component.

8. What is Module in Angular? What is app.module.ts file?
Module is a place where you can group the components, directives, pipes amd services which are related to the application.
app.module.ts file --> Root module.
@NgModule({
    declarations:[
        AppComponent
    ],
    imports:[
        BrowserModule,
        AppRountingModule
    ],
    providers[],
    bootstrap:[AppComponent]
})

9. How an Angular App gets Loaded and Started? What are index.html, app-root, selector and main.ts?
index.html --> Main.ts --> app.module.ts(bootstrap) --> App-component(bootstrap).
Angular is used to create Single Page Applications. 
index.html file is that single page.
index.html will invoke main.js file which is the JavaScript version of main.ts file.

main.ts file is like the entry point of web-app.
It compiles the web-apps and bootstraps the AppModule to run in the browser.

App module file will then bootstrap the Appcomponent.

App-component or app-root component is the html which you will see finally.


10. What is a Bootstrapped Module & Bootstrapped Component?
When the Angular Web application will start then the first module launched is the bootstrapped module and same is true for the bootstrapped component also.

Data Binding

11. What is Data Binding in Angular?
Data binding is the way to communicate between your typescript code of your component and your html view.
TypeScript Code(app.component.ts)        -------->      HTML Template(app.component.html)view
                                    String Interpolation, Property Binding, Event Binding, 2-way data binding.

12. What is String Interpolation in Angular?
String Interpolation is a one-way data binding technique that is used to transfer the data from TypeScript code(Component) to an HTML template(view).

String Interpolation can work on string type only not numbers or any other type.
It is represented inside{{data}} double curly braces.


13. What is Property Binding in Angular?
Property Binding is a superset of interpolation. It can do whatever interpolation can do.
In addition, it can set an element property to a non-string data value like Boolean.

14. What is Event Binding in Angular?
Event Binding is used to handle the events raised by the user actions like button click.
Ex: Submit button.

15. What is Two way Binding in Angular? combination of Property Binding and Event Binding.
Two-way data binding in Angular will help users to exchange data from the view to component and then from component to the view at the same time.

Section 4 
16. What are Directives? What are the type of directives?
Directives are classes that add additional behavior to elements in your Angular applications.
                        Types of directives
                Structural              Attribute          Component
                *ngIf                   [ngClass]           
                *ngFor                  [ngStyle]
                *ngSwitch

Structural directives change appearance of DOM by adding or removing elements.
Attribute directives change the appearance or behavior of an element.
Component directive are directives with its own template.

17. What is *ngIf Structural directive?
Structural Directives are classes that change appearance of DOM by adding or removing elements.
ngIf Directive is used to add or remove items based on the if condition.

18. What is *ngFor Structural directive?
The *ngFor directive is used to iterate a list of items and then display them.

19. What is *ngSwitch Structural directive?
ngSwitch is an Structural directive used in combination with *ngSwitchCase and *ngSwitchDefault that are both structural directives.

20. What is [ngStyle] Attribute directive?
Attribute directives change the appearance or behavior of an element.
ngStyle is an Attribute directive that updates styles for the HTML element.


21. What is [ngClass] Attribute directive?
ngClass directive adds and removes CSS Classes on an HTML element.

22. What is the difference between Component, Attribute and Structural Directives?

Component Directive
Component Directive is responsible for showing the first whole view. It is the mosed used one.
Starts with @ Sign.
Like: @Component

Structural Directive
Structural directive is responsible for adding and deleting html elements in the view.
Starts with * sign.
Like: *ngIf, *ngFor, *ngSwitch

Attribute Directive
Attribute directive is responsible for changing the appearance of view by adding or removing styles/css classes of the html elements.
Set inside square brackets. []
Like: [ngClass], [ngStyle]

Section 5 Decorator & Pipes

23.What is Decorator?
Angular decorators store metadata about a class, method, or property.
Metadata is "data that provides information about other data".
All decorators are represented with @ symbol.

24. What are the types of Decorator?
4 types
Class Decorators Ex: @NgModule, @Component

Property Decorators Ex: @Input, @Output

Method Decorators Ex: HostListner

Parameter Decorators Ex: @Inject, @Self


25. What are Pipes? What are the types of Pipes & Parameterized Pipes?
Pipes are simple functions which accept an input value and return a transformed value.

                        Angular Pipes
            Build-in Pipe                   Custom Pipe
lower-case, upper-case (conversion)
When we pass any parameters to the pipes, it is called Parameterized pipes.

26. What is Chaining Pipes?
The chaining pipes use multiple pipes on a data input. Ex: {{dob | date | uppercase}}


Section 6
27. Explain Services with Example?
A service is a typescript class and a reusable code which can be used in multiple components.
Service can be implemented with the help of Dependency Injection.

Ex: LoginComponent       MenuComponent

ErrorLoggingService

28. How to create Service in Angular? App/login/Menu Component
open terminal --> ng generate service

29. How to use Dependency Injector with Services in Angular? 3 step process.
    Register the service.
    Create the new property and assign the Service type.
    this.loggingService.logError(); 

30. What is Hierarchical Dependency Injection? Parent --> Child


31. What is Provider in  Angular?
A provider is an object declared inside the decorators which inform Angular that a particular service is available for injecting inside the components.


32. What is the role of @Injectable Decorator in a Service? How to use one service inside another service?
With @Injectable decorator one service can be used by another service.


Section 7 -Lifecycle Hooks
33. What are Parent-Child Components?
Suppose Parent Component with input field, button.
create ng g c child
ng serve
 
34.  What are Lifecycle Hooks in Angular?
A component from creation to destruction goes through several stages and these stages are life cycle hooks.
The Stages will cover activities like:
    1. Component instantiating.
    2. Rendering the component html view.
    3. Creating the Child Components(if required).
    4. Destroying the component.

constructor: It is a default method of the typescript class that is executed when the class is instantiated. 
It always run before any angular hook and it is not part of lifecycle hooks.

ngOnChanges : called when input property changes.

ngOnInit: called when the component is created.

ngDoCheck : if changes not detected then it is called.

ngAfterContentInit
ngAfterContentChecked
ngAfterViewInit
ngAfterViewChecked  ---> 4 of them are called for component children.

ngOnDestroy: called when the component is destroyed.


35. What is a Constructor in Angular?
The Constructor is a method in a Typescript class that automatically gets called when the class is being instantiated.
Constructor always run before any angular hook and it is not part of Lifecycle Hooks.
Constructor is widely used to inject dependencies(services) into the component class.

Syntax: 
export class SampleComponent implements onInit {
    constructor(){
        console.log("inside constructor");
    }
        ngOnInit():void{
            console.log("Inside ngOnInit");
        }
    }


36. What is ngOnInit life cycle hook in Angular?
1. NgOnInit signals the activation of the created component.
2. This is the second hook and called after ngOnChanges.
3. NgOnint called only once during lifecyle.
4. By default, present in the component.

37. What is the difference between constructor and ngOnInit?
ngOnInit                                                
1. NgOnInit is an Angular Lifecycle hook which signals the activation of the created component.
2. ngOnInit is called after ngOnChanges lifecycle-hook.
3. When ngOnInit called, everything about component is already ready, so it's use is to perform most of the business logic on component.

Constructor
1. The Constructor is a method in a TypeScript class, that automatically gets called when the class is being instantiated.
2. Constructor is called before any lifecycle-hook.
3. When Constructor called, everything in component is not ready, so it's mostly used for injecting dependencies only.


Section 8 Observable/ HttpClient/RxJS

38. What are Asynchronous operations?
Observables are used to perfrom Asynchronous operations and handle asynchronous data.
4Tasks run at same time.


39. What is the difference between Promise and Observable?
Observables
1. Emit multiple values over a period of time. also called streaming of data.
2. Are lazy: they're not executed until we subscribe to them using the subscribe() method.
3. Have subscriptions that are cancellable using the unSubscribe() method.

Promise
1. Emit a single value at a time.
2. Are not lazy: execute immediately after creation.
3. Are not cancellable.

40. What is RxJS?
RxJS is a library for composing asynchronous and event-based programs by using observable sequences.
RxJS is a JavaScript library, that allow us to work with asynchronous data stream with the help of Observables.
Observables introduced by RxJS Library.
RxJS stands for Reactive Extensions for JavaScript.

41. What is Observable? How to implement Observable
Observables are used to stream data to multiple components.
It's a 3 step process:
1. Import Observable from RxJS Library.
2. Create Observable & Emit Data.
3. Finally subscribe the Data.

42. What is the role of HttpClient in Angular?
HttpClient is a built-in service class available in Angular.
@angular/common/http package.
Performs HTTP requests.

Section 9 
43. What is Typescript? Or What is the difference between Typescript and Javascript?
1. Tyescript is a strongly typed language. Ex: let someValue: string="test message";
2. Tyescript is a superset of JavaScript.
3. It has Object oriented features.
4. Detect error at compile time.

44. What is the difference between let and var keyword?
Var has global scope inside function.
let keyword scope is limited to the block only, from where it is declared.

45. What is Type annotation?
Definition: Type annotation is assigning a variable or object.
a type which will show the compile time error,
if we will try to assign the variable a different type.

46. What are Built in/ Primitive and User-Defined/ Non-primitive Types in Typescript?
Built-in Data types are used to store simple data.
User-Defined Types are used to store complex data.

47. What is “any” type in Typescript?
Definition - When a value is of type any,
then no typechecking will be done by compiler and
the flexibility is there to do anything with the variable.

48. What is Enum type in Typescript?
Definition - Enums allows to define a set of named constants.

49. What is Type Assertion in Typescript?
Definition: Type assertion is a technique that informs the compiler about the type of a variable.

50. What are Arrow Functions in Typescript?
Arrow functions are the shorthand Syntax
for defining the anonymous function


=============================================================================================

Angular IQ
 
1. What is CSS Float Property?
The float property specifies how an element should float.
 
2. What is CSS Position?
The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky).
 
3. HTML5 Semantic Web?
A semantic element clearly describes its meaning to both the browser and the developer.
Examples of non-semantic elements: <div> and <span> - Tells nothing about its content.
Examples of semantic elements: <form>, <table>, and <article> - Clearly defines its content.
 
4. Difference b/w local storage and session storage
Session storage is temporary which exists as long as the current window is opened and data gets lost when window 
is closed, where as Local Storage is persistant and remains intact across sessions unless anyone deletes it.
 
5.What is Javascript function?
Functions are one of the fundamental building blocks in JavaScript.
Particular business logic called as function. 
 
6.What is the scope of the variable?
Scope determines the accessibility (visibility) of variables.
 
In JavaScript there are two types of scope:
 
Local scope
Global scope
JavaScript has function scope: Each function creates a new scope.
 
Scope determines the accessibility (visibility) of these variables.
 
Variables defined inside a function are not accessible (visible) from outside the function.
 
7. What is Callback, closure?
Passing "one function" to "another function" as an argument called as "CallBack".
if any inner function accessing the outer function data, then such scenario called as closure.
 
 
8.explain crud operations in angular?
CRUD operations in Angular refer to the four basic functions for managing data: Create, Read, Update, and Delete.
Create
Creating new data involves sending a POST request to the server API. In Angular, this is typically done using the HttpClient service.


9.why we use bootstrap? explain some bootstrap class?
Bootstrap is a framework to help you design websites faster and easier. 
It includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, 
modals, image carousels, etc. It also gives you support for JavaScript plugins.  
 
10.explain directives
To enhance view capabilities or view features we go for directives. 
Types of Directives – 2 types 
Predefined Directives --- Directives given by the Angular framework 
Custom Directives --- Directives developed by users
 
11.explain routing?  Navigating from 1 component to another component is called routing. 
 
12.Events in HTMl?
HTML has the ability to let events trigger actions in a browser, like starting a JavaScript when a user clicks on an element.
 
 
13.differnce between display:block and visibility hidden?
display:none will hide the element and collapse the space is was taking up, 
whereas visibility:hidden will hide the element and preserve the elements space.
 
14.difference between var, let, const keyword?
 
                             var                                         let 
 
    1) ES1                                                          1) ES6 
    2) duplicate variables allowed                                  2) duplicate variables not allowed 
    3) won't obey scope rule                                        3) obeys scope rule 
    4) global polluting issue raised                                4) we can overcome global polluting issue
    5) variable hoisting raised                                     5) we can overcome variable hoisting  
    6) var keyword is the global scope                              6) let keyword is the block scoped member 
       member 
//const keyword 
 
//const keyword used to declare the variables 
 
//const keyword introduced in "ES6" 
 
//in const keyword "reinitialization" not possible 
  
15.types of Binding in angular?
There are four different types of ways through which we can do data bindings in Angular 2 namely 
event binding, 
unidirectional binding (i.e. one-way binding), 
bi-directional binding (i.e. two-way binding), 
and the interpolation.
 
 
16.Lifecycle hooks in Angular?
 
ngOnChanges: Called every time a data-bound input property changes. 
It’s called a first time before the ngOnInit hook. The hook receives a SimpleChanges object that contains the previous and current values for the data-bound inputs properties. This hook gets called often, so it’s a good idea to limit the amount of processing it does.
 
ngOnInit: Called once upon initialization of the component.
 
ngDoCheck: Use this hook instead of ngOnChanges for changes that Angular doesn’t detect. It gets called at every change detection cycle, so keeping what it does to a minimum is important for performance.
 
ngAfterContentInit: Called after content is projected in the component.
 
ngAfterContentChecked: Called after the projected content is checked.
 
ngAfterViewInit: Called after a component’s view or child view is initialized.
 
ngAfterViewChecked: Called after a component’s view or child view is checked.
 
ngOnDestroy: Called once when the component is destroyed and a good hook to use to cleanup and unsubscribe from observables.
 
 
 
17.differnce between promise and observable?
 
Promises Establishes the communication between "producer" and "consumer". 
       - Promises also called as "special javascript objects". 
       - we will create Promises by using "Promise" class constructor. 
        - Promises have 3 states 
            1) success  (resolve) 
            2) error    (reject) 
            3) pending 
          - we will consume promises by using "then()" 
 
a Promise is always asynchronous,
while an Observable can be either synchronous or asynchronous,
a Promise can provide a single value,
whereas an Observable is a stream of values (from 0 to multiple values), 
you can apply RxJS operators to an Observable to get a new tailored stream
 
=====================================================================================================

What is | ? 
In JavaScript, the | symbol is primarily used as the bitwise OR operator.
Pipes in Angular are a way to transform data in your template
they are simple functions that accept an input value and return a transformed value. 
Pipes are used in template expressions to modify the way data is displayed.

What is arrow function ?   Arrow functions acts like "callbacks" to receive the response from server.

React                                           Angular
Architecture: only the View of MVC              Complete MVC
Rendering: Server Side Rendering                Client-side rendering
DOM: use Virtual DOM                            uses Real DOM
Data Binding: 1-way data binding                2-way data binding
Debugging: Compile-time Debugging               Runtime debugging
Author: Facebook                                Google