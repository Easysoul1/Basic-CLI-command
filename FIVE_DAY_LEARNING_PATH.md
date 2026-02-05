# 📚 Your First Week: 5-Day Learning Pathway

**A day-by-day guide to learning the command line. Recommended pace: 30-60 minutes per day.**

---

## 🎯 Learning Goals for This Week

By the end of this week, you will:
- ✅ Confidently navigate any folder on your computer
- ✅ Create files and folders from the command line
- ✅ Use Git to track your code
- ✅ Know the most important commands
- ✅ Understand how to keep yourself safe
- ✅ Feel ready to keep learning on your own

**Remember: It's okay to go slower! This is a guide, not a speed test.**

---

# 📅 DAY 1: JUST NAVIGATION

## Goal
Get comfortable moving around your file system. **Don't create, copy, or delete anything today - just look!**

## 🎓 What to Learn
1. Open your terminal
2. Understand the prompt
3. Use `pwd` to see where you are
4. Use `ls` or `dir` to look around
5. Use `cd` to navigate one folder

## 💻 Exercises

### Exercise 1: Opening and Greeting (5 minutes)
```
Open your terminal
Type: echo "Hello, CLI!"
Press Enter
See: Hello, CLI!
```
**Checkpoint:** ✅ If you see "Hello, CLI!" printed back, you did it!

---

### Exercise 2: Orientation (5 minutes)
```
Type: pwd
See: Your current location
(Example: /Users/sarah or C:\Users\Sarah)
```
**Checkpoint:** ✅ You know where you are!

---

### Exercise 3: Looking Around (5 minutes)
```
Type: ls  (Mac/Linux)
   or: dir (Windows)

See: List of folders and files in your current location
Try to recognize some of them from your GUI
```
**Checkpoint:** ✅ You can see what's in a folder!

---

### Exercise 4: First Navigation (10 minutes)

**On Mac/Linux:**
```
Type: cd Documents
Type: pwd
See: should end in /Documents

Type: ls
See: what's in your Documents folder

Type: cd ..
Type: pwd
See: back where you started
```

**On Windows:**
```
Type: cd Documents
Type: pwd or cd (to see current location)
See: should end in \Documents

Type: dir
See: what's in your Documents folder

Type: cd ..
Type: pwd or cd
See: back where you started
```

**Checkpoint:** ✅ You successfully navigated DOWN and came back UP!

---

### Exercise 5: Exploration (15 minutes)

**Pick any 3 folders and explore them:**

```
Type: cd Documents
Type: ls or dir
Type: cd (pick a subfolder)
Type: ls or dir
Type: cd ..
Repeat for 3 different folders
```

**Questions to ask yourself:**
- What's in my Documents folder?
- Can I see my Desktop files with `ls`?
- What does the Projects folder contain?

**Checkpoint:** ✅ You're comfortable navigating!

---

### Exercise 6: Tab Completion Practice (10 minutes)

**Try this in a folder with files:**
```
Type: cd Doc[TAB]
Press Tab - it completes to: Documents
Press Tab again to see other Doc* options

Type: l[TAB]
Press Tab - it should suggest: ls or similar
```

**Checkpoint:** ✅ You're typing less and feeling like a power user!

---

## 📝 Day 1 Summary

**Today you learned:**
- How to open and use the terminal
- `pwd` - knowing where you are
- `ls` / `dir` - seeing what files exist
- `cd` - moving between folders
- Tab completion - the best shortcut

**Tomorrow:** You'll create things!

---

---

# 🌅 DAY 2: CREATE AND VIEW FILES

## Goal
Create files and folders. View what you created. Learn that you CREATED them!

## 🎓 What to Learn
1. Create folders with `mkdir`
2. Create files with `touch` or `echo`
3. View files with `cat` or `type`
4. Verify everything with `ls`

## 💻 Exercises

### Exercise 1: Create Your First Project (10 minutes)

