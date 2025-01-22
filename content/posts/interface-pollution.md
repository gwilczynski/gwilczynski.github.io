+++
date = '2025-01-16T16:10:50+01:00'
title = 'Interface pollution'
tags = ["golang", "softwarearchitecture"]
author = "Grzegorz Wilczynski"
+++

I was looking for distilled information about clean architecture in the context of GO. In the meantime, my colleague found (in my opinion) the best article that describes this topic in great depth: https://pkritiotis.io/clean-architecture-in-golang/

In general I like most of it. However, what I don't like is that every handler's builder returns an interface instead of a concrete struct, and the domain defines the repository interface.

Here's why returning the concrete structure might be a better choice in many cases:

✨ Interfaces Should Be Defined by Consumers. Interfaces are generally more useful when defined by the consuming code rather than the producing code. Returning a concrete struct instead allows the consumer to define and use their own interfaces as needed. This decouples the producer from the consumer and avoids forcing a specific abstraction on the user of the handler

✨ Interface Segregation. Returning the concrete struct allows you to add methods to the struct in the future without breaking backward compatibility. If you return an interface and later need to add a method, all implementations of that interface need to be updated, which can be disruptive.

✨ Testability and Mocking. When the factory function returns the struct, consumers can create their own interfaces based on their specific needs. This makes it easier to mock the behavior for testing since the interface can be narrower and focused on the specific methods the test cares about.

As an appendix, I recommend this article https://100go.co/5-interface-pollution/, and the entire book https://www.manning.com/books/100-go-mistakes-and-how-to-avoid-them in general.

Happy hacking! 🚀
