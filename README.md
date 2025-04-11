# Lab 2

## How to Remove Branches

### 🔹 Delete branches locally:
```bash
git branch -d dev
git branch -d test
```
### 🔹 Delete branches remotely:
```bash
Copy
Edit
git push origin --delete dev
git push origin --delete test
```
---

## 🏷️ Tags and Rebase Explanation

### 🔖 What's the difference between Annotated and Lightweight tags?

- **Annotated tags** are stored as full objects in the Git database.
  - They include metadata like the tagger name, date, message, and even a GPG signature.
  - Command: `git tag -a v1.0 -m "my version"`
  
- **Lightweight tags** are just pointers to a commit.
  - No extra data is stored.
  - Command: `git tag v1.0`

---

### 🔁 When to use `rebase` instead of `merge`?

- Use `rebase` when you want a **cleaner, linear history**.
- Good for syncing a feature branch with the latest changes from `main`.
- Instead of:
  ```bash
  git merge main
  git rebase main
  ````
  -------

  📜 How to list and delete tags?
List all tags:

bash
Copy
Edit
git tag
Delete a tag locally:

bash
Copy
Edit
git tag -d v1.7
Delete a tag remotely:

bash
Copy
Edit
git push origin --delete v1.7
sql
Copy
Edit

### Then commit and push it:

```bash
git add README.md
git commit -m "Add tag and rebase explanations"
git push origin main
```
-----