```
Type: cd Desktop
(or cd ~/Desktop or your preferred location)

Type: mkdir my_first_project
(Creates a folder)

Type: ls or dir
See: my_first_project appears in the list! ✅

Type: cd my_first_project
Type: pwd
See: you're inside my_first_project ✅
```

**Checkpoint:** ✅ You created your first folder!

---

### Exercise 2: Create Project Subfolders (10 minutes)

```
You're still in my_first_project

Type: mkdir src
Type: mkdir docs
Type: mkdir images
(Creates three folders)

Type: ls or dir
See: src, docs, images all appear ✅
```

**Checkpoint:** ✅ You have a project structure!

---

### Exercise 3: Create Files (10 minutes)

**On Mac/Linux:**
```
Type: touch README.md
Type: touch index.html
Type: touch notes.txt

Type: ls
See: all three files appear ✅
```

**On Windows:**
```
Type: echo. > README.md
Type: echo. > index.html
Type: echo. > notes.txt

Type: dir
See: all three files appear ✅
```

**Checkpoint:** ✅ You created files from the command line!

---

### Exercise 4: Add Content to a File (10 minutes)

**Create a file with content in one command:**

**On Mac/Linux:**
```
Type: echo "This is my first project!" > notes.txt

Type: cat notes.txt
See: This is my first project!
(Success! You just put content in a file!) ✅
```

**On Windows (PowerShell):**
```
Type: echo "This is my first project!" > notes.txt

Type: type notes.txt
See: This is my first project! ✅
```

**Checkpoint:** ✅ You created and populated a file!

---

### Exercise 5: Explore Your Created Structure (10 minutes)

```
Type: pwd
See: .../my_first_project

Type: ls or dir
See: src, docs, images, README.md, index.html, notes.txt

Type: cd src
Type: ls or dir
See: it's empty (that's ok!)

Type: cd ..
See: back in my_first_project

Type: ls
See: your structure again
```

**Checkpoint:** ✅ You understand what you created!

---

### Exercise 6: View Your Project (5 minutes)

**Find your project in your GUI file explorer:**
- Open Finder (Mac) or Explorer (Windows)
- Navigate to Desktop or wherever you created it
- See: my_first_project folder
- See: Inside: src, docs, images, and files
- See: **Everything you created with commands is here!** ✅

**Checkpoint:** ✅ Your CLI work appears in the GUI!

---

## 📝 Day 2 Summary

**Today you learned:**
- `mkdir` - creating folders
- Creating files (multiple ways)
- Adding content with `echo`
- `cat` / `type` - reading files
- That CLI and GUI show the same thing

**Tomorrow:** Copy, move, and organize!

---

---

# ☀️ DAY 3: MANAGE YOUR FILES

## Goal
Copy, move, and rename files. Practice being careful about what you delete.

## 🎓 What to Learn
1. Copy files with `cp` / `copy`
2. Move files with `mv` / `move`
3. Rename files (same as move!)
4. Safely practice deletion on test files

## 💻 Exercises

### Exercise 1: Copy a File (10 minutes)

```
Navigate to your project:
Type: cd Desktop/my_first_project
(or wherever you put it)

Create a backup of notes.txt:
Type: cp notes.txt notes_backup.txt  (Mac/Linux)
   or: copy notes.txt notes_backup.txt  (Windows)

Type: ls or dir
See: notes.txt AND notes_backup.txt ✅

Type: cat notes_backup.txt (or type on Windows)
See: It has the same content ✅
```

**Checkpoint:** ✅ You made a backup!

---

### Exercise 2: Rename a File (10 minutes)

```
You're in my_first_project

Rename index.html to index_home.html:
Type: mv index.html index_home.html  (Mac/Linux)
   or: move index.html index_home.html  (Windows)

Type: ls or dir
See: index.html is GONE, index_home.html exists ✅
(This is how moving/renaming works!)

Rename it back:
Type: mv index_home.html index.html
Type: ls
See: it's back to index.html ✅
```

**Checkpoint:** ✅ You renamed files!

---

### Exercise 3: Move a File to a Subfolder (10 minutes)

