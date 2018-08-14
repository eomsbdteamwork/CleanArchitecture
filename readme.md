## Base elements(annotation) of Dagger2

This [link1](https://android.jlelse.eu/dagger-2-part-i-basic-principles-graph-dependencies-scopes-3dfd032ccd82) and [link2](https://proandroiddev.com/dagger-2-part-ii-custom-scopes-component-dependencies-subcomponents-697c1fa1cfc)is best example for understanding Dagger2 

Base elements (annotations) of Dagger 2

**@Inject** — base annotation whereby the “dependency is requested”

**@Module** — classes which methods “provide dependencies”

**@Provide ** — methods inside @Module, which “tell Dagger how we want to build and present a dependency“

**@Component** — bridge between @Inject and @Module

**@Scope** — enables to create global and local singletons

**@Qualifier** — if different objects of the same type are necessary



## Custom Scope annotation

Below you can see some features of the scope annotations:

- Usually the scope annotations are set for the Component and provide method.

- **If at least one provide method has a scope annotation the Component should have the same scope annotation.**

- The Component can be unscoped only if all provide methods in all its modules are unscoped too.


- All scope annotations for one component (for all modules with provide methods to be a part of Component and for the Component itself) should be the same.


## Component dependencies

Let’s denote Component dependencies traits right away:
   
- Two dependent components cannot have the same Scope. 

## Clean Architecture
This project has divided into 2 different layer
- presentation
- data

Currently we don't focus on *domain* layer.

### UML Diagram
![presentation](https://github.com/anjandebnath/CleanArchitecture/blob/master/uml/UML1.PNG) layer
