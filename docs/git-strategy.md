# 📚 Branching Strategy for Personal Projects

This is a simple and clean Git branching strategy designed for solo developers working on personal projects.

---

##  `main` 

- The **production-ready** branch.
- Contains **stable and tested code** only.
- Never commit directly — merge feature branches or development (`dev`) into it when ready.
- Use this branch for:
    - Deployment
    - Production builds
    - Version tagging

---

## `dev` 

- A **development integration** branch.
- Merge all feature and fix branches into `dev`.
- Periodically merge `dev` into `main` when a release is ready.
- Recommended for larger or ongoing projects.

---

## `feature/feature-name`

- Used to develop **new features**.
- Naming convention: `feature/add-login`, `feature/refactor-header`, etc.
- Branches off from: `dev` (or `main` if no `dev`)
- Merge into: `dev` (or `main`)

---

##  `fix/fix-name`

- Used for **bug fixes**.
- Naming convention: `fix/typo-about-page`, `fix/navbar-overlap`
- Branches off from: `dev` or `main`
- Merge into: `dev` or `main` depending on urgency

---

##  `hotfix/hotfix-name` (optional)

- Used for **urgent fixes** to production.
- Branches off from: `main`
- Merge into: `main` and `dev` (to keep them in sync)

---