```
You're in my_first_project

Move notes.txt into the docs folder:
Type: mv notes.txt docs/
Type: ls or dir
See: notes.txt is GONE from here ✅

Type: ls docs/ or dir docs
See: notes.txt is in the docs folder! ✅

Type: cat docs/notes.txt (or type on Windows)
See: The content is still there ✅
```

**Checkpoint:** ✅ You organized your files!

---

### Exercise 4: Copy a Folder Structure (10 minutes)

**Create a backup of your entire project:**

**On Mac/Linux:**
```
Go back up:
Type: cd ..
Type: ls
See: my_first_project

Copy the whole folder:
Type: cp -r my_first_project my_first_project_backup

Type: ls
See: my_first_project AND my_first_project_backup ✅

Type: cd my_first_project_backup
Type: ls
See: Everything was copied (src, docs, images, etc.) ✅
```

**On Windows (using copy command recursively):**
```
This is trickier on Windows Command Prompt, so skip to GUI:
Use Explorer to copy the folder as backup (easier for now!)
```

**Checkpoint:** ✅ You backed up your project!

---

### Exercise 5: Safe Deletion Practice (15 minutes)

**⚠️ This is where we're CAREFUL!**

```
Go back to Desktop/my_first_project:
Type: cd ../my_first_project

Create a test file to safely delete:
Type: touch test_file.txt  (Mac/Linux)
   or: echo. > test_file.txt  (Windows)

Type: ls
See: test_file.txt exists

BEFORE DELETING, verify with ls:
Type: ls
See: test_file.txt ✅

Now delete it (this is PERMANENT):
Type: rm test_file.txt  (Mac/Linux)
   or: del test_file.txt  (Windows)

Type: ls
See: test_file.txt is GONE, not in Trash/Recycle ✅
(This shows deletion is final!)
```

**Checkpoint:** ✅ You understand why to be careful!

---

## 📝 Day 3 Summary

**Today you learned:**
- `cp` / `copy` - making copies
- `mv` / `move` - moving and renaming
- `cp -r` - backing up entire folders
- `rm` / `del` - permanent deletion
- **Lesson: Always check before deleting!**

**Tomorrow:** Version control with Git!

---

---

# 🌤️ DAY 4: INTRO TO GIT (Version Control Magic)

## Goal
Initialize Git, make your first commits, understand version control.

## 🎓 What to Learn
1. Git configuration (tell Git who you are)
2. `git init` to start tracking
3. `git add` to prepare changes
4. `git commit` to save versions
5. `git log` to see history

## 💻 Exercises

### Exercise 1: Configure Git (5 minutes)

**Tell Git who you are (one time setup):**

```
Type: git config --global user.name "Your Name"
(Replace "Your Name" with your actual name)

Type: git config --global user.email "you@example.com"
(Use a real email you can remember)

Verify it worked:
Type: git config --list
See: user.name and user.email appear ✅
```

**Checkpoint:** ✅ Git knows who you are!

---

### Exercise 2: Initialize a Git Repository (10 minutes)

```
Navigate to your project:
Type: cd Desktop/my_first_project
(or wherever you put it)

Initialize Git:
Type: git init

See: "Initialized empty Git repository in ..."

Type: ls -la  (Mac/Linux)
   or: dir    (Windows - but hidden folders don't show)

See: A .git folder (on Mac/Linux) ✅
This hidden folder stores all Git history!

Type: pwd
See: You're definitely in my_first_project ✅
```

**Checkpoint:** ✅ Git is watching your project!

---

### Exercise 3: Check Git Status (5 minutes)

```
You're in my_first_project

Type: git status

See something like:
"On branch master
No commits yet
Untracked files:
  src/
  docs/
  images/
  README.md
  etc."

This means Git sees your files but hasn't saved them yet ✅
```

**Checkpoint:** ✅ You understand what "status" means!

---

### Exercise 4: Stage Your Files (5 minutes)

```
You're still in my_first_project

Prepare all files to be saved:
Type: git add .

(The . means "everything in this folder")

Type: git status

See: Files are now "green" or "to be committed" ✅
This means they're ready to save!
```

