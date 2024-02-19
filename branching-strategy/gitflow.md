# Git Flow
Git Flow is a branching model that defines a strict branching structure designed for projects that have a scheduled release cycle. It involves multiple branches for different purposes: ``feature``, ``develop``, ``release``, ``hotfix``, and ``main``.

## Pros:

 - **Structured:** It provides a clear structure for managing releases, which can help in organizing large projects.
- **Separation of concerns:** Different branches for different stages of development ensure that various aspects of development like features, releases, and hotfixes are cleanly separated.


## Cons:

- **Complexity:** Can be overkill for small projects due to its complexity and the number of branches involved.
- **Learning Curve:** New team members may require time to fully understand and effectively use this model.

```mermaid
gitGraph:
    commit tag: "v.01"
    branch develop
    checkout develop
    commit
    branch feature/feature1
    checkout feature/feature1
    commit
    checkout develop
    merge feature/feature1
    branch release/v1.0
    checkout release/v1.0
    commit
    checkout develop
    merge release/v1.0
    checkout main
    merge release/v1.0 tag: "v1.0"
    commit
    branch hotfix/hotfix1
    checkout hotfix/hotfix1
    commit
    checkout main
    merge hotfix/hotfix1 tag: "v1.1"
    checkout develop
    merge hotfix/hotfix1
```