## 🔀 What Is a **Fork**?

### 📌 Definition:

A **fork** is a **copy of an entire repository** (including its full history) that lives under **your own GitHub account**.

### ✅ Use Case:

* Contributing to someone else’s project
* Experimenting freely without affecting the original code
* Making a private copy of a public repo

### 📂 Example:

You want to contribute to an open-source repo like `github.com/facebook/react`.

1. You **fork** it to your account:
   `github.com/yourusername/react`
2. Make changes on your version.
3. Create a **pull request** to propose changes back to the original repo.

### 🔧 Command (CLI):

> *Forks happen on GitHub, not via CLI directly*, but you can clone it after:

```bash
git clone https://github.com/yourusername/react.git
```

---

## 🌿 What Is a **Branch**?

### 📌 Definition:

A **branch** is an **independent line of development** in the same repository.

### ✅ Use Case:

* Add features without breaking `main`
* Work on bug fixes
* Isolate experiments

### 📂 Example:

You want to build a login feature:

1. On your local repo:

```bash
git checkout -b feature/login
```

2. Make changes and commit:

```bash
git add .
git commit -m "Add login UI"
```

3. Push your branch:

```bash
git push origin feature/login
```

4. Later, merge it back into `main`.

---

## 🔁 What Is a **Merge**?

### 📌 Definition:

A **merge** brings together the history and changes from one branch into another.

### ✅ Use Case:

* Finalize a feature or fix
* Combine branches for release
* Sync updates from other team members

### 📂 Example:

You want to merge `feature/login` into `main`.

1. Switch to `main`:

```bash
git checkout main
```

2. Pull in the changes:

```bash
git merge feature/login
```

3. Push:

```bash
git push origin main
```

> 🧠 GitHub also allows **pull requests** to handle merges with review and CI checks.

---

## 🔄 Summary Table

| Concept    | What It Is          | Use Case                   | Where It Lives  | Common Command               |
| ---------- | ------------------- | -------------------------- | --------------- | ---------------------------- |
| **Fork**   | Copy of entire repo | Contribute to another repo | On GitHub       | `Fork` via UI                |
| **Branch** | Line of development | Add feature, fix bug       | Inside one repo | `git checkout -b branchname` |
| **Merge**  | Combine branches    | Finalize feature, release  | Any Git repo    | `git merge branchname`       |

---

## 🧭 Visual Workflow (Optional Mermaid)

```mermaid

flowchart LR
    A[Original Repo (main)] -->|Fork| B[Your Forked Repo (main)]
    B -->|Create Branch| C[feature/login]
    C -->|Make Commits| D[Commits]
    D -->|Push to Fork| E[Pull Request]
    E -->|Merge| F[Original Repo (main)]
