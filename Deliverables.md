# SeniorHub Deliverables (Design Patterns & Video Script)

This document contains the theoretical and presentation components required for the SDA Assignment.

---

## Deliverable 3: Design Patterns Recommendation

### 1. Model-View-Controller (MVC)
*   **Specific Problem it Solves**: In SeniorHub, the logic for managing students and faculty (Model) is separated from the Swing windows (View). The `ActionListener` blocks in our code act as the Controller. This prevents "Spaghetti Code" where data logic and UI code are mixed.
*   **Would the code work without this?**: **Yes**, but it would be significantly harder to maintain. Without MVC, a change in how we store Student data would require us to rewrite the entire GUI code.
*   **Limitation**: For small-scale projects like this, MVC can feel like "over-engineering," as it requires more files and interfaces than a simple procedural script.

### 2. Singleton Pattern
*   **Specific Problem it Solves**: Our `DataStorage` class uses the Singleton pattern to ensure that only one instance of the "Mock Database" exists. This prevents data inconsistency where one screen might show a student that another screen doesn't recognize.
*   **Would the code work without this?**: **Yes**, we could pass the list of students as a parameter to every constructor, but this leads to "Prop Drilling" and makes the code messy.
*   **Limitation**: Singletons create a global state, which can make Unit Testing difficult because tests might interfere with each other if they modify the shared data.

---

## Deliverable 4: 3-Minute Video Script (Technical Reflection)

**Title**: SeniorHub: From Design to Implementation  
**Cast**: Member 1 (Project Lead), Member 2 (Developer), Member 3 (Architect)

**Member 1 (Intro & Productivity)**:  
"Hello everyone! We are Group [Number], and today we’re presenting SeniorHub, our solution for streamlining Final Year Projects. For this assignment, we transitioned from our Task 2 UML design to a functional Java Swing application. A key part of our workflow was using Gemini as our AI coding partner. We chose this approach to maximize productivity—Gemini helped us quickly generate the Swing boilerplate code and ensured our domain classes, like `Student` and `Supervision_Request`, matched our UML exactly. This allowed us to focus on the architecture rather than getting stuck on syntax."

**Member 2 (The Good and The Bad)**:  
"Using an LLM came with both pros and cons. On the **positive side**: it allowed for rapid prototyping, caught layout errors that usually take hours to debug, and helped us stick to clean Java SE standards. However, we did face **challenges**: the AI sometimes 'hallucinated' method names that didn't exist in our UML, struggled with precise GridBagLayout positioning without manual tweaks, and occasionally lacked the specific context of our university’s business rules. We had to carefully 'self-correct' the code to ensure it was 100% compliant with the rubric."

**Member 3 (Design Patterns & Conclusion)**:  
"To ensure our system was professional, the LLM recommended the **MVC** and **Singleton** patterns. We agreed because MVC keeps our project logic clean and separate from the GUI, while the Singleton pattern ensures our data stays consistent across all screens. While the code would work without them, these patterns solve the problem of scalability and global data access. Of course, the limitation is that they add a bit of complexity, but they are essential for a 'SeniorHub' scale system. Overall, this approach taught us how to bridge the gap between abstract design and real-world implementation. Thank you!"
