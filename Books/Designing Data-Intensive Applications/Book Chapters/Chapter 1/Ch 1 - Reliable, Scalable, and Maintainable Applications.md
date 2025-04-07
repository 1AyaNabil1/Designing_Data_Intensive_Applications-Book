_Chapter 1 of [[Designing Data-Intensive Applications.pdf]] by Martin Kleppmann_

## Overview

- Introduces the core goals of data-intensive systems: **reliability**, **scalability**, and **maintainability**.
- Focuses on why these properties matter in modern applications that handle large amounts of data.
- Sets the stage for the book’s exploration of data systems, from databases to distributed architectures.

## Key Concepts

### Reliability

- A system should work correctly, even when things go wrong (e.g., hardware failures, software bugs, human errors).
- Fault tolerance is critical: anticipate and handle failures gracefully.
- Examples of faults:
    - Hardware failures (e.g., disk crashes).
    - Software errors (e.g., bugs or unexpected inputs).
    - Human mistakes (e.g., misconfigurations).
- Goal: Minimize downtime and ensure consistent performance.
- Links: [[Fault Tolerance]], [[Reliability Metrics]]

### Scalability

- A system’s ability to handle increased load (e.g., more users, data, or traffic) without degrading performance.
- Key questions:
    - How does the system behave as load increases?
    - What resources (CPU, memory, network) are needed to handle growth?
- Metrics to measure scalability:
    - **Throughput**: Transactions or operations per second.
    - **Latency**: Time taken to process a request (e.g., percentiles like p95, p99).
- Approaches: Vertical scaling (bigger machines) vs. horizontal scaling (more machines).
- Links: [[Scalability Patterns]], [[Load Balancing]]

### Maintainability

- A system should be easy to operate, modify, and extend over time.
- Three aspects:
    - **Operability**: Make it easy for ops teams to manage (e.g., monitoring, automation).
    - **Simplicity**: Reduce complexity to avoid bugs and confusion.
    - **Evolvability**: Allow the system to adapt to changing requirements.
- Trade-off: Building simple systems often requires more upfront design effort.
- Links: [[System Design Principles]], [[Technical Debt]]

## Why These Matter

- Modern apps (e.g., web services, mobile backends) rely on data-intensive systems.
- Users expect:
    - Always-on availability (**Reliability**).
    - Fast performance under heavy load (**Scalability**).
    - New features without breaking existing functionality (**Maintainability**).
- Poor design in any of these areas leads to outages, slow performance, or unmanageable codebases.

## Takeaways

- Reliability, scalability, and maintainability are interconnected—optimizing one often affects the others.
- Designing data-intensive systems requires trade-offs, not silver bullets.
- Understanding the application’s requirements (e.g., load, fault tolerance needs) is the first step.

## Quotes

- “The architecture of a system is shaped by the needs it must fulfill.”
- “A fault is not the same as a failure—a fault-tolerant system can continue operating despite faults.”

## Related Topics

- [[Distributed Systems]]
- [[Database Design]]
- [[Performance Engineering]]