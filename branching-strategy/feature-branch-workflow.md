# Feature Branch Workflow
In the Feature Branch Workflow, all feature development takes place in a dedicated branch instead of the main or master branch. Features are merged back into the main branch once they are completed and tested.

## Pros

- **Isolation:** Developers can work on features in isolation, without affecting the main codebase.
- **Collaboration:** Makes it easier for multiple developers to collaborate on a single feature.

## Cons

- **Merge Conflicts:** Potential for merge conflicts if features are developed in parallel for an extended period.
- **Management:** Requires diligent branch management to avoid a cluttered repository with stale branches.

## Graph

```mermaid
gitGraph
    options
    {
      "showCommitLabel": false
    }
    end
    commit id:"C0" tag:"Initial commit"
    branch feature1
    checkout feature1
    commit id:"C1"
    checkout main
    merge feature1
    branch feature2
    checkout feature2
    commit id:"C2"
    checkout main
    merge feature2
    branch feature3
    checkout feature3
    commit id:"C3"
    checkout main
    merge feature3
```