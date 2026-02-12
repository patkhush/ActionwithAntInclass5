# GitHub Actions Lab

## Workflow 1 — Dependent Jobs
This workflow demonstrates **job dependencies** using the `needs` keyword.  
Jobs run in this order:
1. build
2. test (needs: build)
3. deploy (needs: test)

Key concepts:
- `needs` controls job order
- `runs-on` specifies the VM image (ubuntu-latest)

---

## Workflow 2 — Multi-Platform Testing
This workflow runs **three jobs in parallel** on:
- Ubuntu
- Windows
- macOS

Key concepts:
- Parallel jobs = no `needs`
- OS-specific behavior using `runs-on`
- Each job prints OS information and creates a file

---

## Challenges & Solutions
1. I faced problem that i was not able to see the workflows
   sol: i have to add _dispath in the yml file 
