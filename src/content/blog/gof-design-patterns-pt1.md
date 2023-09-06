---
title: "GoF's Design Patterns (part 1)"
description: 'Notes from Chapter 1 (part 1)'
pubDate: 'Sep 03 2023'
heroImage: '/hero-gof-design-patterns-pt1.jpg'
---

In the **preface**, the authors state that "[Design Patterns] might take a little more work than _ad hoc_ solutions. But the extra effort invariably pays dividends in increased flexibility **and** reusability."

I've stressed "flexibility **and** reusability" because I've seen (and designed myself) code that, while certainly increases reusability, **reduces** flexibility. As far as I know, that could happen mainly because of two reasons:

1. Early abstractions. In an effort for refactoring soon, sometimes one might end up abstracting way too much, taking for certain some assumptions too early.
2. Use of anti-patterns. I think they require a constant effort to be catched as we tend to develop them ourselves, if we don't learn from our own mistakes.

Reusability without flexibility is, in general, a design anti-pattern.

---

What is a design pattern? The authors start out with a quote by the architect [Christopher Alexander](https://en.wikipedia.org/wiki/Christopher_Alexander):

> Each pattern describes a problem which occurs over and over again in our environment, and then describes the core of the solution to that problem, in such a way that you can use this solution a million times over, without ever doing it the same way twice.
<!-- 
A pattern has four essential elements:
1. The **pattern name**.
2. The **problem**, describing when to apply the pattern.
3. The **solution**, an abstract description on how to arrange classes and objects in order to solve an abstract design problem.
4. The **consequences**, which are the results and trade-offs of applying the pattern. -->

---

## The catalog

The authors organize the patterns based on two criteria: **purpose** (creational, structural and behavioral) and **scope** (class and object).

In the scope of **class**, the patterns are:

| **Creational**     | **Structural**     | **Behavioral**            |
| ------------------ | ------------------ | ------------------------- |
| `Factory Method`   | `Adapter (class)`  | `Interpreter`             |
|                    |                    | `Template Method`         |

While the **object patterns** are:

| **Creational**     | **Structural**     | **Behavioral**            |
| ------------------ | ------------------ | ------------------------- |
| `Abstract Factory` | `Adapter (object)` | `Chain of Responsibility` |
| `Builder`          | `Bridge`           | `Command`                 |
| `Prototype`        | `Composite`        | `Iterator`                |
| `Singleton`        | `Decorator`        | `Mediator`                |
|                    | `Facade`           | `Memento`                 |
|                    | `Flyweight`        | `Observer`                |
|                    | `Proxy`            | `State`                   |
|                    |                    | `Strategy`                |
|                    |                    | `Visitor`                 |

**Class patterns** deal with relationships between classes and their subclasses. As these relationships are established through inheritance, they are **static**.

On the other hand, **object patterns** deal with object relationships, which are **dynamic**.

---

I think that, in most cases, implementing patterns wouldn't worth it when prototyping, due to that extra boilerplate needed to achieve a most probably unneeded flexibility.

In the same sense, I think I wouldn't start out implementing a pattern before the actual need for it arises.

---

In the **foreword** [Grady Booch](https://en.wikipedia.org/wiki/Grady_Booch), says: "All well-structured object-oriented architectures are full of patterns. Indeed, one of the ways that I measure the quality of an object-oriented system is to judge whether or not its developers have paid careful attention to the **common collaborations among its objects**". Emphasis mine.

---

> In short, the concept of the design pattern in software provides a key to helping developers leverage the expertise of other skilled architects.<br/>
> — <cite>Grady Booch</cite>

I think this is key. Design patterns not only help build a common language but also unlock **experience reuse**.

---

> Yet experienced object-oriented designers do make good designs. Meanwhile new designers are overwhelmed by the options available and tend to fall back on non-object-oriented techniques they’ve used before.

It's very common to see imperative solutions in object-oriented code. Sometimes it could be good enough. But imperative code is less flexible, less readable, and transparent in intent. You have to understand the guts of the code in order to know what its intent is.

---

> One thing expert designers know _not_ to do is solve every problem from first principles. Rather, they reuse solutions that have worked for them in the past. (...) Such experience is part of what makes them experts.

The more experienced the designer is, the easier they find straight-forward, simple solutions. Less experienced developers tend to reinvent the wheel more frequently.

---

> Once you know the pattern, a lot of design decisions follow automatically. (...) Put simply, design patterns help a designer get a design "right" faster.

---



<!-- 
## Creational, Structural & Behavioral Patterns

> Creational patterns concern the process of object creation. Structural patterns deal with the composition of classes or objects. Behavioral patterns characterize the ways in which classes or objects interact and distribute responsibility.

---

## Class & Object Patterns

> Class patterns deal with relationships between classes and their subclasses. These relationships are established through inheritance, so they are static—fixed at compile-time.

---

> Object patterns deal with object relationships, which can be changed at run-time and are more dynamic.

---

## Other stuff

> Object-oriented designs often end up with classes that have no counterparts in the real world. (...) Strict modeling of the real world leads to a system that reflects today’s realities but not necessarily tomorrow’s. The abstractions that emerge during design are key to making a design flexible. (...) For example, objects that represent a process or algorithm don’t occur in nature, yet they are a crucial part of flexible designs.

## Types

> An object may have many types, and widely different objects can share a type.

---

> Part of an object’s interface may be characterized by one type, and other parts by other types.

---

> Two objects of the same type need only share parts of their interfaces.

---

> Interfaces can contain other interfaces as subsets.

---
 -->
