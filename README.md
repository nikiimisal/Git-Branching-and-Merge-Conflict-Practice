# Git Branching and Merge Conflict Practice

This project shows how to work with multiple branches in Git, merge them, and handle merge conflicts step-by-step.

## 🧩 Steps Followed

### 1️⃣ Create and Clone Repository
- Create a new repository on GitHub.  
- Clone it to your local system using:  
  ```bash
  git clone <repo_url>
  ```

### 2️⃣ Create and Edit index.html
- Create a file named **index.html** and add some sample data.  
- Save the file.

### 3️⃣ Create and Switch to `contact_us` Branch
- Create a new branch from the main branch:
  ```bash
  git checkout -b contact_us
  ```
- Create a file named **contact.html** and add some data.  
- Add an anchor tag in **index.html** linking to **contact.html**.  
- Add and commit the changes:
  ```bash
  git add .
  git commit -m "Added contact page and link"
  ```

### 4️⃣ Merge `contact_us` Branch into Main
- Switch back to the main branch:
  ```bash
  git checkout main
  ```
- Merge the **contact_us** branch:
  ```bash
  git merge contact_us
  ```

### 5️⃣ Create and Work on `about_us` Branch
- Create a new branch:
  ```bash
  git checkout -b about_us
  ```
- Create **about.html**, add some data.  
- Add an anchor tag in **index.html** linking to **about.html**.  
- Add and commit changes:
  ```bash
  git add .
  git commit -m "Added about page and link"
  ```

### 6️⃣ Don’t Merge Yet
- Do not merge **about_us** branch now.  
- We will create another branch to simulate a merge conflict.

### 7️⃣ Create `home` Branch and Make Changes
- Create and switch to a new branch:
  ```bash
  git checkout -b home
  ```
- Create **home.html** and add some data.  
- Add an anchor tag in **index.html** linking to **home.html** (on the same line as the previous links).  
- Add and commit the changes:
  ```bash
  git add .
  git commit -m "Added home page and link"
  ```

### 8️⃣ Merge and Resolve Conflicts
- Go back to the main branch:
  ```bash
  git checkout main
  ```
- Merge **about_us** branch first:
  ```bash
  git merge about_us
  ```
- Then try merging **home** branch:
  ```bash
  git merge home
  ```
- A conflict will occur in **index.html**.  
- Open the file, resolve the conflict manually, then add and commit:
  ```bash
  git add .
  git commit -m "Resolved merge conflict and merged home branch"
  ```

### 9️⃣ Clean Up Branches
- Delete all extra branches and keep only **main**:
  ```bash
  git branch -d contact_us
  git branch -d about_us
  git branch -d home
  ```

## ✅ Final Result
- Only the **main** branch remains in the repository.
- All pages (**index.html**, **contact.html**, **about.html**, **home.html**) are merged successfully.  
