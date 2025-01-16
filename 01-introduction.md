<p><a target="_blank" href="https://app.eraser.io/workspace/0aExo6JApaYi0ECiWX0X" id="edit-in-eraser-github-link"><img alt="Edit in Eraser" src="https://firebasestorage.googleapis.com/v0/b/second-petal-295822.appspot.com/o/images%2Fgithub%2FOpen%20in%20Eraser.svg?alt=media&amp;token=968381c8-a7e7-472a-8ed6-4a6626da5501"></a></p>

# Introduction
>  [﻿Watch video](https://www.youtube.com/watch?v=WXIuQQGrUsQ&t=412) for more details and discussions

Software Architecture as a career does not have a clear career path because of several reasons:

1. The industry doesn't have a clear definition of what "software architecture" is. When asked, the authors of this book refused to provide one. Martin Fowler in his famous whitepaper [﻿"Who Needs an Architect"](https://martinfowler.com/ieeeSoftware/whoNeedsArchitect.pdf)  refused to define it and used the famous quote: _"Architecture is about the important stuff... whatever that is"_ - Ralph Johnson.
2. The software architect's scope of responsibilities is massive, and it continues to expand. At one point, architects only dealt with the technical aspects of architecture, but nowadays their scope includes soft skills, operational awareness, and many other responsibilities aside from the technical abilities. The authors created a mind map that's indicative of the scope of software architecture (incomplete, redrawn by me):
[﻿responsibility-of-software-architect](https://app.eraser.io/workspace/0aExo6JApaYi0ECiWX0X?elements=xN5rA-lCiu4P8iaFusvQWw)  
3. Because software evolves rapidly, creating a definition for software architecture today will most likely be outdated in a few years.
4. Resources and materials on software architecture have only historical relevance. They're things that architects have tried, only to realize the damaging side effects some time later. Solutions that were once valid cannot work now because the context has changed.
## Defining Software Architecture
Some architects think of the architecture as the _blueprint_ of the system, others as the _roadmap_ for developing it. The issue is understanding what both the blueprint and roadmap actually contain. When an architect analyzes an architecture, what is analyzed?

Software architecture consists of:

- _Structure_
    - Type of architecture style(s), like microservices, layered, or micro kernel.
    - Structure doesn't define the architecture itself
    - If we say our application is built with "microservices architecture" we're referring to the structure, not the overall architecture
- _Architecture characteristics_ (so called "-ilities")
    - Availability, Reliability, Testability, Scalability, Security, Agility, Fault Tolerance, Elasticity, Recoverability, Performance, Deployability, Learnability
    - Define the _success criteria of the system_, which is independent of the system's functionality
    - For example, microservices or not, if we want to support _Testability_ we need to design our software to be (easily) testable
- _Architecture decisions_
    - Rules for how a system should be constructed
    - For example, we can make a decision that only the business and services layers within a layered architecture can access the database, and prevent the presentation layer from directly querying the database
    - They form constraints and inform the dev teams what is and what isn't allowed
    - Decisions can also be broken through so called _variances_. Dev teams can submit a variance for a specific standard or decision, explain why it needs to be broken or can't be implemented, and that variant can either be accepted or denied by the chief architect or the Architecture Review Board (ARB) if it exists
- _Design principles_
    - Similar to decisions, but instead are more _guidelines_ rather than _rules_
    - For example, in order to increase performance, the architect can suggest dev teams to leverage async messaging between services within a microservice architecture
    - While an _architectural decision_ defines exact constraints, _design principles_ allow more freedom to developers to choose an appropriate solution
## Expectations of an Architect
Defining the role of an architect is as difficult as defining software architecture. But regardless of the definition, there are eight core expectations of software architects:

- Make architecture decisions
    - _An architect is expected to define the architecture decisions and design principles used to guide technology decisions within the team, the department, or across the enterprise_
    - The key word is _guide_. An architect should _guide_ rather than _specify_ technology choices
    - For example, an architect shouldn't make a decision to use React.js - that's making a technical decision, not an architecture decision. The architect instead can suggest the team to use a _reactive-based framework_, which leaves the choice to the team to pick between React, Angular, Vue, Svelte, etc...
    - But it's also not uncommon for an architect to make a specific technical decision in order to preserve a specific characteristic such as _scalability_ or _performance_
- Continually analyze the architecture
    - _An architect is expected to continually analyze the architecture and current technology environment and then recommend solutions for improvement_
    - This expectation refers to _architecture vitality_
    - The architect needs to assess how viable is the architecture today that was defined three or more years ago
    - Not adapting the architecture leaves room for structural decay, which occurs when developers make design changes that impact architectural characteristics
- Keep current with latest trends
    - _An architect is expected to keep current with the latest technology and industry trends_
    - Just like the developers, architects too need to keep up to date with the latest technologies
    - The architect's decision is usually long-lasting and difficult to change. Being up to date helps the architect prepare for the future and make correct decisions
- Ensure compliance
    - _An architect is expected to ensure compliance with architecture decisions and principles_
    - This means the architect makes sure the development team is following the architecture decisions and design principles that are defined, documented, and communicated by the architect
    - The architect can measure compliance using _automated fitness functions_ and other tools
- Diverse exposure and experience
    - _An architect is expected to have exposure to multiple and diverse technologies, frameworks, platforms, and environments_
    - Not to be an expert, but at least be familiar with a variety of technologies
    - Architects need to stretch their comfort zone in order to fulfill this expectation
    - An effective software architect seeks to gain experience in multiple languages, platforms and technologies
    - Focus on technical breadth rather than technical depth
    - For example, it's more valuable for an architect to be familiar with 10 caching products (knowing their pros and cons) rather than an expert in only one of them
- Have business domain knowledge
    - _An architect is expected to have a certain level of business domain expertise_
    - The business domain can influence certain architecture decisions or characteristics, so it's important for an architect to have business domain knowledge
    - Having a business domain expertise is also needed to communicate effectively with stakeholders, C-level execs, and business users, otherwise the architect will quickly lose credibility
- Possess interpersonal skills
    - _An architect is expected to possess exceptional interpersonal skills, including teamwork, facilitation, and leadership_
    - One of the more difficult expectations
    - _"No matter what they tell you, it's always a people problem" - Gerald Weinberg_
    - An architect is expected to lead the development team through the implementation of the architecture
    - Also a great skill to differentiate when job searching
- Understand and navigate politics
    - _An architect is expected to understand the political climate of the enterprise and be able to navigate the politics_
    - Almost every decision an architect makes will be challenged by product owners, project managers, developers, and business stakeholders due to increased cost or increased effort
    - In all cases, the architect must navigate the politics of the company and apply their negotiation skills to get most decisions approved
## Intersection of Architecture and...
### Engineering Practices
There's a difference between _development process_ and _engineering practices_. "Process" is the mechanics of how people organize and interact (how meetings are conducted, how teams are formed, workflow organization, etc...). Engineering practices refers to process-agnostic practices that have repeatable benefit. One example of an engineering practice is _continuous integration_.
The architects must ensure that the architectural style they picked and the engineering practices form a symbiotic mesh. For example, microservices architecture assumes automated machine provisioning, and automated testing and deployments. That's _continuous integration_. That's _engineering practices_. Architects must integrate engineering practices with architectural decisions to ensure cohesion and success.
Due to the facts that in software development predicting structural changes up front is hard, that developers are bad at estimation due to _unknown unknowns_, and that it's impossible for architects to design for unknown unknowns, an _agile_ and _iterative development process_ aligns better with architecture.

### Operations / DevOps
Historically, operations has been considered as a separate function and often outsourced. Because of that, architects couldn't control operations and had to design defensively around that restriction. That resulted in vastly more complex architectures. To address this, many companies started experimenting with new forms of architecture that combine many operational concerns with the architecture itself.
For example, in older-style architectures like ESB-driven SOA, handling things like elastic scaling meant building them in the architecture itself, which greatly complicated it. In contrast to this, microservices architects realized that things like elasticity and scalability are best handled by the operations team. By creating a liaison between architecture and operations, architects can simplify the design and rely on ops for the things they handle best.

### Process
The process that the development team uses has impact on many facets of software architecture. Agile projects can assume iterative development - iterative development and faster feedback loop for decisions. This allows architects to be more aggressive about experimentation.
_"All architectures become iterative; it's just a matter of time" - Mark Richards (one of the authors)_

### Data
- Code and data have a symbiotic relationship: one isn't useful without the other
- Database admins work with architects to build data architecture for complex systems
## Laws of Software Architecture
1. _"Everything in software architecture is a trade-off" - First Law of Software Architecture_
    - _"... if an architect thinks they've discovered something that isn't a trade-off, it's more likely that they just haven't identified the trade-off yet" - Corollary 1_
2. _"Why is more important than how" - Second Law of Software Architecture_
    - Architecture is defined beyond structural scaffolding, incorporating principles, characteristics, and so on. It's broader than just the combination of structural elements.
    - An architect can look at an existing system and identify how the structure works, but will struggle to explain why certain decisions were made.




<!--- Eraser file: https://app.eraser.io/workspace/0aExo6JApaYi0ECiWX0X --->