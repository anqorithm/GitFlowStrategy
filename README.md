# GitFlow Strategy


```mermid
gitGraph
    commit id: "Initial commit"
    commit id: "Create empty Calculator class"
    
    branch develop
    checkout develop
    commit id: "Start development branch"
    commit id: "Add Calculator class structure"
    
    branch feature/add-method
    checkout feature/add-method
    commit id: "Implement add(a, b) method"
    commit id: "Add tests for addition"
    
    checkout develop
    merge feature/add-method
    commit id: "Addition feature complete"
    
    branch feature/subtract-method
    checkout feature/subtract-method
    commit id: "Implement subtract(a, b) method"
    commit id: "Add tests for subtraction"
    
    checkout develop
    merge feature/subtract-method
    commit id: "Subtraction feature complete"
    
    branch feature/multiply-method
    checkout feature/multiply-method
    commit id: "Implement multiply(a, b) method"
    commit id: "Add tests for multiplication"
    
    checkout develop
    merge feature/multiply-method
    commit id: "Multiplication feature complete"
    
    branch feature/divide-method
    checkout feature/divide-method
    commit id: "Implement divide(a, b) method"
    commit id: "Add basic division tests"
    
    checkout develop
    merge feature/divide-method
    commit id: "Division feature complete"
    
    branch release/v1.0.0
    checkout release/v1.0.0
    commit id: "Version bump to 1.0.0"
    commit id: "Add documentation"
    commit id: "Final testing"
    
    checkout main
    merge release/v1.0.0
    commit id: "Tag: v1.0.0 Calculator Release"
    
    checkout develop
    merge release/v1.0.0
    commit id: "Sync develop with release"
    
    branch hotfix/divide-by-zero
    checkout hotfix/divide-by-zero
    commit id: "Fix: Add zero check to divide method"
    commit id: "Add tests for divide by zero"
    
    checkout main
    merge hotfix/divide-by-zero
    commit id: "Tag: v1.0.1 Division Bug Fix"
    
    checkout develop
    merge hotfix/divide-by-zero
    commit id: "Apply division fix to develop"
    
    checkout develop
    commit id: "Continue development"
```