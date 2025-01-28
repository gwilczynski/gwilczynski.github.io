+++
date = '2025-01-28T20:45:51+01:00'
title = 'From Chore to Habit'
tags = ["software architecture"]
author = "Grzegorz Wilczynski"
+++

Every time I joined a new project, I made it a point to take responsibility for fixing bugs. Why? Because fixing bugs is the best way to understand the architecture and get familiar with the codebase. Often, there’s little to no documentation, and all the knowledge is locked inside the developers’ heads. By fixing bugs (and writing tests as I went), I created my own map to navigate the codebase, uncover its quirks, and ensure I wasn’t lost.

Writing tests isn’t just a technical task; it’s a mindset, a rhythm I’ve developed over time. [TDD](https://martinfowler.com/bliki/TestDrivenDevelopment.html) is now second nature to me. When I sit down to write a new feature, my first step isn’t writing the functionality itself. Instead, I start with a question: What should this code do? I define that behavior in the form of tests.

But it wasn’t always like this.

When I started out, I didn’t hate writing tests. In fact, I liked the idea from the moment I learned about it. Still, it was challenging. Writing unit tests required effort. Mocking, stubbing, and dealing with poorly designed code (much of which I had written myself) made testing harder than it needed to be. The problem wasn’t testing itself; it was the code, which wasn’t designed to be testable.

Over time, though, I experienced the payoff. With practice and better design patterns, writing tests became second nature. Now, I can’t imagine working without them. Tests are the guardrails that let me move fast without fear of breaking things. They give me confidence to iterate, refactor, and push forward.

But tests alone aren’t enough.

While tests give you confidence in the functionality of your code, they don’t provide an overarching understanding of the system. What if there are no bugs? What if everything just works? Test coverage might be high (90% or more) but that doesn’t mean you fully understand how the application works.

That’s where documentation comes in.

For many developers, writing documentation feels like a chore, much like writing unit tests did when I first started. Many of us struggle with it. We either overexplain irrelevant details, leave out critical information, or skip it entirely.

Here’s the thing: writing documentation doesn’t have to be hard. Like testing, it can become a habit, a natural part of your workflow. All you need is the right method. And that method is [C4](https://c4model.com/).

Think of the C4 model as a framework to think about your system and communicate it clearly to both technical and non-technical stakeholders. Instead of writing endless pages of text, you create concise, visual diagrams that explain how your system works.

The C4 model breaks your system into four layers of abstraction:

- **Context**: What does the system do, and who uses it? For example: a content management system (CMS) used by content creators, editors, and admins to create, manage, and publish digital content. It may interact with external systems such as analytics tools, social media platforms, and cloud storage services.

- **Containers**: What are the major building blocks (apps, databases, services)? For example, a web app, a database, and APIs that constitute the system.

- **Components**: How are those building blocks broken down internally? For example: Authentication includes login and access control; the Content Editor is used for creating and formatting articles; and Workflow manages approvals and publishing.

- **Code** (optional): How does the actual code support the components? Inline documentation may replace this layer if your code is already well-commented.

The beauty of the C4 model is its simplicity. It captures the most important details without overwhelming readers. It’s focused, easy to understand, and effective.

Once you get into the flow of using the C4 model, writing documentation stops being a chore. It becomes part of your rhythm, just like writing unit tests. It’s no longer a big, scary task you put off until the end of the project, or never do at all. Instead, it’s something you do naturally as part of your development process.

Here’s my challenge to you: the next time you’re tempted to skip writing documentation, think back to how you felt about unit tests when you started. Remember how challenging they seemed at first? Consider using tools like [Structurizr](https://structurizr.com/) alongside the C4 model to create effective, visual documentation. Structurizr can make it easy to translate your understanding into clean, professional diagrams.

Over time, just like testing, documentation will give you confidence and speed.

Unit tests and documentation aren’t just tools; they’re the guardrails that let us build with confidence, speed, and clarity. They separate good developers from great ones and reduce the infamous "bus factor".

Start small. Create your first Context diagram with the C4 model. Stick with it, and soon these habits will become second nature. Before long, you’ll wonder how you ever worked without them.

Happy hacking! 🚀