**Checkpoint:** ✅ Files are staged!

---

### Exercise 5: Make Your First Commit (5 minutes)

```
You're still in my_first_project

Save a version (called a "commit"):
Type: git commit -m "Initial project setup"

See: "X files changed, X insertions..."
This means it saved! ✅

Type: git status

See: "nothing to commit, working tree clean"
Everything is saved! ✅
```

**Checkpoint:** ✅ Your first commit is saved!

---

### Exercise 6: View Your Commit History (10 minutes)

```
You're still in my_first_project

See all your commits:
Type: git log

See something like:
"commit abc123...
Author: Your Name <you@example.com>
Date: Day Month Date Time Year

    Initial project setup"

This is your commit! ✅

Press q to exit
Type: git log --oneline
See: A shorter version showing just the message ✅
```

**Checkpoint:** ✅ You can see your project history!

---

### Exercise 7: Make Changes and Commit Again (15 minutes)

```
Edit a file (or create a new one):
Type: echo "# My First Project" > README.md
(This overwrites the old empty file)

Type: git status
See: "README.md modified" (in red) ✅
Git notices you changed something!

Prepare it:
Type: git add README.md

Type: git status
See: "README.md to be committed" (in green) ✅

Commit it:
Type: git commit -m "Add project title to README"

Type: git log --oneline
See two commits now:
  - "Add project title to README"
  - "Initial project setup"
✅ You have history!
```

**Checkpoint:** ✅ You made multiple commits!

---

## 📝 Day 4 Summary

**Today you learned:**
- `git config` - configure Git
- `git init` - start tracking a project
- `git add .` - prepare files to save
- `git commit -m "message"` - save a version
- `git log` - see your history
- **Lesson: Every commit is a save point you can return to!**

**Tomorrow:** Combining everything + bonus GitHub!

---

---

# 🌞 DAY 5: PUTTING IT ALL TOGETHER + GITHUB

## Goal
Use everything you've learned to create a real project, and (optionally) share it on GitHub.

## 🎓 What to Learn
1. Building a complete project structure
2. Making meaningful commits
3. (Optional) Creating a GitHub repository
4. (Optional) Pushing your project to GitHub

## 💻 Exercises

### Exercise 1: Create a Real Project (15 minutes)

**Let's build something bigger:**

```
Go to Desktop:
Type: cd Desktop

Create a web project:
Type: mkdir my_website

Type: cd my_website

Create structure:
Type: mkdir css
Type: mkdir images
Type: touch index.html
Type: touch style.css
Type: touch README.md

Add real content:
Type: echo "<!DOCTYPE html><html><body><h1>Welcome</h1></body></html>" > index.html
Type: echo "body { font-family: Arial; }" > style.css

Verify with ls ✅
```

**Checkpoint:** ✅ You have a real project structure!

---

### Exercise 2: Initialize Git and Make Commits (15 minutes)

```
You're in my_website:

Type: git init

Type: git add .

Type: git commit -m "Create initial project structure"

Edit and commit again:
Type: echo "# My Website" > README.md

Type: git add .

Type: git commit -m "Add README with project title"

Edit HTML:
Type: echo "<!DOCTYPE html><html><body><h1>My Website</h1><p>Welcome!</p></body></html>" > index.html

Type: git add .

Type: git commit -m "Add welcome message to homepage"

View history:
Type: git log --oneline
See: 3 commits ✅
```

**Checkpoint:** ✅ You have a versioned project!

---

### Exercise 3: Practice Undoing Changes (10 minutes)

**Let's see how Git saves you:**

```
Make a change:
Type: echo "This is wrong" > README.md

Type: git status
See: "README.md modified"

Oops! Undo it:
Type: git checkout README.md
(Reverts to last commit)

Type: cat README.md
See: "# My Website" (the correct version) ✅
(Git saved you!)

Note: This only works if you haven't committed the bad change!
```

**Checkpoint:** ✅ You understand Git's safety!

---

### Exercise 4: Upload to GitHub (Optional - 20 minutes)

