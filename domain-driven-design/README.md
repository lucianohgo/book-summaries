# Domain-Driven Design

Book Author: *Eric Evans*

## Preface

### The Challenge of complexity

When complexity gets out of hand, developers can no longer understand the
software well enough to change or extend it quickly and safely. On the other
hand, **a good design can create opportunities to exploit those complex
features**.

A successful design must systematically deal with the domain itself, the
activity or business of the user.

The premise of this book is twofold:

1. For most software projects, the primary focus should be on the domain and
   domain logic
2. Complex domain designs should be based on a model

### Design versus development process

Design and process are inextricable. Design concepts must be implemented
successfully, or else they will dry up into academic discussion.

This book assumes that a couple of practices are in place on the project:

1. *Development is iterative*
2. *Developers and domain experts have a close relationship*

Agile development practices put an admirable effort into communication and
improving the project's ability to change course rapidly. With that ability to
react, developers can use the "simplest thing that could work" at any stage of a
project and then continuously refactor, making many small design improvements,
ultimately arriving at a design that fits the customer's true needs.

Unfortunately, some of these process ideas can be misinterpreted. Each person
has a definition of "simplest." Continuous refactoring is a series of small
redesigns; developers without solid design principles will produce a codebase
that is hard to understand or change - the opposite of agility. The fear to
avoid overengineering can develop into another feat: fear of doing any deep
design thinking at all.

## Part 1: Putting the Domain Model to Work

> A model is a simplification. It is an interpretation of reality that abstracts
> the aspects relevant to solving the problem at hand and ignores extraneous
> detail.

Every software program relates to some activity or interest of its user. The
subject area to which the user applies the program is the *domain* of the
software. To create software that is valuably involved in users' activities, a
development team must bring to bear a body of knowledge related to those
activities.

A domain model is not a particular diagram; it is the idea that the diagram is
intended to convey. **_It is a rigorously organized and selective abstraction of
that knowledge_**.

> Just as a moviemaker selects aspects of experience and presents them in an
> idiosyncratic way to tell a story or make a point, a domain modeler chooses a
> particular model for its utility.

### The Utility of a Model in Domain-Driven Design

Three basic uses determine the choice of a model:

1. *The model and the heart of the design shape each other*: The link between
   model & implementation makes the modeling useful. The code can be interpreted
   based on understanding the model
2. *The model is the backbone of a language used by all team members*:
   Developers can talk about the program in the model language.
3. *The model is distilled knowledge*: A model captures how we choose to think
   about the domain as we select terms, break down concepts, and relate them.

### The Heart of Software

> The heart of the software is its ability to solve domain-related problems for
> its user. All other features, vital though they may be, support this basic
> purpose.

> Complexity in the heart of software has to be tackled head-on. To do otherwise
> is to risk irrelevance.

Leaders within a team who understand the centrality of the domain can put their
software project back on course when the development of a model that reflects
deep understanding gets lost in the shuffle.

There are systematic ways of thinking that developers can employ to search for
insight and produce effective models. There are design techniques that can bring
order to a sprawling software application. Cultivation of these skills makes a
developer much more valuable, even in an initially unfamiliar domain.

## Chapter One: Crunching Knowledge

### Ingredients of Effective Modeling

1. *Binding the model and the implementation*;
2. *Cultivating the language based on the model*;
3. *Developing a knowledge-rich model*;
4. *Distilling the model*: Concepts dropped when they don't prove useful or
   central;
5. *Brainstorming and experimenting*.

> It is the creativity of brainstorming and massive experimentation, leveraged
> through a model-based language and disciplined by the feedback loop through
> implementation, that makes it possible to find a knowledge-rich model and
> distill it. This kind of *knowledge crunching* turns the knowledge of the team
> into valuable models.

### Knowledge Crunching

> Effective domain modelers are knowledge crunchers. They try one organizing
> idea after another, searching for the simple view that makes sense of the
> mass. Success comes in an emerging set of abstract concepts that makes sense
> of all the detail.

In the old waterfall method, knowledge trickles in one direction but does not
accumulate - Analysts have full responsibility for creating the model.

Other projects use an iterative process, but fail to build up knowledge because
they don't abstract. If programmers are not interested in the domain, they learn
only what the application should do, not the principles behind it. Useful
software can be built that way, but the project will never arrive at a point
where powerful new features unfold as corollaries to older features.

Constant refinement of the model:

1. Forces developers to learn essential principles of the business they are
   assisting;
2. Refine the domain experts' understanding of the domain by being forced to
   distill what they know to essentials;
3. Makes the model a tool for organizing the information that continues to flow
   through the project: The model focuses on requirement analysis

Because analysts and programmers are feeding into it: It is cleanly organized
and abstracted so that it can provide leverage for the implementation. Because
the domain experts are feeding into it, the model reflects a deep knowledge of
the business. The abstractions are true business principles.

These models are never perfect; they evolve. They must be:

1. Practical and useful in making sense of the domain
2. Rigorous enough to make the application simple to implement and understand


### Continous Learning

> **When we set out to write software, we never know enough.**

All projects leak knowledge. People who have learned something move on.
Reorganization scatters the team, and the knowledge is fragmented again.

> Highly productive teams grow their knowledge consciously, practicing
> *continuous learning*

These self-educated team members form a stable core of people to focus on the
development tasks that involve the most critical areas. The accumulated
knowledge in the minds of this core team makes them more effective knowledge
crunchers.

There should be some learning when a domain model is discussed.

### Knowledge-Rich Design

Business activities and rules are central to a domain as are the entities
involved; any domain will have various categories of concepts.

Domain experts are usually not aware of how complex their mental processes are;
as, in the course of their work, they navigate all these rules, reconcile
contradictions, and fill in gaps with common sense. Software can't do this. It
is though knowledge crunching in close collaboration with software experts that
the rules are clarified, fleshed out, reconciled, or placed out of scope.

### Deep Models

> Useful models seldom lie on the surface.

> Knowledge crunching is an exploration, and you can't know where you will end
> up.

## Chapter Two: Communication and the Use of Language

### Ubiquitous Language

> To create a supple, knowledge-rich design calls for a versatile, shared team
> language, and lively experimentation with language that seldom happens on
> software projects.

A project faces serious problems when its language is fractured. Domain experts
use their jargon while technical team members have their own language tuned for
discussing the domain in terms of design. The terminology of day-to-day
discussions is disconnected from the terminology embedded in the code
(ultimately, the most important product of a software project). And even the
same person uses different languages in speech and in writing so that the most
incisive expressions of the domain often emerge in a transient form that is
never captured in the code or even in writing.

Translation blunts communication nad makes knowledge crunching anemic. Yet none
of these dialects can be a common language because none serves all needs.

A project needs a common language that is more robust than the lowest common
denominator.

Although the sequence may seem circular, the knowledge crunching process that
can produce a more useful kind of model depends on the team's commitment to
model-based language. Persistent use of that language will force the model's
weaknesses into the open.

By using the model-based language pervasively and not being satisfied until it
flows, we approach a model that is complete and comprehensible, made up of
simple elements that combine to express complex ideas.

1. **Use the model as the backbone of a language. Commit the team to exercise
   that language relentlessly in all communication within the team and in the
   code. Use the same language in diagrams, writing and especially speech**
2. **Iron out difficulties by experimenting with alternative expressions, which
   reflect alternative models. Then refactor the code, renaming classes,
   methods, and modules to conform to the new model. Resolve confusion over
   terms in conversation in just the way we come to agree on the meaning of
   ordinary words.**
3. **Recognize that a change in the language is a change in the model;**
4. **Domain experts should object to terms or structures that are awkward or
   inadequate to convey domain understanding; developers should watch for
   ambiguity or inconsistency that will trip up the design.**

With a UBIQUITOUS LANGUAGE, the model is not just a design artifact. The
language will carry knowledge in a dynamic form. Discussion in the language
brings to life the meaning behind the diagrams and code.

### Modeling Out Loud

One of the best ways to refine a model is to explore with speech, trying out
loud various constructs from possible model variations. Rough edges are easy to
hear.

Play with the model as you talk about the system. Describe scenarios out loud
using the elements and interactions of the model, combining concepts in ways
allowed by the model. Find easier ways to say what you need to say, and then
take those new ideas back down to the diagrams and code.

### One team one language

Technical people often feel the need to "shield" the business experts from the
domain model.

***If sophisticated domain experts don't understand the model, there is
something wrong with the model***

The developers and domain experts can informally test the mode by walking
through scenarios, using the model objects step-by-step. Almost every discussion
is an opportunity for the developers and user experts to play with the model
together, deepening each other's understanding and refining concepts as they go.

Of course developers do use technical terminology that a domain expert wouldn't
understand. Developers have extensive jargons that they need to discuss the
technical aspects of a system. Almost certainly, the users will also have
specialized jargon that goes well beyond the narrow scope of the application and
the understanding of the developers. But these are *extensions* of the language.
These dialects should not contain alternative vocabularies for the same domain
that reflect distinct models.

### Documents and Diagrams

Simple, informal UML diagrams can anchor a discussion. The trouble comes when
people feel compelled to convey the whole model or design through UML --> No one
can see the forest for the trees.

Despite of all that detail, the attributes and relationships are only half the
story of an object model. The behavior of those objects and the constraints on
them are not so easily illustrated.

Object interaction diagrams can illustrate some tricky hotspots in the design,
but the bulk of the interactions can't be shown that way.

> A UML diagram cannot convey two of the most important aspects of a model: the
> meaning of the concepts it represents, and what the objects are meant to do.
> This doesn't need to trouble us though, because careful use of language can
> fill this role pretty well.

Diagrams are a means of communication and explanation, and they facilitate
brainstorming. They serve these ends best if they are **minimal**.

***The vita details about the design are captured in the code.***

Write text documents illustrated with selective and simplified diagrams. *The
model is not the diagram*!

### Written design documents

> **Making written documents that actually help the team produce good software
> is a challenge.**

Once a document takes on a persistent form, it often loses its connection with
the flow of the project. It is left behind by the evolution of the code, or by
the evolution of the language of the project.

#### Documents Should COMPLEMENT Code and Speech

Extreme programming advocates using no extra design documents at all and letting
the code speak for itself. Even comments added to the code do not affect program
behavior, so they always fall out of sync with the active code and its driving
model

> ** This dependence on the code as a communication medium motivates developers
> to keep the code clean and transparent **

However, code as a design document does have its limits. Although its behavior
is unambiguous, that doesn't mean it is obvious --> Too much unnecessary
details.

Massive spoken communication within the team gives context and guidance around
the code, but it is ephemeral and localized and developers are not the only
people who need to understand the model.

> **A document should NOT try to do what the code already does well.**

The code already provides detail. Other documents need to:

1. Illuminate meaning;
2. Give insight into large-scale structures and
3. Focus attention on core elements.

Documents can clarify design intent when the programming language does not
support a straightforward implementation of a concept.

#### Documents Should Work for a Living and Stay Current

> In addition to saving labor, hand-drawn diagrams have the advantage of feeling
> casual and temporary. These are good things to communicate because they are
> generally true of our model ideas.

The greatest value of a design document is to explain the concepts of the model,
help in navigating the detail of the code, and perhaps give some insight into
the model's intended style of use.

> **A document must be INVOLVED in project activities**

Always check:

1. Is the document written in langugage people speak on the project now?
2. Is it written in language embedded in the code?

Listen to the UBIQUITOUS LANGUAGE and how it is changing: the elements described
in the document should be start showing up in both the conversations and code.

> **If a document isn't playing an important role, keeping it up to date though
> sheer will and discipline wastes effort**

By keeping documents **minimal** and focusing them on **complementing the code
and conversation**, documents can stay connected to the project. Let the
UBIQUITOUS LANGUAGE and its evolution be your guide to choosing documents that
live and get woven into the project's activity

### Executable Bedrock

> **Well written code can be very communicative, but the message it communicates
> is not guaranteed to be accurate**

It takes fastidiousness to write code that doesn't just *do* the right thing but
also *says* the right thing.

