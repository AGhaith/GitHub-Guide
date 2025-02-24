# **Let's Talk About Git & GitHub**

If you're here, you’re probably trying to figure out Git and GitHub. And yes, they’re **not** the same thing. But before we dive into how they work, let’s answer a more important question:  

## **Why should you even care?**

### **Why Git?**
Picture this—you’re working on a project with four functions. You’ve successfully written the first three, but while coding the fourth, something goes **terribly wrong**. Errors everywhere. After hours of debugging, your code looks like a warzone. At this point, you wish you could just go back to when everything was working.  

Now, you *could* do what we’ve all done—save multiple versions of your file:
```
final.cpp  
final2.cpp  
FINAL_REAL.cpp  
final_FIXED_TRUST_ME.cpp  
```
But let’s be real, that never ends well. It’s messy, confusing, and far from efficient.  

This is where **Git** comes in.  

🔹 **Git is an offline technology** that keeps track of every version of your code, allowing you to go back to any point in time with ease. No more "final_final" file chaos.  

---

### **Why GitHub?**
Now, imagine we're working together on a project that has two functions. We agree that:
- **I** will implement `function1()`.
- **You** will implement `function2()`.  

We have two choices:  

#### **1. The WhatsApp nightmare:**
You finish `function1()`, send me the file, and I start working on `function2()`. But what if multiple people are involved? What if someone makes a mistake? Suddenly, managing files becomes a **shitty, unbearable process**.  

#### **2. The "merge disaster":**
You create your own file and work on your function. I do the same. Now we have two separate files and have to **manually** merge them, hoping nothing clashes. Spoiler: **something always clashes.**  

And this is **exactly** why GitHub exists.  

🔹 **GitHub is an online platform** where Git-tracked projects are stored. It allows multiple people to work on the same project at the same time, without stepping on each other's toes.  

---

## **Git vs. GitHub (In Simple Terms)**
| Feature   | Git | GitHub |
|-----------|-----|--------|
| **What is it?** | A version control system that tracks changes | A cloud-based platform for hosting Git projects |
| **Works online or offline?** | Offline (on your computer) | Online (on the web) |
| **Main purpose?** | Keeps track of code changes and versions | Helps teams collaborate and share Git-tracked projects |

---

## **Git Terminology You Need to Know**
Before we get into how to actually use Git, let’s go over some key terms you’ll encounter:

- **Repository (Repo):** A folder that contains your project files and the entire history of changes tracked by Git.
- **Commit:** A snapshot of your project at a specific point in time. Think of it as a save point in a video game.
- **Branch:** A separate version of your project where you can work on new features without affecting the main code.
- **Merge:** Combining changes from one branch into another.
- **Clone:** Making a copy of an existing Git repository.
- **Pull Request (PR):** A request to merge changes from one branch into another, commonly used in team collaborations.
- **Push & Pull:** "Push" sends your changes to GitHub, while "Pull" fetches updates from GitHub to your local machine.

---

## **Installing Git & Using the Terminal**

Before creating a repo with Git, you need to **install Git**:

