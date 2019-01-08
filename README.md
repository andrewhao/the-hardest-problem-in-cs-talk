# Conquering the hardest problem in computer science!*

* Seriously

## Intro

### Intro quote

"There are only two hard things in computer science; naming and cache invalidation"

"There are only two hard things in computer science: naming, cache invalidation and off-by-one errors"

### The hardest thing? Really?

Really harder than:

- scaling & performance?
- concurrency & distributed systems?
- blockchain?
- machine learning, artificial intelligence?

### Naming is hard!

Because it has to do with readability and maintainability.

It has to do with making a cohesive system that is elegantly mapped into parts

## Names & Semiotics

We turn to the field of semiotics - the construction and communication of meaning

### Signs: Signifier and Signified

(Photo of rose): What is this?

(Audience guess)

Right, a rose.

We call this a "signifier". It's a concrete thing that represents a concept.

A rose's signifier can be an image of a rose, or the word "ROSE".


### Signs: Signified

But more than just a "rose", there is additional meaning attached to it. When you see a rose, what are some concepts you attach to it?

(Audience participation)

Love, passion, romance.

This is the "signified" - when a rose appears in an advertisement, or story, or you are given one in real life, you understand this appears in the context of romantic love.

How did you associate this with love, passion, romance? These notions and patterns are embedded in our culture.

if you asked someone what a rose meant from an East Asian culture, they may shrug since there isn't a cultural association!

Takeaway: in the field of semiotics, we generally agree that there is no such thing as a "universal truth" of sign == signifier that everyone can agree on. There is usually a cultural lens - the signified - that depends on the eye of the beholder.

### A Sign is Signifier + Signified

Semiotics is the study of signs!

Semiotics is typically applied to how we understand and perceive messages, and the meanings that are applied to them.

### Signs in your software systems

But the same thing appears in software too!

A UserFactory could be the signifier. It could be the reference to the class, or the class definition itself.

However, the "signified" is the concept behind the class name or the class itself. In our software system, the UserFactory signifies an OO class that constructs an instance of a User object, which itself is a signifier for the concept of a User, which hopefully maps to a real user in your business.

Let's apply semiotic theory here. If you asked ten people on your team what the UserFactory does, you may get 10 different answers (or not). If an engineer is not familiar with the Factory pattern, they may see things differently than somebody who does. If you asked someone in the Marketing team what a User is, they may be confused since they don't refer to customers as users.

Takeaway: our Cultural contexts are different. IOW, our subjective understanding of the way our business operates varies from team member to team member (if you have any).

### If you don't have the same cultural lens of your software system, you won't write clear software

The Hebrew story goes that the Tower of Babel was mankind's greatest feat, an act of hubris where the world was to make a tower so tall it would reach Heaven. God saw man's hubris and causes the workers to speak different tongues. In the confusion that ensued, the project fell apart and the tower was destroyed.

The takeaway is clear: if you want to accomplish anything together, you need to speak the same language.

## Tips on getting on the same linguistic page

Much of this is drawn from DDD by Eric Evans

### Acknowledge the different cultural contexts at play in your org!

Put on your anthropologist's hat: 

Your Growth team speaks a different lingo than your
Finance Operations team, different from your
Customer Support team, different from the
Legal team,
Core Services team, ...

An "Account" means one thing in Legal, versus in your Identity Access.

Here's the thing - your software systems need to ALLOW for that flexibility.

### Document the language that is spoken by the business.

Ubiquitious language

Build a Glossary

Note that a Ubiquitous Language doesn't literally mean ubiquitious, it just means within your particular tribe

### Refactor terms to match real biz terms

Don't let your software system evolve out of whack. Less layers of indirection

### Build a software boundary around each tribal language

Bounded Context

Then build adapter layers when translating between each language! (Anti-Corruption Layer)

## More General Tips on Naming

A good name is specific. Avoid lazy naming conventions...

It's not a AppointmentList, it's a Calendar
It's not a PlaceCollection, it's an Itinerary
It's not an InvoiceManager, it's a BillingFlow
etc etc.

## Change: destroyer of systems

Your biggest enemy is change:

- the business pivots
- another team starts working in the code base and the terms start to drift
- an employee leaves, taking a large chunk of institutional knowledge with her

Your biggest tool is knowledge, vigilance and documentation

Be aware of when things change!

- the business pivots: so start drafting up some ideas to rename or remove concepts.

Your system is defined by what is *not* there as much as there *is*. Minimalism.

- another team starts working in the code base and the terms start to drift

Code reviews are a great place to discuss naming. 
Architecture review discussions are good places to ask "is this the right name?"

- an employee leaves, taking a large chunk of institutional knowledge with her

Anticipate her departure, and sit down with her and collaboratively write down the things you need to know.

pair program to download understanding.

## With your new Linguistic X-Ray Vision,

### From the field of Semiotics, we understand that signs (code) is only as good as the cultural contexts they are written in.

Therefore: invest energy in integrating everyone into that context.

### Change can slowly cause chaos with ambiguity.

Therefore: Derive clear names from the business. Clear away everything that can be confusing. Invest energy into cleaning things up.

### Names conflict, overlap and diverge depending on the cultural context (business context).

Therefore: Allow each part of the system to have its own cultural context, bounded by real software boundaries (systems)

### Doing business with software (& coding) is a social activity.

Therefore: Discuss with each other. Discuss with business. Collaboratively develop vocabularies.