Aligning the behavior, intent, and message of code using current standard
technology requires discipline and a certain way of thinking about design. To
communicate effectively, the code must be based on the same language used to
write the requirements -- the same language that the developers speak with each
other and with domain experts.

### Explanatory Models

> **Having separate models for implementation, design and team communication
> poses a hazard.**

The model that drives the design is one view of the domain, but it may aid
learning to have other views, used only as educational tools, to communicate
general knowledge of the domain.

One particular reason that other models are needed is scope. An explanatory
model can include aspects of the domain that provide context that clarifies the
more narrowly scoped (technical) model.

## Chapter Three: Binding Model and Implementation

> Domain-driven design calls for a model that doesn't just aid early analysis
> but is the very foundation of the design. This approach has some important
> implications for the code. What is less obvious is that domain-driven design
> requires a different approach to modeling.

> **Tighlt relating the code to an underlying model gives the code meaning and
> makes the model relevant.**

Many design methodologies advocate an *analysis model*, quite distinct from the
design and usually developed by different people. The analysis model is not
created with design issues in mind, and therefore it is likely to be quite
impractical for those needs --> Most of the knowledge crunching done while
building the model is lost when it is implemented.

> If the developers perceive analysis to be a separate process, modeling happens
> in a less disciplined way. If the managers perceive analysis to be a separate
> process, the development team may not be given adequate access to domain
> experts

Software that lacks a concept at the foundation of its design is, at best, a
mechanism that does useful things without explaining its action.

**If the design, or some central part of it, does not map to the domain model,
that model is of little value, and the correctness of the software is suspect.
At the same time, complex mappings between models and design functions are
difficult to understand and, in practice, impossible to maintain as the design
changes. A deadly divide opens between analysis and design so that insight
gained in each of those activities does not feed into the other.**

MODEL-DRIVEN-DESIGN discards the dichotomy of the analysis model and design to
search out a single model that serves both purposes. This requires us to be more
demanding of the chosen model, since it must fulfill two quite different
objectives.

The binding of model and design mustn't come at the cost of a weakened analysis,
fatally compromised by technical considerations. Nor can we accept clumsy
designs, reflecting domain ideas but eschewing software design principles.

**Design a portion of the software system to reflect the domain model in a very
literal way, so that mapping is obvious. Revisit the model and modify it to be
implemented more naturally in software, even as you seek to make it reflect
deeper insight into the domain. Demand a single model that serves both purposes
well, in addition to supporting a robust UBIQUITOUS LANGUAGE.**

**Draw from the model the terminology used in the design and the basic
assignment of responsibilities. The code becomes an expression fo the model, so
a change to the code may be a change to the model. Its effect must ripple
through the rest of the project's activities accordingly**

**To tie the implementation slavishly to a model usually requires software
development tools and languages that support a modeling paradigm, such as
object-oriented programming**

### Letting the Bones Show: Why Models Matter to Users

> When a design is based on a model that reflects the basic concerns of the
> users and domain experts, the bones of the design can be revealed to the user
> to a greater extent than with other design approaches. Revealing the model
> gives the user access to the potential of the software and yields consistent,
> predictable behavior.

### Hands-on Modelers

> **Software development is _ALL_ design!**

**If the people who write the code do not feel responsible for the model, or
don't understand how to make the model work for an application, then the model
has nothing to do with the software. If developers don't realize that changing
code changes the model, then their refactoring will weaken the model rather than
strengthen it. Meanwhile, when a modeler is separated from the implementation
process, he or she never acquires, or quickly loses, a feel for the constraints
of implementation. The basic constraint of MODEL-DRIVEN-DESIGN -- that the model
supports an effective implementation and abstracts key domain knowledge -- is
half-gone, and the resulting models will be impractical. Finally, the knowledge
and skills of experienced designers won't be transferred to other developers if
the division of labor prevent the kind of collaboration that conveys the
subtleties of coding a MODEL-DRIVEN-DESIGN.**

**Any technical person contributing to the model must spend some time touching
the code, whatever primary role he or she plays on the project. Anyone
responsible for changing code must learn to express a model through the code.
Every developer must be involved in some level of discussion about the model and
have contact with domain experts. Those who contribute in different ways must
consciously engage those who touch the code in a dynamic exchange of model ideas
through the UBIQUITOUS LANGUAGE.**

## Part 2: The building blocks of a Model-Driven Design

> Certain kinds of decisions keep the model and implementation aligned with each
> other, each reinforcing the other's effectiveness

To make the domain-driven design process resilient, developers need to
understand *how* the well-known fundamentals support MODEL-DRIVEN-DESIGN, so
they can compromise without derailing.

> Developing a good domain model is an art. But the practical design and
> implementation of a model's individual elements can be relatively systematic.
> Isolating the domain design from the mass of other concerns in the software
> system will greatly clarify the design's connection to the model.

## Chapter Four: Isolating the Domain

> The part of the software that specifically solves problems from the domain
> usually constitutes only a small portion of the entire software system,
> although its importance is disproportionate to its size.

We need to **decouple the domain objects from other functions of the system, so
we can avoid confusing the domain concepts with other concepts related only to
software terminology** or losing sight of the domain altogether in the mass of
the system.

**In an object-oriented program, UI, database, and other support code often gets
written directly into the business objects. Additional business logic is
embedded in the behavior of UI wdigets and database scripts. This happens
because it is the easiest way to make things work, in the short run.**

**When the domain-related code is diffused through such a large amount of other
code, it becomes extremely difficult to see and  to reason about. Superficial
changes to the UI can actually change business logic. To change a business rule
may require a meticulous tracing of UI code, database code, or other program
elements. Implementing coherent, model-driven objects becomes impractical.
Automated testing is awkward. With all the technologies and logic involved in
each activity, a program must be kept very simple or it becomes impossible to
understand.**

Creating programs that can handle very complex tasks calls for the separation of
concerns, allowing concentration on different parts of the design in isolation.

LAYERED ARCHITECTURES: The essential principle is that any element of a layer
depends only on other elements in the same layer or on elements of the layers
"beneath" it. Communication upward must pass through some indirect mechanism.

Example of layers:

| User Interface (or Presentation Layer)  | Responsible for showing information to the user and interpreting the user's commands. The external actor might sometimes be another computer system rather than a human user.   |
|---------------------------------------- |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------  |
| Application Layer   | Defines the jobs the software is supposed to do and directs the expressive domain objects to work out problems. The tasks this layer is responsible for are meaningful to the business or necessary for interaction with the application layers of other systems.  This layer is kept thin. It does not contain business rules or knowledge, but only coordinates tasks and delegates work to collaborations of domain objects in the next layer down. It does not have state reflecting the business situation, but it can have state that reflects the progress of a task for the user or the program   |
| Domain Layer (or Model Layer)   | Responsible for representing concepts of the business, information about the business situation, and business rules. State that reflects the business situation is controlled and used here, even though the technical details of storing it are delegated to the infrastructure. This layer is the heart of business software.   |
| Infrastructure Layer  | Provides generic technical capabilities that support the higher layers: message sending for the application, persistence for the domain, drawing widgets for the UI, and so on. The infrastructure layer may also support the pattern of interactions between the four layers through an architectural framework.   |

**Partition a complex program into layers. Develop a design within each layer
that is cohesive and that depends only on the layers below. Follow standard
architectural patterns to provide loose coupling to the layers above.
Concentrate all the code related to the domain model in one layer and isolate it
from the user interface, application and infrastructure code. The domain
objects, free of the responsibility of displaying themselves, storing
themselves, managing application tasks, and so forth, can be focused on
expressing the domain model. This allows a model to evolve to be rich enough and
clear enough to capture essential business knowledge and put it to work.**

### Relating the Layers

> Layers are meant to be loosely coupled, with design dependencies in only one
> direction. Upper layers can use or manipulate elements of lower ones
> straightforwardly by calling their public interfaces, holding references to
> them (at least temporarily), and generally using conventional means of
> interaction. But when an object of a lower level needs to communicate upward,
> we need another mechanism, drawing on architectural patterns for relating
> layers such as callbacks or OBSERVERS.

The infrastructure layer usually does not initiate action in the domain layer.
Being "below" the domain layer, it should have no specific knowledge of the
domain it is serving. Indeed, such technical capabilities are most often offered
as SERVICES.

The application and domain layers call on the SERVICES provided by the
infrastructure layer. When the scope of a SERVICE has been well chosen and its
interface well designed, the caller can remain loosely coupled and uncomplicated
by the elaborate behavior the SERVICE interface encapsulates.

### The Smart UI "Anti-pattern"

If an unsophisticated team with a simple project decides to try a MODEL-DRIVEN
DESIGN with LAYERED ARCHITECTURE, it will face a difficult learning curve. Team
members will have to master complex new technologies and stumble through the
process of learning object modeling (which is challenging, even with the help of
this book!). The overhead of managing infrastructure and layers makes very
simple tasks take longer. Simple projects come with short time lines and modest
expectations. Even if the team is given more time, the team members are likely
to fail to master the techniques without expert help. And in the end, if they do
surmount these challenges, they will have produced a simply system. Rich
capabilities were never requested.

Domain-driven design pays off best for ambitious projects, and it does require
strong skills. Not all projects are ambitious. Not all project teams can muster
those skills.

**Therefore, when circumstances warrant: Put all business logic into the user
interface. Chop the application into small functions and implement them as
separate user interfaces, embedding the business rules into them. Use a
relational database as a shared repository of the data. Use the most automated
UI building and visual programming tools available.**

In truth, there are advantages to the SMART UI, and there are situations where
it works best.

*Advantages:*

- Productivity is high and immediate for simple applications.
- Less capable developers can work this way with little training.
- Even deficiencies in requirements analysis can be overcome by releasing a
  prototype to users and then quickly changing the product to fit their
  requests.
- Applications are decoupled from each other, so that delivery schedules of
  small modules can be planned relatively accurately. Expanding the system with
  additional, simples behavior can be easy.
