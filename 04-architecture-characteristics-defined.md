# Architecture Characteristics Defined

When designing a system, architects gather a list of requirements for that
system. But aside from the implicit requirements, architects needs to consider
many other factors, such as auditability, performance, security, scalability,
etc.

These are called _architecture characteristics_. Architecture characteristics
are all the things the software must possess that aren't directly related to the
domain functionality, but are crucial for the success. Sometimes they're
referred to as _nonfunctional requirements_, or _quality attributes_.

The architecture characteristic must:

- Specify a nondomain design consideration
  - A common important architecture characteristic is _performance_. It
    specifies a certain level of performance for the application, but it rarely
    is mentioned explicitly in the requirements.
- Influences a structural part of the design
  - Take _security_ for example. Every project requires a certain level of
    security practices to be put in place, but it raises to the level of
    architecture characteristic when we need to design something special for it.
    For example, in an application that handles payments through a third-party
    payment processor, no special security designs need to be considered. But if
    the payments were processed inside of the application, then certain modules,
    components, or services need to be designed in order to handle payments
    securely.
- Is critical or important to the application's success
  - Again, take the previous _security_ example. If in-application payment
    processing fails (security wasn't considered when designing the
    architecture), the application could face severe financial and reputational
    damage.

Architecture characteristics are divided into _implicit_ and _explicit_
characteristics. The implicit ones rarely appear in requirements, but they're
crucial for application success. Availability, reliability, and security are
some examples of implicit architecture characterictics. To uncover the implicit
characteristics, architects must use their knowledge in the problem domain. The
explicit ones appear in the requirement documents or other specific
instructions.

## Architecture Characteristics (Partially) Listed

There is no true, universal standard that defines architecture characteristics.
Each organization can have their own definitions, but let's explore some of the
common ones.

### Operational Architecture Characteristics

| Term                 | Definition                                                                                                                                           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Availability         | How long the system will need to be available (if 24/7, specific things need to be design to allow the system to reboot in case of a failure).       |
| Performance          | Stress testing, peak analysis, capacity required, response times.                                                                                    |
| Recoverability       | In case of a disaster, how quickly is the system required to be online again. This affects backup strategy and requirements for duplicated hardware. |
| Reliability / safety | Does the system need to be fail-safe? Is it mission critical in a way that affects lives? If it fails, will the company lose large sums of money?    |
| Robustness           | Ability to handle errors and boundary conditions while running, like if the internet goes down, or there's a power outage, or a hardware failure.    |
| Scalability          | Ability for the system to continue to operate normally as the number of users or requests increase.                                                  |

### Structural Architecture Characteristics

| Term            | Defintion                                                                                                                                            |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Configurability | Should the end user be allowed to easily change certain aspects of the system (through usable interfaces)?                                           |
| Extensibility   | How easy it is to plug new pieces of functionality in.                                                                                               |
| Installability  | How easy it is to install the system on al lnecessary platforms.                                                                                     |
| Reusability     | How easy it is to reuse common components arcross multiple products.                                                                                 |
| Localization    | Support for multiple languages, including date formats, currencies, units of measure.                                                                |
| Maintainability | How easy it is to apply changes and enhance the system?                                                                                              |
| Supportability  | What level of technical support is needed by the application? What level of logging and other facilities are required to debug errors in the system? |
| Upgradeability  | Ability to easily upgrade from a previous version to a newer version on servers and clients.                                                         |

### Cross-Cutting Architecture Characteristics

| Term           | Definition                                                                                                                                                                                                                  |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Accessibility  | Ease of access to all users, including those with disabilities like color blindness or hearing loss.                                                                                                                        |
| Archivability  | Will the data be archived or deleted after a period of time?                                                                                                                                                                |
| Authentication | Security requirements to ensure users are who they say they are.                                                                                                                                                            |
| Authorization  | Security requirements to ensure users can access only certain functions within the application.                                                                                                                             |
| Legal          | What legislative constraints is the system operating in (GDPR, data protection, etc.)? What reservation rights does the company require? Are there any regulations that influence how the application is built or deployed? |
| Privacy        | Ability to hide transactions from internal company employees (ex. encrypted transactions so even DBAs and network architects cannot see them).                                                                              |
| Security       | Does the data need to be encrypted in the database? Encrypted for network communication between internal systems? What type of authentication needs to be in place for remote user access?                                  |
| Supportability | What level of technical support is needed by the application?                                                                                                                                                               |
| Usability      | Level of training required for users to achieve their goals with the application. Usability requirements need to be treated as seriously as any other architectural issue.                                                  |

## Trade-Offs and Least Worst Architecture

Each supported architecture characteristic adds to the complexity of the system.
Some architecture characteristics are even contradicting each other, like
_performance_ and _security_ - if we implement on-the-fly encoding and decoding
for higher security, the performance is degraded. For those reasons, the
decision of which architecture characteristics the system will support come down
to trade-offs.

> Never shoot for the best architecture, but rather the least worst
> architecture.

But as the system grows and changes, architects should aim to design the
architecture to be as iterative as possible. If you can easily make changes to
the architecture, you can stress less about discovering the right set of
characteristics in the first attemp.