**If you want to share your code online:**

**Step 1: Create GitHub Account**
- Go to github.com
- Sign up (free account is fine)
- Verify your email

**Step 2: Create Repository on GitHub**
- Click "New Repository"
- Name it: "my_website"
- Click "Create Repository"
- Don't initialize with README (you have one already!)

**Step 3: Connect Your Local Project**

```
You're in my_website folder locally:

Type: git remote add origin https://github.com/YOUR_USERNAME/my_website.git
(Replace YOUR_USERNAME with your GitHub username!)

Type: git branch -M main

Type: git push -u origin main

See: Your code uploading ✅

Go to github.com and see your project there! ✅
```

**Checkpoint:** ✅ Your project is on GitHub!

---

### Exercise 5: Make Another Change and Push (10 minutes)

```
Make a change locally:
Type: echo "<!DOCTYPE html><html><body><h1>My Awesome Website</h1><p>Welcome to my site!</p></body></html>" > index.html

Commit it:
Type: git add .
Type: git commit -m "Improve homepage content"

Push to GitHub:
Type: git push

Go to github.com and refresh ✅
See your changes are online!
```

**Checkpoint:** ✅ You know the GitHub workflow!

---

### Exercise 6: Review Everything You've Done (15 minutes)

**Take a victory lap!**

```
View your project structure:
Type: ls -la

View your git history:
Type: git log --oneline

Count your commits:
Type: git log --oneline | wc -l (Mac/Linux)
   or just: git log --oneline (Windows)

You've done:
☑ Created folders
☑ Created files
☑ Copied and backed up
☑ Tracked with Git
☑ Made multiple commits
☑ (Optional) Pushed to GitHub

YOU'RE NOT A BEGINNER ANYMORE! 🎉
```

**Checkpoint:** ✅ You've completed the entire journey!

---

## 📝 Day 5 Summary

**This week you learned:**
- Day 1: Navigation (`pwd`, `ls`, `cd`)
- Day 2: Creating (`mkdir`, `touch`, `cat`)
- Day 3: Managing (`cp`, `mv`, `rm`)
- Day 4: Version Control (`git init`, `add`, `commit`)
- Day 5: Real Project + GitHub (optional)

---

---

# 🎓 Weekly Reflection

**Answer these questions to solidify your learning:**

1. **What was the easiest command to learn?**
   ```
   _____________________________________________
   ```

2. **What command still feels confusing?**
   ```
   _____________________________________________
   ```

3. **What did you create this week that you're proud of?**
   ```
   _____________________________________________
   ```

4. **What would you like to build next?**
   ```
   _____________________________________________
   ```

5. **How much more confident do you feel about the command line?**
   (1 = still scared, 10 = very confident)
   ```
   Rating: _____ out of 10
   ```

---

# 🚀 What's Next?

## Week 2-3: Consolidation
- Repeat these exercises with different projects
- Create projects for real purposes (not just practice)
- Join a coding community
- Help someone else learn the CLI

## Month 2: Deeper Learning
- Learn a programming language (Python is beginner-friendly)
- Learn more Git features (branches, merging)
- Customize your terminal (shell aliases, prompts)
- Start working on real projects

## Ongoing: Keep Growing
- Build real projects and share them
- Contribute to open-source projects
- Keep learning from:
  - Official docs
  - YouTube tutorials
  - Coding communities
  - Building cool stuff

---

# ✨ Final Words

**You started this week unable to use the command line.**

**You end this week with:**
- ✅ Practical command-line skills
- ✅ Version control knowledge
- ✅ A project on GitHub (optional)
- ✅ Confidence to learn more
- ✅ Real accomplishments

**That's incredible progress in 5 days!**

The command line is now YOUR tool. Use it. Build with it. Teach others.

**Welcome to the developer community!** 🎉

---

*If you got stuck anywhere, that's completely normal! Programming is about problem-solving. Google it, read the error message carefully, and keep going. You've totally got this!*

**Keep learning, keep building, keep pushing forward!** 🚀
