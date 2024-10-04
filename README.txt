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
Module is a place where you can group the components, directives, pipes amd services which are ralted to the application.
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
Starts with @ Sign

Structural Directive
Structural directive is responsible for adding and deleting html elements in the view.
Starts with * sign.

Attribute Directive
Attribute directive is responsible for changing the appearance of view by adding or removing styles/css classes of the html elements.
Set inside square brackets. []

Section 5 
23.What is Decorator?
Angular decorators store metadata about a class, method, or property.
Metadata is "data that provides information about other data".
All decorators are represented with @ symbol.

24. What are the types of Decorator?
4 types
Class Decorators Ex: @NgModule

Property Decorators Ex: @Input, @Output

Method Decorators Ex: HostListner

Parameter Decorators Ex: @Inject, @Self



25. What are Pipes? What are the types of Pipes & Parameterized Pipes?
Pipes are simple functions which accept an input value and return a transformed value.

                        Angular Pipes
            Build-in Pipe                   Custom Pipe

When we pass any parameters to the pipes, it is called Parameterized pipes.

26. What is Chaining Pipes?
The chaining pipes use multiple pipes on a data input.


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
 
34.  What are Lifecycle Hooks in Angular?
35. What is a Constructor in Angular?
36. What is ngOnInit life cycle hook in Angular?
37. What is the difference between constructor and ngOnInit?

Section 8 
38. What are Asynchronous operations?
 What is the difference between Promise and Observable?
 What is RxJS?
What is Observable? How to implement Observable
What is the role of HttpClient in Angular?

Section 9 
What is Typescript? Or What is the difference between Typescript and Javascript?
 What is the difference between let and var keyword?
What is Type annotation?
What are Built in/ Primitive and User-Defined/ Non-primitive Types in Typescript?
What is “any” type in Typescript?
What is Enum type in Typescript?
What is Type Assertion in Typescript?
What are Arrow Functions in Typescript?