- Relational databases work well and provide integration at the data level.
- [4GL](https://en.wikipedia.org/wiki/Fourth-generation_programming_language)
  tools work well.
- When applications are handed off, maintenance programmers will be able to
  quickly redo portions they can't figure out, because the effects of the
  changes should localized to each particular UI.

*Disadvantages:*

- Integration of applications is difficult except through the database
- There is no reuse of behavior and no abstraction of the business problem.
  Business rules have to be duplicated in each operation to which they apply.
- Rapid prototyping and iteration reach a natural limit because the lack of
  abstraction limits refactoring options.
- Complexity buries you quickly, so the growth path is strictly toward
  additional simple applications. There is no graceful path to richer behavior.

> It is a common mistake to undertake a sophisticated design approach that the
> team isn't committed to carrying all the way through. Another common costly
> mistake is to build a complex infrastructure and use industrial-strength tools
> for a project that doesn't need them.

The bottom line is this: *If the architecture isolates the domain-related code
in a way that allows a cohesive domain design loosely coupled to the rest of the
system, then that architecture can probably support domain-driven design*

If you have a complex application and are committing to MODEL-DRIVEN DESIGN,
bite the bullet, get the necessary experts, and *avoid the SMART UI*.

### Other Kinds of Isolation

There are influences other than infrastructure and user interfaces that can
corrupt your domain model. You must deal with other domain components that are
not fully integrated into your model. You have to cope with other development
teams who use different models of the same domain. These and other factors can
blur your model and rob it of its utility. -- See chapter 14 (Maintaining Model
Integrity) to learn how to avoid this.

A really complicated model can become unwieldy all by itself -- See chapter 15
(Distillation) to learn how to avoid this.

## Chapter Five: A Model Expressed in Software

> This chapter brings together all of the building blocks of a MODEL-DRIVEN
> DESIGN, which embody the model in software

### Associations

> *For every traversable association in the model, there is a mechanism in the
> software with the same properties*

For example, a one-to-many association might be implemented as a collection in
an instance variable. But the design is not necessarily so direct. There may be
no collection; an accessor method may query a database to find the appropriate
records and instantiate objects based on them. Both of these designs would
reflect the same model.

There are at least three ways of making associations more tractable:

1. Imposing traversal direction
2. Adding a qualifier, effectively reducing multiplicity
3. Eliminating nonessential associations

> **It is important to constrain relationships as much as possible**

Understanding the domain may reveal a natural directional bias. Very often,
deeper understanding leads to a "qualified" relationship. This qualifier may
reduce multiplicity of the association and explicitly embed an important rule
into the model.

Consistently constraining associations in ways that reflect the bias of the
domain not only makes those associations more communicative and simpler to
implement, it also gives significance to the remaining bidirectional
associations.

> Carefully distilling and constraining the model's associations will take you a
> long way toward a MODEL-DRIVEN DESIGN!

### Entities (A.K.A Reference Objects)

> **Many objects are not fundamentally defined by their attributes, but rather
> by a thread of continuity and identity.**

Example: A person has an identity that stretches from birth to death and even
beyond. That person's physical attributes transform and ultimately disappear.
The name may change. Financial relationships come and go. There isn't a single
attribute of a person that cannot change; yet the identity persists.

Object modeling tends to lead us to focus on the attributes of an object, but
the fundamental concept of an ENTITY is an abstract continuity threading through
a life cycle and even passing through multiple forms.

**Some objects are not defined primarily by their attributes. They represent a
thread of identity that runs through time and often across distinct
representations. Sometimes such an object must be matched with another object
even though attributes differ. An object must be distinguished from other
objects even though they might have the same attributes. Mistaken identity can
lead to data corruption.**

An object defined primarily by its identity is called an ENTITY. ENTITIES have
special modeling and design considerations. Entities have special modeling and
design considerations:

1. They have life cycles that can radically change their form and content, but a
   thread of continuity must be maintained. Be alert to requirements that call
   for matching objects by attributes.
2. Their identities must be defined so that they can be effectively tracked. The
   model must define what it *means* to be the same thing.
3. Their class definitions, responsibilities, attributes and associations should
   revolve around WHO they are, rather than the particular attributes they
   carry. Keep the class definition simple and focused on lifecycle continuity
   and identity.

> Identity is not intrinsic to a thing in the world; it is a meaning
> superimposed because it is useful. In fact, the same real-world thing might or
> might not be represented as an ENTITY in a domain model.

#### Modeling Entities

> The most basic responsibility of ENTITIES is to establish continuity so that
> behavior can be clear and predictable. They do this best if they are kept
> spare.

Some guidelines:
1. Strip the ENTITY object's definition down to the most intrinsic
   characteristics, particularly those that identity it or are commonly used to
   find or match it.
2. Add only behavior that is essential to the concept and attributes that are
   required by that behavior that is essential to the concept and attributes
3. Look to remove behavior and attributes into other objects associated with the
   core ENTITY. Some of these will be other ENTITIES. Some will be VALUE
   OBJECTS.

Beyond identity issues, ENTITIES tend to fulfill their responsibilities by
**coordinating the operations of objects they own.**

##### Designing the identity operation

> **The definition of identity emerges from the model. Defining identity demands
> understanding of the domain**

When there is no true unique key made up of the attributes of an object, another
common solution is to attach to each instance a symbol that is unique within the
class. Once it is created and stored, it's immutable, it must never change.

Often, the means of identification demand a careful study of the domain, as
well.

There are cases in which a generated ID *is* of interest to the user. E.g. a
tracking number.

> **In some cases, the uniqueness of the ID must apply beyond the computer
> system's boundaries. In this cases usually identity is generated by a third
> party.**

When the application requires an external ID, the users of the system become
responsible for supplying IDs that are unique, and the system must give them
adequate tools to handle exceptions that arise.

> Given all these conceptual problems, it's easy to lose sight of the underlying
> conceptual problem: **What does it mean for two objects to be the same
> thing?**

### Value Objects

> Many objects have no conceptual identity. These objects describe some
> characteristic of a thing.

Because the most conspicuous objects in a model are usually ENTITIES, and
because it is so important to track each ENTITY's identity, it is natural to
consider assigning an identity to all domain objects.

This causes:
1. Artificial identity: misleading
2. The system have to cope with the tracking: Many possible performance
   optimizations are ruled out
3. Analytical effort is required to define meaningful identities and work out
   foolproof ways to track objects across distributed systems or in database
   storage.

**Tracking the identity of ENTITIES is essential, but attaching identity to
other objects can hurt system performance, add analytical work, and muddle the
model by making all objects look the same.**

**Software design is a constant battle with complexity. We must make
distinctions so that special handling is applied only where necessary.**

**However, if we think of this category of object as just the absence of
identity, we haven't added much to our toolbox or vocabulary. In fact, these
objects have characteristics of their own and their own significance to the
model. _These are the objects that describe things_**

- A VALUE OBJECT can be an assemblage of other objects.
- VALUE OBJECTS can even reference ENTITIES
- VALUE OBJECTS are often passed as parameters in messages between objects.
- They are frequently transient, created for an operation and discarded
- VALUE OBJECTS are used as attributes of ENTITIES (and other VALUES)
- The attributes that make up a VALUE OBJECT should form a conceptual whole.

**When you care only about the attributes of an element of the model, classify
it as a VALUE OBJECT. Make it express the meaning of the attributes it conveys
and give it related functionality. Treat the VALUE OBJECT as immutable. Don't
give it any identity and avoid the design complexities necessary to maintain
ENTITIES.**

#### Designing VALUE OBJECTS

VALUE OBJECTS can be *shared* between ENTITIES (each with a pointer to the same
instance) with no change in their behavior or identity.

> In order for an object to be shared safely, it must be immutable: it cannot be
> changed except by full replacement

**The economy of copying versus sharing depends on the implementation
environment. E.g. sharing can slow down a distributed system.**

Sharing is best restricted to those cases in which it is most valuable and least
troublesome:

- When saving space or object count in the database is critical
- When communication overhead is low (centralized server)
- When the shared object is strictly immutable

As long as a VALUE OBJECT is immutable, change management is simple.

> Avoiding unnecessary constraints in a model leaves developers free to do
> purely technical performance tuning. Explicitly defining the essential
> constraints lets developers tweak the design while keeping safe from changing
> meaningful behavior.

Database considerations:
1. If an object is referenced by many other objects, some of those objects will
   not be located nearby (on the same page), requiring an additional physical
   operation to get the data.
2. Sometimes it's wiser to *denormalize* when access time is more critical than
   storage space or simplicity of maintenance
3. In a distributed system, holding a reference to a VALUE OBJECT on another
   server will probably make for slow responses to messages; instead a copy of
   the whole object should be passed to the other server (FOR VALUE OBJECTS
   ONLY)

#### Designing Associations That Involve Value Objects

Same things that apply for ENTITIES, apply here.

> Bidirectional associations between two VALUE OBJECTS just make no sense. Try
> to completely eliminate bidirectional associations between VALUE OBJECTS.

### Services

> In some cases, the clearest and most pragmatic design includes operations that
> do not conceptually belong to any object. Rather than force the issue, we can
> follow the natural contours of the problem space and include SERVICES
> explicitly in the model.

Now, the more common mistake is to give up too easily on fitting the behavior
into an appropriate object, gradually slipping toward procedural programming.

**Some concepts from the domain aren't natural to model as objects. Forcing the
required domain functionality to be responsibility of an ENTITY or VALUE either
distorts the definition of a model-based object or adds meaningless artificial
objects.**

A SERVICE is an operation offered as an interface that stands alone in the
model, without encapsulating state, as ENTITIES and VALUE OBJECTS do. A SERVICE
tends to be named for an activity, rather than an entity.

SERVICES should be used judiciously and not allowed to strip the ENTITIES and
VALUE OBJECTS of all their behavior.

A good SERVICE has 3 characteristics:

1. The operation relates to a domain concept that is not a natural part of an
   ENTITY or VALUE OBJECT;
2. The interface is defined in terms of other elements of the domain model;
3. The operation is stateless.

**When a significant process or transformation in the domain is not a natural
responsibility of an ENTITY or VALUE OBJECT, add an operation to the model as a
standalone interface declared as a SERVICE. Define the interface in terms of the
language of the model and make sure the operation name is part of the UBIQUITOUS
LANGUAGE. Make the SERVICE stateless.**

#### SERVICES and the Isolated Domain Layer

SERVICES are not used only in the domain layer. It takes care to distinguish
SERVICES that belong to the domain layer from those of other layers and to
factor responsibilities to keep that distinction sharp.

Technical SERVICES should lack any business meaning at all.

Many domain or application SERVICES are built on top of the population of
ENTITIES and VALUES, behaving like scripts that organize the potential of the
domain to actually get something done.

What's more, in most development systems, it is awkward to make a direct
interface between a domain object and external resources. **We can dress up such
external SERVICES with a FACADE that takes inputs in terms of the model, perhaps
returning an object as a result. But whatever intermediaries we might have, and
even though they don't belong to us, those SERVICES are carrying out the domain
responsibility of funds transfer.**

#### Granularity

Medium-grained, stateless SERVICES can be easier to reuse in large systems
because they encapsulate significant functionality behind a simple interface.
Also, fine-grained objects can lead to inefficient messaging in a distributed
service.

Too fine-grained domain objects can contribute to knowledge leaks from the
domain into the application layer, where the domain object's behavior is
coordinated. The judicious introduction of domain services can help maintain the
bright line between layers.

This pattern favors interface simplicity over client control and versatility. It
provides a medium grain of functionality very useful in packaging components of
large or distributed systems.

#### Access to SERVICES

The means of providing access to a SERVICE is not as important as the design
decision to carve off specific responsibilities. Elaborate architectures should
be used only when there is a real need to distribute the system or otherwise
draw on the framework's capabilities.

### Modules (A.K.A PACKAGES)

> The MODULES in the domain layer should emerge as a meaningful part of the
> model, telling the story of the domain on a larger scale.

**Everyone uses MODULES, but few treat them as a full-fledged part of the model.
Code gets broken down into all sorts of categories, from aspects of the
technical architecture to developers' work assignments. Even developers who
refactor a lot tend to content themselves with MODULES conceived early in the
project.**

**It is a truism that there should be low coupling between MODULES and high
cohesion within them. Explanations of coupling and cohesion tend to make them
sound like technical metrics, to be judged mechanically based on the
distributions of associations and interactions. Yet it isn't just code being
divided into MODULES, but concepts. There is a limit to how many things a person
can think about at once (hence low coupling). Incoherent fragments of ideas are
as hard to understand as an undifferentiated soup of ideas (hence high
cohesion).**

1. Low Coupling: The relationships between model elements separated into
   different models are less direct, which increases the overhead of
   understanding their place in the design. Low Coupling minimises this cost;
2. High Cohesion: The elements of a good model have synergy, and well-chosen
   MODULES bring together elements of the model with particularly rich
   conceptual relationships.

> MODULES and the smaller elements should coevolve, but typically they do not.
> Just as model objects tend to start out naive and concrete and then gradually
> transform to reveal deeper insight, MODULES can become subtle and abstract.
> Letting the MODULES reflect changing understanding of the domain will also
> allow more freedom for the objects within them to evolve.


**When you place some classes together in a MODULE, you are telling the next
developer who looks at your design to think about them together.**

Therefore:
1. **Choose MODULES that tell the story of the system and contain a cohesive set
   of concepts:** This often yields low coupling between MODULES, but if it
   doesn't, look for a way to change the model to disentangle the concepts, or
   search for an overlooked concept that might be the basis of a MODULE that
   would bring the elements together in a meaningful way
2. **Seek low coupling in the sense of concepts that can be understood and
   reasoned about independently of each other**
3. **Refine the model until it partitions according to high-level domain
   concepts and the corresponding code is decoupled as well.**
4. **Give the MODULES names that become part of the UBIQUITOUS LANGUAGE**:
   MODULES and their names should reflect insight into the domain;

#### Agile MODULES

> MODULE structures and names often reflect much earlier forms of the model than
> the classes do.

Inevitable early mistakes in MODULE choices lead to high coupling, which makes
it hard to refactor. The lack of refactoring just keeps increasing the inertia.
It can only be overcome by biting the bullet and reorganizing MODULES based on
experience.

**Whatever development technology the implementation will be based on, we need
to look for ways of minimizing the work of refactoring MODULES, and minimizing
clutter in communicating to other developers.**

#### The Pitfalls of Infrastructure-Driven packaging

> Strong forces on our packaging decisions come from technical frameworks. Some
> of these are helpful, while others need to be resisted;

Elaborate technically driven packaging schemes impose two costs:

- If the framework's partitioning conventions pull apart the elements
  implementing the conceptual objects, the code no longer reveals the model.
- There is only so much partitioning a mind can stitch back together, and if the
  framework uses it all up, the domain developers lose their ability to chunk
  the model into meaningful pieces.

It is best to keep things simple. Choose a minimum of technical partitioning
rules that are essential to the technical environment or aid development. For
example, decoupling complicated data persistence code from the behavioral
aspects of the objects may make refactoring easier.

**Unless there is a real intention to distribute code on different servers, keep
all the code that implements a single conceptual object in the same MODULE, if
not the same object.**

**Use packaging to separate the domain layer from the other code. Otherwise,
leave as much freedom as possible to the domain developers to package the domain
objects in ways that support their model and design choices.**

Each concept from the domain model should be reflected in an element of
implementation. The ENTITIES, VALUE OBJECTS, and their associations, along with
a few domain SERVICES and the organizing MODULES, are points of direct
correspondence between the implementation and the model.

> **Resist the temptation to add anything to the domain objects that does not
> closely relate to the concepts they represent.**

## Chapter Six: The Life Cycle of a Domain Object

> Every object has a life cycle. An object is born, it likely goes through
> various states, and it eventually dies -- being either archived or deleted.

Challenges of object lifecycle fall into two categories:

1. Maintaining integrity throughout the life cycle
2. Preventing the model from getting swamped by the complexity of managing the
   life cycle

This chapter will address these issues through three patterns:

1. AGGREGATES: Clear ownership and boundaries
2. FACTORIES: Create and reconstitute complex objects
3. REPOSITORIES: Address the middle and end of the life cycle, finding and
   retrieving encapsulating infrastructure.

### AGGREGATES

> How do we know where and object made up of other objects begins and ends?

**It is difficult to guarantee the consistency of changes to objects in a model
with complex associations. Invariants need to be maintained that apply to
closely related groups of objects, not just discrete objects. Yet cautious
locking schemes cause multiple users to interfere pointlessly with each other
and make a system unusable.**

Finding a balanced solution to these kinds of problems calls for deeper
understanding of the domain, this time extending to factors such as the
frequency of change between the instances of certain classes. We need to find a
model that leaves high-contention points looser and strict invariants tighter.

Although this problem surfaces as technical difficulties in database
transactions, it is rooted in the model -- in its lack of defined boundaries.

An AGGREGATE is a cluster of associated objects that we treat as a unit for the
purpose of data changes. Each aggregate has a root and a boundary.

- Boundary: Defines what is inside the AGGREGATE. Objects within the boundary
  may hold references to each other.
- Root: A **single** specific ENTITY contained in the AGGREGATE. The **ONLY**
  member of the AGGREGATE that outside objects are allowed to hold references
  to.

ENTITIES other than the root have local identity, but that identity needs to be
distinguishable only within the AGGREGATE.

Invariants, which are consistency rules that must be maintained whenever data
changes, will involve relationships between members of the AGGREGATE. Any rule
that spans AGGREGATES will not be expected to be up-to-date at all times. The
invariants applied within an AGGREGATE will be enforced with the completion of
each transaction.

To translate the conceptual AGGREGATE into the implementation we need a set of
rules to apply to all transactions:

- The root ENTITY has a global identity and is ultimately responsible for
  checking invariants
- Root ENTITIES have global identity. ENTITIES inside the boundary have local
  identity, unique only within the AGGREGATE;
- Nothing outside the AGGREGATE boundary can hold a reference to anything
  inside, except to the root ENTITY. The root ENTITY can hand references to the
  internal ENTITIES to other objects, but those objects can use them only
  transiently and they may not hold on to the reference.
- As a corollary to the previous rule, only AGGREGATE roots can be obtained
  directly with database queries. All other objects must be found by traversal
  of associations.
- Objects within the AGGREGATE can hold references to other AGGREGATE roots.
- A delete operation must remove everything within the AGGREGATE boundary at
  once.
- When a change to any object within the AGGREGATE boundary is committed, all
  invariants of the whole AGGREGATE must be satisfied.

**Cluster the ENTITIES and VALUE OBJECTS into AGGREGATES and define boundaries
around each. Choose one ENTITY to be the root of each AGGREGATE, and control all
access to the objects inside the boundary through the root. Allow external
objects to hold references to the root only. Transient references to internal
members can be passed out for use within a single operation only. Because the
root controls access, it cannot be blindsided by changes to the internals. This
arrangement makes it practical to enforce all invariants for objects in the
AGGREGATE and for the AGGREGATE as a whole in any state change.**

### FACTORIES

> When creation of an object, or an entire AGGREGATE, becomes complicated or
> reveals too much of the internal structure, FACTORIES provide encapsulation.

**Creation of an object can be a major operation in itself, but complex assembly
operations do not fit the responsibility of the created objects. Combining such
responsibilities can produce ungainly designs that are hard to understand.
Making the client direct construction muddies the design of the client, breaches
encapsulation of the assembled object or AGGREGATE, and overly couples the
client to the implementation of the creation object.**

Complex object creation is a responsibility of the domain layer, yet that task
does not belong to the objects that express the model. Object creation and
assembly usually have no meaning in the domain; they are a necessity of the
implementation.

FACTORIES do not correspond to anything in the model, but they are nonetheless
part of the domain layer's responsibility.

**Shift the responsibility for creating instances of complex objects and
AGGREGATES to a separate object, which may itself have no responsibility in the
domain model but is still part of the domain design. Provide an interface that
encapsulates all complex assembly and that does not require the client to
reference the concrete classes of the objects being instantiated. Create entire
AGGREGATES as a piece, enforcing their invariants.**

The two basic requirements for any good FACTORY are:

1. Each creation method is atomic and enforces all invariants of the created
   object or AGGREGATE. A FACTORY should only be able to produce and object in a
   consistent state. If the interface makes it possible to request an object
   that can't be created correctly, then an exception should be raised or some
   other mechanism should be invoked that will ensure that no improper return
   value is possible.
2. The FACTORY should be abstracted to the type desired, rather than the
   concrete class(es) created.

#### Choosing FACTORIES and Their Sites

> Usually you place the FACTORY where you want the control to be.

Some examples:
1. FACTORY METHOD on AGGREGATE root: This hides the implementation of the
   interior of the AGGREGATE from any external client, while giving the root
   responsibility for ensuring the integrity of the the AGGREGATE as elements
   are added;
2. FACTORY METHOD on an object that is closely involved in spawning another
   object, although it doesn't own the product once created. Example:
   **BrokerageAccount** & **TradeOrders**, it makes sense for the factory to be
   within the account in this case.
3. Dedicated FACTORY object or SERVICE: Usually produces an entire AGGREGATE.
   Point of attention: **Respect the rules limiting access within an AGGREGATE**

A FACTORY is **very tightly coupled to its product,** so a FACTORY should be
attached only to an object that has a close natural relationship with the
product.

#### When a constructor is all you need

There are times in which the directness of a constructor makes it the best
choice:

- The class is the type. It is not part of any interesting hierarchy, and it
  isn't used polymorphically by implementing an interface;
- The client cares about the implementation, perhaps as a way of choosing a
  STRATEGY;
- All of the attributes of the object are available to the client, so that no
  object creation gets nested inside the constructor exposed to the client;
- Construction is not complicated

A public constructor must follow the same rules as a FACTORY: It must be an
atomic operation that satisfies all invariants of the created object.

Avoid calling constructors within constructors of other classes. Constructors
should be dead simple. Complex assemblies, especially of AGGREGATES, call for
FACTORIES. The threshold for choosing to use a little FACTORY METHOD isn't high.

#### Designing the Interface

1. *Each operation must be atomic:* Pass in everything needed to create a
   complete product in a single interaction with the FACTORY. You will also
   decide what will happen if creation fails, in the event some invariant isn't
   satisfied. Adopt a coding standard for failures in FACTORIES;
2. *The FACTORY will be coupled to its arguments:* If you are not careful in
   your selection of input parameters, you can create a rat's nest of
   dependencies. The degree of coupling will depend on what you do with the
   argument. If it is simply plugged into the product, you've created a modest
   dependency. If you are picking parts out of the argument to use in the
   construction, the coupling gets tighter.
3. Use the abstract type of the arguments, not their concrete classes. The
   FACTORY is coupled to the concrete class of the products; it does not need to
   be coupled to concrete parameters also.


Safest parameters: objects from the lower design layer; objects that are closely
related to the product in the model, so that no new dependency is added.

#### Where Does Invariant Logic Go?

> You should always think twice before removing the rules applying to an object
> outside that object. The FACTORY can delegate invariant checking to the
> product, and this is often best.

Under some circumstances, there are advantages to placing invariant logic in the
FACTORY and reducing clutter in the product. This is especially *appealing* with
AGGREGATE rules (which spans many objects). It is especially *unappealing* with
FACTORY METHODS attached to other domain objects.

#### Entity Factories Versus Value Object Factories

1. VALUE OBJECTS are immutable: So FACTORY operations have to allow for a full
   description of the product, it comes out in its final form. ENTITY FACTORIES
   tend to take just the essential attributes required to make a valid
   AGGREGATE. Details can be added later
2. ENTITIES have issues involved in assigning identity -- irrelevant for a VALUE
   OBJECT. The FACTORY must receive all parameters involved in assigning
   identity.

#### Reconstituting Store Objects

> Most transmission methods flatten an object into an even more limited
> presentation. Therefore, retrieval requires a potentially complex process of
> reassembling the parts into a live object.

A FACTORY used for reconstitution is very similar to one used for creation, with
two major differences:

1. *An ENTITY FACTORY used for reconstitutions does not assign a new tracking
   ID.* To do so would lose the continuity with the objects previous
   incarnation. So identifying attributes must be part of the input parameters
   in a FACTORY reconstituting a stored object;
2. *A FACTORY reconstituting an object will handle violation of an invariant
   differently.* During the creation of a new object, a FACTORY should simply
   balk when an invariant isn't met, but a more flexible response may be
   necessary in reconstitution. If an object already exists somewhere in the
   system (such as in the database), this fact cannot be ignored. Yet we can't
   also ignore the rule violation. There has to be some strategy for repairing
   such inconsistencies, which can make reconstitution more challenging than the
   creation of new objects.

---

The access points for the creation of instances must be identified, and their
scope must be defined explicitly They may simply be constructors, but often
there is a need for a more abstract or elaborate instance creation mechanism.
This need introduces new constructs into the design: FACTORIES.

A FACTORY encapsulates the life cycle transitions of creation and
reconstitution. Another transition that can swamp the domain design is the
transition to and from storage. This transition is the responsibility of another
domain design construct, the REPOSITORY.

### Repositories

> Associations allow us to find an object based on its relationship to another.
> But we must have a starting point for a traversal to an ENTITY or VALUE in the
> middle of its life cycle.

**A client needs a practical means of acquiring references to pre-existing
domain objects. If the infrastructure makes it easy to do so, the developers of
the client may add more traversable associations, muddling the model. On the
other hand, they may use queries to pull the exact data they need from the
database, or to pull a few specific objects rather than navigating from
AGGREGATE roots. Domain logic moves into queries and client code, and the
ENTITIES and VALUE OBJECTS become mere data containers. The sheer technical
complexity of applying most database access infrastructure quickly swamps the
client code, which leads developers to dumb down the domain layer, which makes
the model irrelevant.**

Some things that help:
1. Do not worry with Transient objects
2. Any object internal to an AGGREGATE is prohibited from access except by
   traversal from the root.

**A subset of persistent objects must be globally accessible through a search
based on object attributes. Such access is needed for the roots of AGGREGATES
that are not convenient to reach by traversal. They are usually ENTITIES,
sometimes VALUE OBJECTS with complex internal structure, and sometimes
enumerated VALUES. Providing access to other objects muddies important
distinctions. Free database queries can actually breach the encapsulation of
domain objects and AGGREGATES. Exposure of technical infrastructure and database
access mechanisms complicates the client and obscures the MODEL-DRIVEN DESIGN.**

The REPOSITORY pattern is a simple conceptual framework to encapsulate those
solutions and bring back our model focus. A REPOSITORY represents all objects of
a certain type as a conceptual set. It acts like a collection, except with more
elaborate querying capability.

**For each type of object that needs global access, create an object that can
provide the illusion of an in-memory collection of all objects of that type. Set
up access through a well-known global interface. Provide methods to add and
remove objects, which will encapsulate the actual insertion or removal of data
in the data store. Provide methods that select objects based on some criteria
and return fully instantiated objects or collections of objects whose attribute
values meet the criteria, thereby encapsulating the actual sotrage and query
technology. Provide REPOSITORIES only for AGGREGATE roots that actually need
direct access. Keep the client focused on the model, delegating all object
storage and access to the REPOSITORIES.**

---

Advantages of REPOSITORIES:

- Present clients with a simple model for obtaining persistent objects and
  managing their life cycle;
- Decouple application and domain design from persistence technology, multiple
  database strategies, or even multiple data sources;
- Communicate design decisions about object access
- Allow easy substitution of a dummy implementation, for use in testing.

#### Querying a Repository

Although most queries return an object or a collection of objects, it als ofits
within the concept to return some types of summary calculations, such as an
object count, or a sum of a numerical attribute that was intended by the model
to be tallied.

Queries cna be written directly in the underlying language, or abstractions like
SPECIFICATIONs or CRITERIAs can be used to query the data

#### Client Code Ignores REPOSITORY Implementation; Developers do not

> The developers **must understand what is happening under the hood.** The
> performance implications can be extreme when REPOSITORIES are used in
> different ways or work in different ways.

Developers need to understand the implications of using encapsulated behavior.
That does not have to mean deatiled familiarity with the implementation.
Well-designed components can be characterized.

There MUST be feedback to developers in both directions between the use of the
REPOSITORY and the implementation of its queries.

#### Implementing a Repository

> Hide inner workings from the client, so that the client code will be the same
> whether the data is stored in an object database, relational database or
> simply held in memory.

The REPOSITORY needs to delegate to the appropriate infrastructure services to
get the job done. Encapsulating the mechanisms of storage, retrieval, and query
is the most basic feature of a REPOSITORY implementation.

Concerns to keep in mind:

1. *Abstract the type*. A REPOSITORY "containes" all instances of a specific
   type, but this does not mean that you need one REPOSITORY for each class. The
   type could be an abstract superclass of a hierarchy. The type could be an
   interface whose implementers are not even hierarchically related. Or it could
   be a specific concrete class. Keep in mind that you may well face constraints
   imposed by the lack of such polymorphism in your database technology.
2. *Take advantage of the decoupling from the client.* You have more freedom to
   change the implementation of a REPOSITORY than you would if the client were
   calling the mechanisms directly. You can take advantage of this to optimize
   for performance, by varying the query technique or by caching objects in
   memory, freely switching persistence strategies at any time. You can
   facilitate testing of the client code and the domain objects by providing an
   easily manipulated, dummy in-memory strategy.
3. *Leave transaction control to the client.* Althought the REPOSITORY will
   insert into and delete from the database, it will ordinarily not commit
   anything. It is tempting to commit after saving, for example, but the client
   presumably has the context to correctly initiate and commit units of work.
   Transaction management will be simpler if the REPOSITORY keeps its hands off.

#### Relationships with Factories

> A FACTORY handles the beginning of an object's life; a REPOSITORY helps manage
> the middle and the end.

FACTORIES and REPOSITORIES have distinct responsibilities:
1. The FACTORY makes new objects;
2. The REPOSITORY finds old objects;

The client of a REPOSITORY should be given the illusion that the objects are in
memory. The object may have to be reconstituted, but it is the same conceptual
object, still in the middle of its life cycle.

The REPOSITORY can *delegate* object creation to a FACTORY, which (in theory,
though seldom in practice) could be used to create objects from scratch.

#### Designing Objects for Relational Databases

There are three common cases:

1. The database is primarily a repository for the objects;
2. The database was designed for another system
3. The database is designed for this system but servers in roles other than
   object store.

When the database schema is being created specifically as a store for the
objects, it is worth accepting some model limitations in order to keep the
mapping very simple.

It is crucial that the mappings be transperent, easily understandable by
inspecting the code or reading entiries in the mapping tool.

- When the database is being viewed as an object store, don't let the data model
  and the object model diverge far, regardess of the power of the mapping tools.
  Sacrifice some richness of object relationships to keep close to the
  relational model. Compromise some formal relational standards, such as
  normalization, if it helps simplify the object mapping;
- Processes outside the object system should not access such an object store.
  They could violate the invariants enforced by the objects. Also, their access
  will lock in the data model so that it is hard to change when the objects are
  refactored.

## Chapter Seven: Using the Language: An Extended Example

The whole chapter is an extended example, so I'm just gonna outline what I
gather I learned from it:

Process outlined:

1. Gather Scenarios to stress the given model
2. Solve the problem in a simple way - Derive a simple model that solves the
   problem
3. Understand what the user will do within the system: This will show you the
   applications that you have
4. Distinguish ENTITIES and VALUE OBJECTS: Assign identity to entities and work
   out what is an ENTITY and a VALUE OBJECT
5. Design the Associations: Qualify associations to reduce multiplicity, remove
   unecessary associations, make associations directional by understanding the
   model
6. Set Aggregate Boundaries: Refer back to how the user is going to use the data
   and understand where to set the boundaries of an aggregate.
7. Select Repositories: Not all ENTITIES need a repository. No Repository for
   ENTITY that exists within an AGGREGATE.
8. Walk through Scenarios: Stress the given model and see how you would
   implement the scenarios that you outlined. Understand contention and what
   happens in different scenarios that might be awkward &/or a bottleneck.
9. Refactor: Understand awkwardness and remodel to fix problems. Based on the
   context of the project, remove or add things that might be a problem. Make
   trade-offs.
10. Define MODULES: Find slices that provide cohesion and are intuitive
    explanations of the business of the software. Set directionality between
    modules and which can depend on which. Isolate your core domain and make it
    not depend on any other module

Connecting two systems:

1. When interacting with the model of a different system, it's wise to provide
   an **Anti-Corruption Layer**. This could be manifested by a SERVICE.
2. Do not bind the name of the service to the system being used, instead use a
   meaningful name;
3. When we interact with ENTITIES that exist in both models (e.g. Customers),
   create a translator
4. Hide the Interface and translation logic behind the Anti-Corruption Layer,
   the domain must be completely isolated from this;
5. Sometimes, to enable the connection we will need to add a concept from the
   other System to our model: When doing this **always check if we can remap
   that concept to something more general that makes sense for our system** and
   add the translation to the Anti-Corruption Layer
6. Do not add the logic of the connection to the Application Layer, refrain to
   only calling the systems and passing the result;

Performance Tuning:

1. Tune the performance only after you solved the problem to great detail!
2. Caching data can be done within the Anti-Corruption Layer to avoid requests
   from being fired, but still keeping the Application simple;

## Part 3: Refactoring Toward Deeper Insight

> The real challenge is to actually **_find_** an incisive model, one that
> captures subtle concerns of the domain experts and can drive a practical
> design. Ultimately, we hope to develop a model that captures a deep
> understanding of the domain.

Success developing useful models comes down to three points:

1. Sophisticated domain models are achievable and worth the trouble;
2. They are seldom developed except through an iterative process of refactoring,
   including close involvement of the domain experts with developers interested
   in learning about the domain;
3. They may call for sophisticated design skills to implement and to use
   effectively.

### Levels of Refactoring

> The refactorings that have the greatest impact on the viability of the system
> are those motivated by new insights into the domain or those that clarify the
> model's expression through code. This is refactoring to a deeper model.

The motivation of this kind of refactoring is not the state of the code. It's:

1. Providing change towards a more insightful model, aggregating knowledge into
   the software.
2. Making the developer not only understand *what* the code does, but also *why*
   the code does that and be able to relate that to the ongoing communication
   with the domain experts.

### Deeper Model

> Initial models usually are very naive and superficial, based on shallow
> knowledge

**_A deep model provides a lucid expression of the primary concerns of the
domain experts and their most relevant knowledge while it sloughs off the
superficial aspects of the domain_**

Versatility, simplicity, and explanatory power come from a model that is truly
in tune with the domain. One feature such models almost always have is a simple,
though possibly abstract, language that the business experts like to use.

### Deep Model/Supple Design

in the process of of constant refactoring, the design itself needs to support
change

The very act of transforming the model and code again and again can bring about
flexibility at just the points where change is most needed, along with easy ways
of doing the common things. So, although there is a lot of trial and error
involved in this approach to modeling and design, the changes can actually
become easier to make, and the repeated changes actually move us toward a supple
design.

A deep model makes possible an expressive design. At the same time, a design can
feed insight into the model discovery process when it has the flexibility to let
a developer experiment and the clarity to show a developer what is happening.

**The model we are looking for is the foundation of the system.**

### The Discovery Process

Because of the close relationship between model and design, the modeling process
comes to a halt when the code is hard to refactor. You will usually depend on
creativity and trial and error to find good ways to model the concepts you
discover, but sometimes someone has laid down a pattern you can follow. Such
patterns are never ready-made solutions, but they feed your knowledge crunching
process and narrow your search.

## Chapter Eight: Breakthrough

The returns from refactoring are not linear. Usually, there is a marginal return
for a small effort, and the small improvements add up. They find entropy, and
they are the frontline protection against a fossilized legacy, But, some of the
most valuable insights come abruptly and send a shock through the project.

Often, continuous refactoring prepares the way for something less orderly. Each
refinement of code and model gives developers a clearer view. This clarity
creates the potential for a breakthrough of insights. A rush of change leads to
a model that corresponds on a deeper level to the realities and priorities of
the users. Versatility and explanatory power suddenly increase even as
complexity evaporates.

> This sort of breakthrough is not a technique; it is an event. The challenge
> lies in recognizing what is happening and deciding how to deal with it.

A Breakthrough usually happened when:

1. Run through every scenario you have ever encountered relatively effortlessly,
   much more simply than ever before;
2. Your model diagrams make perfect sense to the business experts, which no
   longer indicate that they're too technical for them;
3. The clarity and simplicity of the new design, combined with the enhanced
   communication based on the new UBIQUITOUS LANGUAGE lead to even more insight;
4. Results in a clear and simple model which is reflected in an acceleration of
   the pace of development at a stage where projects begin tobog down in the
   mass and complexity of what has already been built.

The gospel of refactoring is that you always go in small steps, always keeping
everything working. But sometimes refactoring the code to a new, more insightful
model require changing a lot of support code, and there are a few, if any,
stopping points in between. When this happens, some useful questions:

1. How long would it take to get back to current functionality with the new
   design?
2. Could we solve the problems without it?
3. Would we be able to move forward in the next release if we didn't do it now?
4. Do *we* think it is the right thing to do?

Depending on the answers, even if pressure comes from above, the manager should
handle the heat and commit with the new design. Productivity usually will follow
in the next releases.

### Opportunities

When the prospect of a breakthrough to a deeper model presents itself, it is
often scary. Such a change has higher opportunity *and* higher risk than most
refactorings. And timing may be inopportune.

Much as we might like it to be otherwise, progress isn't a smooth ride. The
transition to a really deep model is a profound shift in your thinking and
demands a major change to the design. On many projects the most important
progress in model and design come in these breakthroughs.

### Focus on Basics

**Don't become paralyzed trying to bring about a breakthrough.** The possibility
usually comes after many modest refactorings. Most time is spent making
piecemeal improvements, with model insights emerging gradually during each
successive refinement.

**To set the stage for a breakthrough, concentrate on knowledge crunching** and
cultivating a robust UBIQUITOUS LANGUAGE:

1. Probe for important domain concepts and make them explicit in the model;
2. Refine the design to be suppler;
3. Distill the model;
4. Push on these more predictable levers, which increase clarity--usually a
   precursor of breakthroughs.

**Don't hold back from modest improvements.** They will gradually deepen the
model even if confined within the same general conceptual framework.

**Don't be paralyzed looking too far forward.** Just be watchful for the
opportunity.

## Chapter Nine: Making Implicit Concepts Explicit

The first step to modeling is yo somehow represent the essential concepts of the
domain in the model. Refinement comes later, after successive iterations of
knowledge crunching and refactoring. But this process really gets into gear when
an important concept is recognized and made explicit in the model and design.

Many transformations of domain models and the corresponding code happen when
developers recognize a concept that has been hinted at in discussion or present
implicitly in the design, and they then represent it explicitly in the model
with one or more objects or relationships.

### Digging Out Concepts

Most such discoveries come from listening to the language of the team,
scrutinizing awkwardness in the design and seeming contradictions in the
statements of experts, mining the literature of the domain, and doing lots and
lots of experimentation.

#### Listen to Language

Listen to the language the domain experts use. Are there terms that succinctly
state something complicated? Are they correcting your word choice (perhaps
diplomatically)? Do the puzzled looks on their faces go away when you use a
particular phrase? These are hints of a concept that might benefit the model.

This is *not* the old "nouns are objects" notion. A new word is simply a lead,
follow it up with knowledge crunching and conversation, with the goal of carving
out a clean, useful concept.

The UBIQUITOUS LANGUAGE is made up of the vocabulary that pervades speech,
documents, model diagrams, and even code. If a term is absent from the design,
it is an opportunity to improve the model and design by including it.

#### Scrutinize Awkwardness

The concept you need is not always floating on the surface, emerging in
conversation or documents. You may have to dig and invent. The place to dig is
the most awkward part of your design. The place where procedures are doing
complicated  things that are hard to explain. The place where every new
requirement seems to add complexity.

Engage the experts in the search. If you are lucky, they may enjoy playing with
ideas and experimenting with the model.

#### Contemplate Contradictions

Domain experts see things different ways based on experience and needs. This
creates contradictions. Some are just variations in terminology or are based on
misunderstanding. But there is a residue where two factual statements by experts
seem to contradict.

It is not practical to reconcile all contradictions, and it may not even be
desirable. However, even when a contradiction is left in place, contemplation of
**_how_** two statement scould both apply to the same external reality can be
revealing.

#### Read the book

Don't overlook the obvious when seeking model concepts. In many fields, you can
find books that explain the fundamental concepts and conventional wisdom. You
still have to work with your own domain experts to distill the part relevant to
your problem and to crunch it into something suited to object-oriented software.
But you may be able to start with a coherent, deeply considered view.

Even with ample support from domain experts, it pays to look at the literature
to get a grasp of the theory of the field.

#### Try, Try Again

You might have to follow half a dozen leads in conversation before finding one
that seems clear and useful enough to try out in the model. Additional
experience and knowledge crunching serve up better ideas. A modeler/designer
cannot afford to get attached to his own ideas.

Do not thrash the model, but rather embed deeper insight into it. Each
refactoring should leave the design more supple, easier to change the next time,
ready to bend the places that turn out to need to bend.

Experimentation is the way to learn what works and doesn't.

### How to model less obvious kinds of concepts

#### Explicit Constraints

They often emerge implicitly, and expressing them explicitly can greatly improve
a design.

Sometimes constraints find a natural home in an object method.

```java
class Bucket {
   private float capacity;
   private float contents;

   public void pourIn(float addedVolume) {
      if (contents + addedVolume > capacity) {
         contents = capacity;
      } else {
         contents = contents + addedVolume;
      }
   }
}

// VS

class Bucket {
   private float capacity;
   private float contents;

   public void pourIn(float addedVolume) {
      float volumePresent = contents + addedVolume;
      contents = constrainedToCapacity(volumePresent);
   }

   private float constrainedToCapacity(float volumePlacedIn) {
      if (volumePlacedIn > capacity) return capacity;

      return volumePlacedIn;
   }
}
```

The second version has a more obvious relationship to the model. When the rules
being enforced are more complex, they start to overwhelm the object or operation
they apply to, as any implicit concept does. Factoring the constraint in its own
method allows us to give it an intention-revealing name that makes the
constraint explicit in our design. It is now a named thing we can discuss.

There are lots of cases when a constraint just can't fit comfortably in a single
method. Or even if the method stays simple, it may call on information that the
object doesn't need for its primary responsibility. The rule may just have no
suitable home in an existing object.

🚨 Warning signs:

1. Evaluating a constraint requires data that does not otherwise fit the
   object's definition
2. Related rules appear in multiple objects, forcing duplication or inheritance
   between objects that are not otherwise a family
3. A lot of design and requirements conversations revolved around the
   constraints, but in the implementation, they are hidden away in procedural
   code.

When the constraints are obscuring the object's basic responsibility, or when
the constraint is prominent in the domain yet not prominent in the model, you
can factor it out into an explicit object or even model it as a set of objects
and relationships.

See [OverbookingPolicy example -- slide
8](https://www.cs.colorado.edu/~kena/classes/6448/s05/lectures/lecture23.pdf)

#### Processes as Domain Objects

We do *__not__* want to make procedures a prominent aspect of our model. Objects
are meant to encapsulate the procedures and let us think about their goals or
intentions instead.

Here Processes mean processes that exist in the domain, which we have to
represent in the model. When these emerge, they tend to make for awkward object
designs.

A SERVICE is one way of expressing a process explicitly, while still
encapsulating the extremely complex algorithms.

When there is more than one way to carry out the process, another approach is to
make the algorithm itself, or some key part of it, an object in its own right,
i.e. each implementation represents a STRATEGY.

The key to distinguishing a process that ought to be made explicit:

> Is this something the domain experts talk about, or is it just part of the
> mechanism of the computer program?

#### SPECIFICATION

Boolean test methods appear in all kinds of application that really part of
little rules. As long as they are simple, we handle them with testing methods.

Example:

```java
class Invoice {
   private Date dueDate;
   // ...
   public boolean isOverdue() {
      Date currentDate = new Date();
      return currentDate.after(dueDate);
   }
}
```

But not all rules are so simple. Example: `isDeliquent()` which may need to
check the account data, past payments, etc.

Developers working in the logic-programming paradigm would handle these
situations with *predicates*. Predicates are functions that evaluate "true" or
"false" and can be combined using operators such as "AND" and "OR" to express
more complex rules. With predicates we could declare rules explicitly and use
them with the **Invoice**.

**Business rules often do not fit the responsibility of any of the obvious
ENTITIES or VALUE OBJECTS, and their variety and combinations can overwhelm the
basic meaning of the domain object. But moving the rules out of the domain layer
is even worse, since the domain code no longer expresses the model.**

**Logic programming provides the concept of separate, combinable, rule objects
called "predicates", but full implementation of this concept with objects is
cumbersome. It is also so general that it doesn't communicate intent as more
specialized designs.**

Most of our rules fall into a few special cases. We can borrow the concept of
predicates and create specialized objects that evaluate to a Boolean.

These truth tests can evaluate other truth tests to see if the predicate is true
for that object. In that case, the new object is a *specification*. A
SPECIFICATION states a constraint on the state of another object, which may or
may not be present. It has multiple uses, but one that conveys the most basic
concept is that a SPECIFICATION can test any object to see if it satisfies the
specified criteria.

**Create explicit predicate-like VALUE OBJECTS for specialized purposes. A
SPECIFICATION is a predicate that determines if an object does or does not
satisfy some criteria.**

The SPECIFICATION keeps the rule in the domain layer. Because the rule is a
full-fledged object, the design can be a more explicit reflection of the model.
A FACTORY can configure a SPECIFICATION using information from other sources,
such as the customer's account or the corporate policy database.

##### Applying and Implementing SPECIFICATION

Much of the value of SPECIFICATION is that it unifies application functionality
that may seem quite different. We might need to specify the state of an object
for one or more of these three purposes.

1. **Validation:** To validate an object to see if it fulfills some need or is
   ready for some purpose
2. **Selection** To select an object from a collection (as in the case of
   querying for overdue invoices)
3. **Building:** To specify the creation of a new object to fit some need

These three are the same in a conceptual level. Applying the SPECIFICATION
pattern allows a consistent model to be used, even when the implementation may
have to diverge.

###### Validation

Example:

```java
class DelinquentInvoiceSpecification extends InvoiceSpecification {
   private Date currentDate;

   public DelinquentInvoiceSpecification(Date currentDate) {
      this.currentDate = currentDate;
   }

   public boolean isSatisfiedBy(Invoice candidate) {
      int gracePeriod = candidate.customer().getPaymentGracePeriod();
      Date firmDeadline = DateUtility.addDaysToDate(
         candidate.dueDate(),
         gracePeriod
      );

      return currentDate.after(firmDeadline);
   }
}

public boolean accountIsDelinquent(Customer customer) {
   Date today = new Date();
   Specification delinquentSpec = new DelinquentInvoiceSpecification(today);
   Iterator it = customer.getInvoices().iterator();
   while (it.hasNext()) {
      Invoice candidate = (Invoice) it.next();
      if (delinquentSpec.isSatisfiedBy(candidate)) return true;
   }

   return false;
}
```

###### Selection (or Querying)

Example:

```java
public Set selectSatisfying(InvoiceSpecification spec) {
   Set results = new HashSet();
   Iterator it = invoices.iterator();
   while(it.hasNext()) {
      Invoice candidate = (Invoice) it.next();
      if (delinquentSpec.isSatisfiedBy(candidate)) results.add(candidate);
   }

   return results;
}

Set delinquentInvoices = invoiceRepository.selectSatisfying(
   new DelinquentInvoiceSpecification(currentDate)
);
```

SQL is a very natural way to write SPECIFICATIONS. A simple example with a db
query:

```java
class DelinquentInvoiceSpecification extends InvoiceSpecification {
   // ...
   public String asSQL() {
      return
         "SELECT * FROM INVOICE, CUSTOMER" +
         "  WHERE INVOICE.CUST_ID = CUSTOMER.ID" +
         "  AND INVOICE.DUE_DATE + CUSTOMER.GRACE_PERIOD" +
         "    < " + SQLUtility.dateAsSQL(currentDate);
   }
}
```

This has a problem that the SQL language has crept into the domain layer.
Depending on what you use, however, we can translate models and relationships to
SQL queries automatically.

SPECIFICATIONS mesh smoothly with REPOSITORIES. Avoid coupling your domain layer
code with your infrastructure. Some ways to avoid are:

*1. ORM Mapping*

*2. Adding the query to the repository and using it in the specification:*

```java
public class InvoiceRepository {
   // ...
   public Set selectWhereGracePeriodPast(Date aDate) {
      String sql = whereGracePeriodPast_SQL(aDate);
      ResultSet queryResultSet = SQLDatabaseInterface.instance().executeQuery(sql);

      return buildInvoicesFromResultSet(queryResultSet);
   }

   public String whereGracePeriodPast_SQL(Date aDate) {
      return
         "SELECT * FROM INVOICE, CUSTOMER" +
         "  WHERE INVOICE.CUST_ID = CUSTOMER.ID" +
         "  AND INVOICE.DUE_DATE + CUSTOMER.GRACE_PERIOD" +
         "    < " + SQLUtility.dateAsSQL(aDate);
   }

   public Set selectSatisfying(InvoiceSpecification spec) {
      return spec.satisfyingElementsFrom(this);
   }
}

public class DelinquentInvoiceSpecification {
   // ...
   public Set satisfyingElementsFrom(InvoiceRespository repository) {
      return repository.selectWhereGracePeriodPast(currentDate);
   }
}
```

This puts the SQL in the REPOSITORY, while the SPECIFICATION controls what query
should be used.

*3. Selecting more from the database and filtering in memory*

```java
public class InvoiceRepository {
   public Set selectWhereDueDateIsBefore(Date aDate) {
      String sql = whereDueDateIsBefore_SQL(aDate);
      ResultSet queryResultSet = SQLDatabaseInterface.instance().executeQuery(sql);

      return buildInvoicesFromResultSet(queryResultSet);
   }

   public String whereDueDateIsBefore_SQL(Date aDate) {
      "SELECT * FROM INVOICE" +
         "  WHERE INVOICE.DUE_DATE" +
         "    < " + SQLUtility.dateAsSQL(aDate);
   }

   public Set selectSatisfying(InvoiceSpecification spec) {
      return spec.satisfyingElementsFrom(this);
   }
}

public class DelinquentInvoiceSpecification {
   public Set satisfyingElementsFrom(InvoiceRepository repository) {
      Collection pastDueInvoices = repository.selectWhereDueDateIsBefore(currentDate);

      Set delinquentInvoices = new HashSet();
      Iterator it = pastDueInvoices.iterator();
      while(it.hasNext()) {
         Invoice anInvoice = (Invoice) it.next();
         if (this.isSatisfiedBy(anInvoice)) {
            delinquentInvoices.add(anInvoice);
         }

         return delinquentInvoices;
      }
   }
}
```

This might be wasteful, since we're querying more and filtering in memory, but
that greatly depends on the circumstances.

###### Building to Order (Generating)

We can specify criteria for objects that are not yet present.

An interface of a generator that is defined in terms of a descriptive
SPECIFICATION explicitly constrains the generator's products. This approach has
several advantages.

- The generator's implementation is decoupled from its interface. The
  SPECIFICATION declares the requirements for the output but does not define how
  that result is reached.
- The interface communicates its rules explicitly, so developers know what to
  expect from the generator without understanding all defailts of its operation.
  The only way to predict the behavior of a procedurally defined generator is to
  run cases or to understand every line of code.
- The interface is more flexible, or can be enahnced with more flexibiliy,
  because the statement of the request is in the hands of the client, while the
  generator is only obligated to fulfill the letter of the SPECIFICATION.
- Last, but not least, this kind of interface is easier to test, because the
  model contains an explicit way to define input into the generator *that is
  also a vliadtion of the output.* That is, the same SPECIFICATION that is
  passed into the generator's interface to constrain the creation process can
  also be used, in its validation role (if the implementation supports it) to
  confirm that the created object is correct

*Building to order* can mean creation of an object from scratch, but it can also
be a configuration of preexisting objects to satisfy the SPEC.

Example:

```java
public class ContainerSpecification {
   private ContainerFeature requiredFeature;

   public ContainerSpecification(ContainerFeature required) {
      requiredFeatured = required;
   }

   boolean isSatisfiedBy(Container aContainer) {
      return aContainer.getFeatures().contains(requiredFeature);
   }
}

public class Container {
   private double capacity;
   private Set contents; // Drums

   public boolean hasSpaceFor(Drum aDrum) {
      return remainingSpace() >= aDrum.getSize();
   }

   public double remainingSpace() {
      double totalContentSize = 0.0;
      Iterator it = contents.iterator();
      while(it.hasNext()) {
         Drum aDrum = (Drum) it.next();
         totalContentSize = totalContentSize + aDrum.getSize();
      }

      return capacity - totalContentSize;
   }

   public boolean canAccommodate(Drum aDrum) {
      return hasSpaceFor(aDrum) &&
         aDrum.getContainerSpecification().isSatisfiedBy(this);
   }
}

public class PrototypePacker implements WarehousePacker {
   public void pack(Collection containers, Collection drums)
      throws NoAnswerFoundException {
         Iterator it = drums.iterator();
         while (it.hasNext()) {
            Drum drum = (Drum) it.next();
            Container container = findContainerFor(container. drum);
            container.add(drum);
         }
   }

   public Container findContainerFor(Collection containers, Drum drum) {
      Iterator it = containers.iterator();
      while (it.hasNext()) {
         Container container = (Container) it.next();
         if (container.canAccommodate(drum)) return container;
      }

      throw new NoAnswerFoundException();
   }
}
```

## Chapter Ten: Supple Design

> The ultimate purpose of software is to server users. But first, that same
> software has to server developers. people have to work with this stuff. But
> will they want to?

When software with complex behavior lacks a good design, it becomes hard to
refactor or combine elements. When software doesn't have a clean design,
developers dread even looking at the existing mess, much less making a change
that could aggravate the tangle or break something through an unforeseen
dependency. In any but the smallest systems, this fragility places a ceiling on
the richness of behavior it is feasible to build. It stops refactoring and
iterative refinement.

To have a project accelerate as development proceeds--rather than get weigthed
down by its own legacy--demands a design that is a pleasure to work with,
inviting to change. A supple design.

Once you have dug out implicit concepts and made them explicit, you have the raw
material. Through the iterative cycle, you hammer that material into a useful
shape, cultivating a model that simply and clearly captures the key concerns,
and shaping a design that allows a client developer to really put that model to
work.

A lot of overengineering has been justified in the name of flexibility. But more
often than not, excessive layers of abstraction and indirection get in the way.
Look at the design of software that really empowers the people who handle it;
you will usually see something simple. Simple is not easy.

Developers play two roles:

1. Developer of a client: Weaves the domain objects into the application code or
   other doamin layer code, utilizing capabilities of the design. The client
   developer can flexibly use a minimal set of loosely coupled concepts to
   express a range of scenarios in the domain. Design elements fit together in a
   natural way with a result that is predicatable, clearly characterized, and
   robust;
2. Developer who needs to change it: To be open to change, a design must be easy
   to understand, revealing that *same* underlying model that the client
   developer is drawing on. It must follow the contours of a deep model of the
   domain, so most changes bend the design at flexible points. The effects of
   its code must be transparently obvious, so the consequences of a change will
   be easy to anticipate.

When complexity is holding back progress, honing the most crucial, intricate
parts to a supple design makes the difference between getting sucked down into
legacy maintenance and punbching through the complexity ceiling

![Supple design patterns. The image shows a graph with several design patterns
that will be explained in the following
sections](./assets/supple-design-patterns.png "Patterns that contribute to a
Supple Design") *Patterns that contribute to a supple design*

### Intention Revealing Interfaces

If the interface doesn't tell the client developer what he needs to know in
order to use the object effectively, he will have to dig into the internals to
understand the details anyway.

If a developer must consider the implementation of a component in order to use
it, the value of encapsulation is lost. If someone other than the original
developer must infer the purpose of an object or operation based on its
implementation, that new developer may infer a purpose that the operation or
class fulfills only by chance. If that was not the intent, the code may work for
the moment, but the conceptual basis of the design will have been corrupted, and
the two developers will be working at cross-purposes.

All public elements of a design together make up its interface, and the name of
each of those elements presents an opportunity to reveal the intention of the
design.

Name classes and operations to describe their effect an purpose, without
reference to the means by which they do what they promise. This relieves the
client developer of the need to understand the internals. These names should
conform to the UBIQUITOUS LANGUAGE so that team members can quickly infer their
meaning. **Write a test for a behavior before creating it, to force your
thinking into client developer mode.**

All the tricky mechanism should be encapsulated behind abstract interfaces that
speak in terms of intentions, rather than means.

In public interfaces of the domain, state relationships and rules but not how
they are enforced; describe events and actions, but not how they are carried
out. Pose the question, but don't present the means by which the answer shall be
found.

Entire subdomains can be carved off into separate modules and encapsulated
behind INTENTION-REVEALING INTERFACES.

Complex logic can be done safely in SIDE-EFFECT-FREE FUNCTIONS. Methods that
change system state can be characterized with ASSERTIONS.

### Side-Effect-Free Functions

Operations can be divided into two categories:

1. Commands (or modifiers): Operations that affect some change to the systems
   and
2. Queries: Obtain information from the system, possibly by simply accessing
   data in a variable, possibly performing a calculation based on that data.

Elements of a complex design interact in ways that are likely to produce
unpredictability. The use of the term *side effect* underlines the inevitability
of that interaction.

Interactions of multiple rules or compositions of calculations become extremely
difficult to predict. The developer calling an operation must understand its
implementation and the implementation of all its delegations in order to
anticipate the result. The usefulness of any abstraction of interfaces is
limited if the developers are forced to pierce the veil. Without safely
predictable abstractions, the developers must limit the combinatorial explosion,
placing a low ceiling on the richness of behavior that is feasible to build.

Operations that return results without producing side effects are called
*functions*. Functions lower risk and are easier to test.

You can't avoid commands in most software systems, but the problems can be
mitigated in two ways:

1. Segregate queries from commands completely. Ensure that the methods that
   cause changes do not return domain data and are kept as simple as possible.
   I.e. perform all queries and calculations in methods that cause no observable
   side effects;
2. There are often alternative models and designs that do not call for an
   existing object to be modified at all: create and return a new VALUE OBJECT
   representing the calculation unlike an ENTITY who's life cycle is carefully
   regulated

VALUE OBJECTS are immutable. So apart from the constructor, all of their
operations are functions.

Place as much of the logic of the program as possible into functions, operations
that return results with no observable side effects. Strictly segregate commands
(methods that result in modifications to observable state)into very simple
operations that do not return domain information. Further control side effects
by moving complex logic into VALUE OBJECTS when a concept fitting the
responsibility presents itself.

### Assertions

ASSERTIONS make side effects explicit and easier to deal with.

In a design where larger parts are built of smaller ones, a command may invoke
other commands. Object interfaces do not restrict side effects so the developer
using them will want to know which is which to anticipate the consequences. This
will breach encapsulation, abstraction and polymorphism.

When the side effects of operations are only defined implicitly by their
implementation, designs with a lot of delegation become a tangle of cause and
effect. The only way to understand a program is to trace execution trough
branching paths. The value of encapsulation is lost. The necessity of tracing
concrete execution defeats abstraction.

We need a way of understanding the meaning of a design element and the
consequences of executing an operation without delving into its internals.

State post-conditions of operations and invariants of classes and AGGREGATES. If
ASSERTIONS cannot be coded directly in your programming language, write
automated unit tests for them. Write them into documentation or diagrams where
it fits the style of the project's development process.

Seek models with coherent sets of concepts, which lead a developer to infer the
inteded ASSERTIONS, accelerating the learning curve and reducing the risk of
contradictory code.

The communicativeness of the INTENTION-REVEALING INTERFACES, combined with the
predictability given by SIDE-EFFECT-FREE FUNCTIONS and ASSERTIONS, should make
encapsulation and abstraction safe.

The next ingredient in recombinable elements is effective decomposition.

### Conceptual Contours

When elements of a model or design are embedded in a monolithic construct, their
functionality gets duplicated. The external interface doesn't say everything a
client might care about. Their meaning is hard to understand, because different
concepts are mixed together.

On the other hand, breaking down classes ad methods can pointlessly complicate
the client, forcing client objects to understand how tiny pieces fit together.
Worse, a concept can be lost completely. Half of a uranium atom is not uranium.
And of course, it isn't just grain size that counts, but just where the grain
runs.

There is a logical consistency deep in most domains. Because of this underlying
consistency, when we find a model that resonates with some part of the domain,
it is more likely to be consistent with other parts that we discover later.
Sometimes the new discovery isn't easy for the model to adapt to, in which case
we refactor to deeper insight, and hope to conform to the *next* discovery.

Repeated refactoring eventually leads to suppleness. The CONCEPTUAL CONTOURS
emerge as the code is adapted to newly understood concepts or requirements.

With each decision, ask yourself, "Is this an expedient based on a particular
set of relationships in the current model and code, or does it echo some contour
of the underlying domain?"

Each object should be a single complete concept, a "WHOLE VALUE".

Decompose design elements (operations, interfaces, classes and AGGREGATES) into
cohesive units, taking into consideration your intuition of the important
divisions in the domain. Observe the axes of change and stability through
successive refactorings and look for the underlying CONCEPTUAL CONTOURS that
explain these shearing patterns. Align the model with the consistent aspects of
the domain that make it a viable area of knowledge in the first place.

The goal is a simple set of interfaces that combine logically to make sensible
statements in the UBIQUITOUS LANGUAGE, and without the distraction and
maintenance burden of irrelevant options.

---

INTENTION-REVEALING INTERFACES allow clients to present objects as units of
meaning rather than just mechanisms. SIDE-EFFECT-FREE FUNCTIONS and ASSERTIONS
make it safe to use those units and make complex combinations. The emergence of
CONCEPTUAL CONTOURS stabilizes parts of the model and also makes the units more
intuitive to use and combine.

We can still run into conceptual overload when interdependencies force us to
think about too many of these things at a time...

### Standalone Classes

Even within a MODULE, the difficulty of interpreting a design increases wildly
as dependencies are added. This adds to mental overload, limiting the design
complexity a developer can handle. Implicit concepts contribute to this load
even more than explicit references.

Every dependency is suspect until proven basic to the concept behind the object.
This scrutiny starts with the factoring of the model concepts themselves. Then
it requires attention to each individual association and operation. Model and
design choices can chip away at dependencies--often to zero.

Low coupling is fundamental to object design. When you can go all the way.
Eliminate *all* other concepts from the picture. Then the class will be
completely self-contained and can be studied and understood alone. Every such
self-contained class significantly eases the burden of understanding a MODULE.

The goal is not to eliminate all dependencies, but to eliminate all nonessential
ones.

Try to factor the most intricate computations into STANDALONE CLASSES, perhaps
by mdeling VALUE OBJECTS held by the more connected classes.

---

Low coupling is a basic way to reduce conceptual overload. A STANDALONE CLASS is
an extreme of low coupling.

Eliminating dependencies should not mean dumbing down the model by arbitrarily
reducing evertyhing to primitives.

### Closure of Operations

When a dependency is fundamental to the concept it isn't a bad thing.

Most interesting objects end up doing things tha can't be characterized by
primitives alone.

Another common practice in refined designs is "CLOSURE OF OPERATIONS". That
comes from mathematics, e.g. 1+1 = 2, the addition operation is closed under the
set of real numbers (R + R will be contained in R). The property of closure
tremendously simplifies the interpretation of an operation, and it is easy to
think about chaining together or combining closed operations.

Where it fits, define an operation whose return type is the same as the type of
its argument(s). If the implementer has state that is used in the computaton.
then the implementer is effectively and argument of the operation, so the
argument(s) and return value should be of the same type as the implementer. Such
an operation is closed under the set of instances of that type. A closed
operation provides a high-level interface without introducing any dependency on
other concepts.

This pattern is most often applied to the operations of a VALUE OBJECT.

### Declarative Design

No matter how MODEL-DRIVEN our design is, we still end up writing procedures to
produce the effect of the conceptual interactions.

INTENTION-REVEALING INTERFACES and the other patterns in this chapter help, but
they can never give conventional object-oriented programs formal rigor.

These are some of the motivations behind *declarative design*: A way to write a
program, or some part of a program, as a kind of executable specification.

Generating a running program from a declaration of model properties is a kind of
Holy Grail of MODEL-DRIVEN-DESIGN, but it does have its pitfalls in practice:

- A declaration language not expressive enough to do everything needed, but a
  framework that makes it very difficult to extend the software beyond the
  automated portion
- Code-generation techniques that cripple the iterative cycle by merging
  generated code into handwritten code in a way that makes regeneration
  destructive

The unintended consequence of many attempts at declarative design is the
dumbing-down of the model and application.

> The greatest value I've seen delivered has been when a narrowly scoped
> framework automates a particularly tedious and error-prone aspect of the
> design , such as persitence and object-relational mapping. The best of these
> unburden developers of drudge work while leaving them complete freedom to
> design.

### Domain-Specific Languages

In this style, client code is written in a programming language tailored to a
particular model.

This can cause:

1. Difficulty to refactor client code given changes in the model
2. High learning to be able to create these languages


### A Declarative Style of Design

Once your design has INTENTION-REVEALING INTERFACES, SIDE-EFFECT-FREE FUNCTIONS,
and ASSERTIONS, you are edging into declarative territory. Many of the benefits
of declarative design are obtained once you have combinable elements that
communicate their meaning, and have characterized or obvious effects, or no
observable effects at all.

### Extending SPECIFICATIONS in a Declarative Style

SPECIFICAtION is an adaption of an established formalism, the predicate.
Predicates have other useful properties that we can draw on, selectively.

#### *Combining* SPECIFICATIONS Using Logical Operators

```java
public interface Specification {
   boolean isSatisfiedBy(Object candidate);
   Specification and(Specification other);
   Specification or(Specification other);
   Specification not();
}
```

Using a Composite:

```java
public abstract class AbstractSpecification implements Specification {
   public Specification and(Specification other) {
      return new AndSpecification(this, other);
   }

   public Specification or(Specification other) {
      return new OrSpecification(this, other);
   }

   public Specification not() {
      return new NotSpecification(this);
   }
}

public class AndSpecification extends AbstractSpecification {
   Specification one;
   Specification two;

   public AndSpecification(Specification x, Specification y) {
      one = x;
      other = y;
   }

   public boolean isSatisfiedBy(Object candidate) {
      return one.isSatisfiedBy(candidate) &&
         other.isSatisfiedBy(candidate);
   }
}

public class OrSpecification extends AbstractSpecification {
   Specification one;
   Specification two;

   public AndSpecification(Specification x, Specification y) {
      one = x;
      other = y;
   }

   public boolean isSatisfiedBy(Object candidate) {
      return one.isSatisfiedBy(candidate) ||
         other.isSatisfiedBy(candidate);
   }
}

public class AndSpecification extends AbstractSpecification {
   Specification wrapped;

   public AndSpecification(Specification x) {
      wrapped = x;
   }

   public boolean isSatisfiedBy(Object candidate) {
      return !one.isSatisfiedBy(candidate);
   }
}
```

There are situations where this may be inefficient. Other implementations
options are possible that would minimize object count or boost speed. The
important thing is a model that captures the key concepts of the domain, along
with an implementation that is faithful to that model. That leaves a lot of room
to solve performance problems.

Using a pattern doesn't mean building features you don't need. They can be added
later, as long as the concepts don't get muddled.

#### Subsumptions

```
NewSpec implies OldSpec ?
---
NewSpec → OldSpec
```

Proving a logical implication in a general way is very difficult, but special
cases can be easy.

```java
public class MinimumAgeSpecification {
   int threshold;

   public boolean isSatisfiedBy(Person candidate) {
      return candidate.getAge() >= threshold;
   }

   public boolean subsumes(MinimumAgeSpecification other) {
      return threshold >= other.getThreshold();
   }
}
```

Other way is using the AND operator, because `A AND B → A`.

```java
public boolean subsumes(Specification other) {
   if (other instanceof CompositeSpecification) {
      Collection otherLeaves =
         (CompositeSpecification) other.leafSpecifications();
         Iterator it = otherLeaves.iterator();
         while (it.hasNext()) {
            if (!leafSpecifications().contains(it.next()))
               return false;
         }
   } else {
      if (!leafSpecifications().contains(other))
         return false;
   }

   return true;
}
```

### Angles of attack

This chapter has presented a raft of techniques to clarify the intent of code,
to make the consequences of using it transparent, and to decouple model
elements. Even so, this kind of design is difficult. You can't just look at an
enormous system and say, "Let's make this supple." You have to choose targets.

#### Carve Off Subdomains

Some aspects of the system will suggest approaches to you, and they can be
factored out and worked over.

Examples:

- You may see a part of the model that can be viewed as specialized math;
  separate that
- Your application enforces complex rules restricting state changes; pull this
  out into a separate model or simple framework that lets you declare the rules.

With each small step, the new module will be cleaner, but also the part left
behind is smaller.

It is more useful to make a big impact on one area, making a part of the design
really supple, than yo spread your efforts thin.

#### Draw on Established Formalisms, When You Can

You can often use and adapt conceptual systems that are long established in your
domain or others, some of which have been refined and distilled over centuries.

---

Supple Design has a profound effect on the ability of software to cope with
change and complexity. It often hinges on quite detailed modeling and design
decisions. The impact can go beyond a specific modeling and design problem.

## Chapter Eleven: Applying Analysis Patterns

When an experienced developer looking at a domain problem sees a familiar sort
of responsibility or a familiar web of relationships, he or she can draw on the
memory of how the problem was solved before. Some of these patterns have been
documented and shared, allowing the rest of us to draw on the accumulated
experience.

These patterns let us cut through expensive trial and error to start with a
model that is already expressive and implementable and addresses subtleties that
might be costly to learn. From that starting point, we refactor and experiment.
These are not out-of-the-box solutions.

> Analysis patterns are groups of concepts that represent a common construction
> in business modeling. It may be relevant to only one domain or it may span
> many domains.

What the name unfortunately does *not* convey is that there is significant
discussion of implementation in these patterns, including some code. Fowler
understands the pitfalls of analysis without thought for practical design. Here
is an example where he is looking at the implactions of specific model choices
on the maintenance of the system:

> When we build a new [accounting] practice, we create a network of new
> instances of the posting rule. We can do this without any recompilation or
> rebuilding of the system, while it is still up and running. There will be
> unavoidable occasions when we need a new subtype of posting rule, but these
> will be rare.

Experience avoids problems. Code that is tried and tested avoids problems.
Analysis patterns at their best can carry that kind of experience from other
projects combining model insights with extensive discussions of design
directions and implementation consequences. To discuss model ideas out of that
context makes them harder to apply and risks opening the deadly divide between
analysis and design, which is antithetical to MODEL-DRIVEN-DESIGN.

Obs.: The examples in this chapter are valuable and carry almost all of what the
content of the chapter actually is.

They attempt to show that:

1. You need to adapt the Analysis patterns to your domain and use case;
2. Reshow this to domain experts and re-evaluate;
3. Infrastructure and code might make you have to change your model;
4. The clarity of the new design might expose new problems.
5. Sometimes you need to add the "Firing methods" of things that are done
   event-based or in batches to your model. I.e. you may need a model driven
   design for your batch scripts or consumers;

### Analysis Patterns Are Knowledge to Draw On

When you are lucky enough to have an analysis pattern, it hardly ever is the
answer to your particular needs. Yet it offers valuable leads in your
investigation, and it provides cleanly abstracted vocabulary. It should also
give you guidance about implementation consequences that will save you pain down
the road.

There is one kind of change you should avoid. When you use a term from a
well-known analysis pattern, take care to keep the basic concept it designates
intact, however much the superficial form might change. There are two reasons
for this:

1. The pattern may embed understanding that will help you avoid problems;
2. (more important) your UBIQUITOUS LANGUAGE is enhanced when it includes terms
   that are widely understood or at least well explained. If your model
   definitions change through the natural evolution of the model, take the
   trouble to change the names too.

Only a few of the Analysis Patterns available have captured the reasoning behind
the choices and the consequences that follow, which are the most useful parts of
an analysis pattern.

This kind of reapplication of organized knowledge is completely different from
attempts to reuse code through frameworks or components, except that either
could provide the seed of an idea that is not obvious. A model, even a
generalized framework, is a complete working whole, while an analysis is a kit
of model fragments. Analysis patterns focus on the most critical and difficult
decisions and illuminate alternatives and choices. They anticipate downstream
consequences that are expensive if you have to discover them for yourself.

## Chapter Eleven: Relating Design Patterns to the Model
