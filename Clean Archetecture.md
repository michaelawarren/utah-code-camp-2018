# Clean Architecture
Why dirty architecture
* requirements
* model the domains and culture
* quick and dirty
* later never arrives
based off uncle bobs book heavy 
## programming paradigms
### structured programming
### object oriented programming
### functional programming
* mix of paradigms causes issues
* solid principles
## Components
### Component Cohesion principle
#### Reuse/Release Equivalence Principle
* You wouldn't release only part of a logging module
#### Common Closure principle
* don't break existing behavior
#### Component Reuse Principle
* but like things together
#### tension diagram
### Acyclic dependencies principles
* no cycles
### stable dependencies principle
* you can measure your dependencies
### Stable Abstract principle
* a component should be as abstract as it is stable
## What is architecture
* Design vs Architecture
* The shape of a software system.
* the shape is the division of that system into components
* how components communicate with each other.
### purpose
* minimize lifetime cost and maximize programmer productivity
    * deployment
    * development
    * operation
    * maintenance
## Good architecture
* support use cases
    * remember the importance of behaviors
    * start with the behavior not the database
* operation
* development
    * conways law
* deployment
    * bring ops in at the beginning
    * roll back plans
* leaves options open
* decoupled the components
    * break coupling from database
## boundaries
* find your seams
* depend on interface
* break business rules out of the gui
## Clean architecture
* onion picture
* Entities (enterprise business rules)(most stable)
* use cases (application business rules)
* interface adapters
* frameworks and drivers (least stable)
### enterprise business rule -> crosses multiple domains
* customer vs invoicing
* security?
## Details
* database is a detail.

speakerdeck.com/craigber