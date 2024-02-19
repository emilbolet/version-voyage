# Trunk Based Development (TBD)
 Trunk Based Development is a Git branching model where all developers work in a single branch called the ``trunk`` or ``main`` branch. Short-lived feature branches may be used, but they are merged back into the trunk frequently, usually at least once a day.

## Pros:

- **Rapid Integration:** Promotes continuous integration by encouraging frequent merges to the trunk, which helps in identifying and resolving conflicts early.
 - **Simplicity:** Maintains a simple repository structure that is easy to navigate and manage.
Speed: Accelerates the development process by reducing the overhead of managing multiple long-lived branches.

## Cons:

- **Risk of Unstable Main Branch:** The trunk can become unstable if not properly managed with rigorous automated testing and code review practices.
- **Requires Discipline:** Developers need to be disciplined in their development practices, ensuring that code committed to the trunk is always in a releasable state.