- **Windows:** Download from [git-scm.com](https://git-scm.com) and install.
- **Mac:** Use `brew install git` (requires Homebrew).

💡 **Tip:** Git Bash, PowerShell, and CMD are used to type commands. They let you navigate files and run Git commands.


# **Files & Folders**

A **file** is stored data—code, text, images, etc. A **folder** (or **directory**) organizes multiple files, keeping things tidy.

💡 **Tip:** In the terminal, "changing directories" (`cd my_project`) means moving between folders.

---

## **Organizing Files & Folders**

Avoid a messy desktop that looks like a **pile of hot garbage**. Instead:

- Use clear names: `project_plan.txt` (not `final_final.docx`)
- Avoid spaces: use `_` or `-` like `my_project` or `my-project`
- Store projects properly: Keep GitHub projects in a dedicated folder.

---

# **What is a Repository (Repo)?**

A **GitHub repository** is a special folder for your project, tracked with Git. It stores your code, remembers changes, and allows collaboration.

## **Creating a Repository Using Git Bash**

Once Git is installed, open **Git Bash** and run:

1. Navigate to your project folder:
   ```sh
   cd path/to/your/project
   ```
2. Initialize Git:
   ```sh
   git init "repo_name"
   ```
   This creates a `.git` folder, making it a Git-tracked repo.

Now you have created a repo called `repo_name`, but remember, until this point, we haven't said anything about GitHub. We are just talking about Git, which means we are still local (offline), and nothing is on the web.

---
# **Commits – Saving Your Work**

A **commit** is like a save point in a video game. Every time you commit, you take a snapshot of your project so you can **go back if something breaks**.
Please remember that after committing, that save point is saved locally and is **not online** yet.

## **Making a Commit**

Before committing, you need to **stage** your changes:
When you commit, Git looks to see what you have staged and commits that. It **doesn’t** just commit everything.

```sh
git add .
```

`add` is the command you use when you want to stage a file. `git add .` means stage everything.
you can also stage only one file.
```sh
git add <filename>
```
If you don’t stage, **you can’t commit**.  

## **Now, commit your changes:** 

Each and every commit has a message, and **THANKFULLY**, Git doesn’t allow you to make a commit without a message. To put a message, write:

```sh
git commit -m "Short, clear message explaining what you did"
```

This command tells Git to commit everything that is **staged** and save that commit with that message. So in the future, when your code becomes a mess (and it will), and you want to go back to a certain point, you can choose that commit by its message.

🚨 **DON’T** write useless messages like `"commit"`, `"c"`, `"final final"`, or `"idk what this does"`. **Make them useful, PLEASE.** Because future you won’t remember what `fix` means.

💡 **Good commit message examples:**\
✅ `"Fixed login bug by updating validation"`\
✅ `"Added navbar and improved styling"`\
✅ `"Refactored database connection logic"`


---
# **Pushing to GitHub – Publishing Your Work**

So far, everything you've done is **local**—it exists only on your machine. To make it available online, you need to **push** your project to GitHub.

## **What is Pushing?**

**Pushing** is the process of uploading your local commits to a GitHub repository. But remember:
1. You **can’t push** if you haven’t **committed** your changes.
2. You **can’t commit** if you haven’t **staged** your files.

It all follows this order:
```sh
# Stage your changes
git add .

# Commit your changes
git commit -m "Added README and initial project setup"

# Push your code (we’ll get to this part below)
git push
```

---

## **What is a README File?**

A **README** is the first thing people see when they visit your repository. It explains **what your project is, how to use it, and any important details**. Think of it as the homepage of your repo.

### **Why Should You Have a README?**
- 📌 **Explains your project** – What does it do? Why did you build it?
- 📜 **Guides users** – How can they install and use it?
- 🤝 **Helps contributors** – How can others help improve your project?

### **How to Create a README File**

1. Open your text editor (VS Code, Notepad++, etc.).
2. Create a new file and name it `README.md`.
3. Inside `README.md`, write something simple, like:

```md
# My Project

This is a simple project to demonstrate pushing to GitHub.

## Features
- Easy to use
- Organized file structure

## How to Use
1. Clone the repo
2. Run the project
```

4. Save the file in your project folder.

💡 **`README.md` uses Markdown (`.md`)**, a lightweight formatting language. It’s similar to HTML but much simpler. Instead of `<h1>Title</h1>` in HTML, you write `# Title` in Markdown.

---

## **Publishing (First-Time Push)**
Now that you have a README and some commits, let’s publish your project online.

Since this is your **first time pushing**, you need to connect your local project to a GitHub repository.

1. **Go to GitHub and create a new repository** (don’t initialize with a README, since we already created one).
2. **In your terminal, link your local repo to GitHub:**

```sh
git remote add origin https://github.com/yourusername/your-repo.git
```

3. **Push your project online:**

```sh
git push -u origin main
```

Now your project is live on GitHub! 🎉

From now on, every time you make changes, you only need to:
```sh
git add .
git commit -m "Updated README"
git push
```

And that’s it! Your code is safely stored online. 🚀

---

# **Pull – Getting the Latest Changes**  

If someone else updates the project on GitHub, you **pull** those changes to stay up to date.  

**Command:**  
```sh
git pull
```
Without pulling first, you **risk conflicts** when pushing your changes.  

---

# **Branches – Working Without Messing Up the Main Project**  

A **branch** is like an alternate universe for your code. You can experiment without screwing up the main project.  

**Commands:**  
- Create a new branch:  
  ```sh
  git branch <branch-name>
  ```  
- Switch to that branch:  
  ```sh
  git checkout <branch-name>
  ```  
- See all branches:  
  ```sh
  git branch
  ```

---

# **Merge – Bringing Everything Back Together**  

Once your branch is ready, you **merge** it into the main project.  

**Command:**  
```sh
git merge <branch-name>
```
Now all your changes are part of the main branch.  

---

## **Merge Conflicts – When Git Tells You to Fix Your Shit**  

A **merge conflict** happens when two people edit the same part of a file. Git doesn’t know which version to keep, so it asks **you** to decide.  

How to fix it:  
1. Open the file. You’ll see Git’s conflict markers.  
2. Choose which version you want.  
3. Remove the conflict markers.  
4. **Commit** the fixed file.  

---

# **Doing Everything in VSCode**  

If typing commands feels like **too much work**, VSCode has **Git built in**.  

### **1. Create a Repo**  
1. Open **VSCode**.  
2. Go to **Source Control** (it looks like a branch).  
3. Click **Initialize Repository**.  

### **2. Staging & Committing**  
1. Click the **+** next to files to stage them.  
2. Write a commit message.  
3. Click the ✅ checkmark to commit.  

### **3. Push Your Code**  
1. Click the **three dots** (menu).  
2. Select **Push**.  

### **4. Pull the Latest Changes**  
1. Click the **three dots**.  
2. Select **Pull**.  

### **5. Creating and Merging Branches**  
1. Click the **branch name** in the bottom left corner.  
2. Select **Create New Branch**.  
3. Make changes and commit.  
4. Switch back to `main`, then **merge**.  

If you want **bragging rights**, learn the commands. But VSCode’s GUI makes it **stupid easy** to use Git without memorizing them.  

---

## **Final Words – Just Use It**  

Git & GitHub **aren’t optional**—if you’re serious about coding, you need them. Now go **initialize a repo**, commit something, and push your first project.
