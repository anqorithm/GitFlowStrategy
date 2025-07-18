# GitFlow Strategy

# Intro

```mermaid
gitGraph
    commit
    branch develop
    checkout develop
    commit

    %% First release: add & subtract
    branch feature/add-method
    checkout feature/add-method
    commit
    checkout develop
    merge feature/add-method

    branch feature/subtract-method
    checkout feature/subtract-method
    commit
    checkout develop
    merge feature/subtract-method

    branch release/v1.0.0
    checkout release/v1.0.0
    commit id: "Release prep v1.0.0"

    checkout main
    commit id: "Tag: v1.0.0"
    merge release/v1.0.0

    checkout develop
    merge release/v1.0.0

    %% Second release: multiply & divide
    branch feature/multiply-method
    checkout feature/multiply-method
    commit
    checkout develop
    merge feature/multiply-method

    branch feature/divide-method
    checkout feature/divide-method
    commit
    checkout develop
    merge feature/divide-method

    branch release/v1.1.0
    checkout release/v1.1.0
    commit id: "Release prep v1.1.0"

    checkout main
    merge release/v1.1.0
    commit id: "Tag: v1.1.0"

    checkout develop
    merge release/v1.1.0

    %% Hotfix after v1.1.0
    branch hotfix/divide-by-zero
    checkout hotfix/divide-by-zero
    commit id: "Fix: divide-by-zero"

    checkout main
    merge hotfix/divide-by-zero
    commit id: "Tag: v1.1.1"

    checkout develop
    merge hotfix/divide-by-zero
```