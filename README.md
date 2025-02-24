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

## **Commits – Saving Your Work**  

A **commit** is like a save point in a video game. Every time you commit, you take a snapshot of your project so you can **go back if something breaks**.  

**Command:**  
```sh
git commit -m "Short, clear message explaining what you did"
```
🚨 **DON’T** write useless messages like `"commit"`,"`c`",`"final final"` or `"idk what this does"`. **Make them useful PLEASE**.  

---

## **Staging – Choosing What to Commit**  

Before committing, you **stage** files. Think of it like packing a suitcase—you decide which changes go into the next commit.  

**Commands:**  
- Stage one file:  
  ```sh
  git add <filename>
  ```
- Stage everything:  
  ```sh
  git add .
  ```  

If you don’t stage, **you can’t commit**.  

---

## **Push – Uploading Your Work**  

A commit only saves **locally**. To actually share it, you **push** it to GitHub.  

**Command:**  
```sh
git push
```
Now your teammates can see (and pull) your latest changes.  

---

## **Pull – Getting the Latest Changes**  

If someone else updates the project on GitHub, you **pull** those changes to stay up to date.  

**Command:**  
```sh
git pull
```
Without pulling first, you **risk conflicts** when pushing your changes.  

---

## **Branches – Working Without Messing Up the Main Project**  

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

## **Merge – Bringing Everything Back Together**  

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

## **Doing Everything in VSCode**  

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
