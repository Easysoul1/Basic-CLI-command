# 🗺️ Visual Command Map: How CLI Commands Relate

**A visual guide to understanding how different commands work together.**

---

## The Command Relationship Diagram

```
                        YOU (at the terminal)
                              |
                    ___________+___________
                   |                       |
             NAVIGATION              FILE OPERATIONS
             (Where am I?)           (Create/Read/Modify/Delete)
                   |                       |
        ___________|_________     _________|_________
       |           |         |   |       |      |    |
      pwd         ls        cd  mkdir  touch  cat   cp
      (show)   (list)   (go)  (make   (make  (read)(copy)
                             folder) empty)
                                  |
                                  v
                            For viewing:
                           cat, type, less
                            |
                            v
                         FILE CONTENTS


                         VERSION CONTROL
                            (Git Magic)
                              |
                    __________|__________
                   |          |         |
                 init       add      commit
              (start)    (stage)     (save)
                           |
                           v
                        log (see history)
                           |
                           v
                        reset (undo)


                          ORGANIZATION
                          (Management)
                              |
                    __________|__________
                   |          |      |
                  mv         rm    rmdir
               (move)   (delete)  (remove)
              (rename)            (empty folder)
                           |
                           v
                     Backup workflow:
                     cp -r (copy folder)
```

---

## Command Categories

### 🧭 **NAVIGATION COMMANDS** - "Where Are You?"

These commands help you move around and see what's where.

```
┌─────────────────────────────────────────────┐
│           NAVIGATION WORKFLOW                │
├─────────────────────────────────────────────┤
│                                             │
│  1. pwd ──→ "Where am I?" ✅               │
│                                             │
│  2. ls/dir ──→ "What's here?"              │
│                                             │
│  3. cd ──→ "Go there"                      │
│                                             │
│  Repeat: pwd → okay? → ls → interesting?   │
│           → cd → new location               │
│                                             │
└─────────────────────────────────────────────┘
```

**Flow Example:**
```
$ pwd
/Users/sarah

$ ls
Documents  Pictures  Projects

$ cd Documents

$ pwd
/Users/sarah/Documents

$ ls
Resume.pdf  Cover Letter.docx  Portfolio
```

---

### 📁 **FILE CREATION COMMANDS** - "Make Something"

These commands create new items in your file system.

```
┌──────────────────────────────────────┐
│      CREATION WORKFLOW               │
├──────────────────────────────────────┤
│                                      │
│  mkdir ──→ Creates folder            │
│  └──→ touch/echo ──→ Creates file    │
│       └──→ echo "content" > file     │
│           ──→ Creates file WITH data │
│                                      │
└──────────────────────────────────────┘
```

**Progression Example:**
```
$ mkdir my_project          ← Create folder
$ cd my_project             ← Enter it
$ mkdir src docs            ← Create subfolders
$ touch index.html          ← Create empty file
$ echo "Title" > README.md  ← Create WITH content
```

---

### 📖 **FILE READING COMMANDS** - "What's Inside?"

These commands let you view file contents.

```
┌──────────────────────────────────────┐
│      READING WORKFLOW                │
├──────────────────────────────────────┤
│                                      │
│  cat/type ──→ View entire file       │
│                                      │
│  For long files:                     │
│  less/more ──→ View page by page     │
│        └──→ Press SPACE to scroll    │
│        └──→ Press Q to quit          │
│                                      │
└──────────────────────────────────────┘
```

**Example:**
```
$ ls
essay.txt

$ cat essay.txt
[shows entire file]

$ less large_file.txt
[shows first page, press space for more]
```

---

### 🔄 **FILE MANAGEMENT COMMANDS** - "Organize Your Stuff"

These commands move, copy, rename, and delete files.

```
┌─────────────────────────────────────────────┐
│    FILE MANAGEMENT WORKFLOW                 │
├─────────────────────────────────────────────┤
│                                             │
│  BEFORE ANY CHANGE:                        │
│  1. pwd ──→ Know where you are            │
│  2. ls  ──→ See what you're affecting      │
│  3. THINK ──→ Is this what I want?        │
│                                             │
│  THEN DO THE OPERATION:                    │
│                                             │
│  cp: file → file_copy (duplicate)          │
│  mv: file → new_location (move OR rename)  │
│  rm: file → GONE (PERMANENT!)              │
│                                             │
└─────────────────────────────────────────────┘
```

**Decision Tree:**
```
I want to:
├─ Keep the original AND have a copy?
│  └─ Use: cp file.txt backup.txt
│
├─ Move to different folder?
│  └─ Use: mv file.txt Documents/
│
├─ Rename it?
│  └─ Use: mv old_name.txt new_name.txt
│
├─ Delete it? ⚠️
│  └─ First: ls (confirm)
│  └─ Think: Really sure?
│  └─ Then: rm file.txt (PERMANENT!)
│
└─ All of above on folders?
   └─ Add -r flag: cp -r folder/ backup/
```

---

### ⏰ **GIT WORKFLOW** - "Save and Track"

This is the most important developer workflow.

```
┌──────────────────────────────────────────────────┐
│         GIT WORKFLOW (The Circle)                │
├──────────────────────────────────────────────────┤
│                                                  │
│     ┌─────────────────────────────────┐         │
│     │    Modify/Create Files          │         │
│     │    (edit README.md, etc.)       │         │
│     └──────────┬──────────────────────┘         │
│                │                                │
│                ▼                                │
│     ┌─────────────────────────────────┐         │
│     │   git add .                     │         │
│     │   (Stage the changes)           │         │
│     └──────────┬──────────────────────┘         │
│                │                                │
│                ▼                                │
│     ┌─────────────────────────────────┐         │
│     │   git commit -m "message"       │         │
│     │   (Save a version)              │         │
│     └──────────┬──────────────────────┘         │
│                │                                │
│                ▼                                │
│     ┌─────────────────────────────────┐         │
│     │   git push (optional)           │         │
│     │   (Upload to GitHub)            │         │
│     └──────────┬──────────────────────┘         │
│                │                                │
│                └──── Repeat! ────────────────┐  │
│                                              │  │
│     When you make more changes, go back    │  │
│     to "Modify Files" ✅                    │  │
│                                              ▼  │
│                                   (always git loop)
│
│  Debug: git status → see what changed
│         git log → see all versions
│
└──────────────────────────────────────────────────┘
```

**Real Example:**
```
$ git init                          Step 1: Start tracking

$ echo "Project" > README.md        Step 2: Make changes
$ git add .                         Step 3: Stage
$ git commit -m "Add README"        Step 4: Save version

$ echo "More info" >> README.md     Step 5: Make more changes
$ git add .                         Step 6: Stage again
$ git commit -m "Expand README"     Step 7: Save new version

$ git log --oneline                 See all versions ✅
2 commits now!
```

---

## The Complete Daily Workflow

**How everything fits together when you're actually working:**

```
MORNING: Start Work
├─ Open terminal
├─ pwd (know where you are)
├─ cd project_folder
├─ git status (see current state)
└─ Ready to work!


DURING DAY: Work Normally
├─ Create files: touch, mkdir, echo
├─ Edit files: (use editor like VS Code)
├─ Check progress: ls, cat, pwd
└─ Get lost: pwd, ls to reorient


AFTERNOON: Save Work
├─ Check what changed: git status
├─ Review changes: git diff (advanced)
├─ Stage changes: git add .
├─ Save version: git commit -m "what I did"
├─ Verify saved: git log --oneline
└─ Create backup: cp -r project/ project_backup/


EVENING: Share Work (Optional)
├─ git push (upload to GitHub)
├─ Check github.com
└─ Celebrate! ✅
```

---

## Command Relationships: Quick Reference

### If You Want To... Use This Command

| Goal | Command | Example |
|------|---------|---------|
| Know where you are | `pwd` | `pwd` |
| See what's here | `ls` / `dir` | `ls` |
| Go somewhere | `cd` | `cd Documents` |
| Make folder | `mkdir` | `mkdir projects` |
| Make file | `touch` | `touch file.txt` |
| View file | `cat` / `type` | `cat file.txt` |
| Copy file | `cp` | `cp old.txt new.txt` |
| Copy folder | `cp -r` | `cp -r old/ new/` |
| Move/rename | `mv` | `mv old.txt new.txt` |
| Delete file | `rm` | `rm file.txt` |
| Delete folder | `rmdir` | `rmdir empty_folder` |
| Start git | `git init` | `git init` |
| Prepare changes | `git add` | `git add .` |
| Save version | `git commit` | `git commit -m "msg"` |
| See history | `git log` | `git log` |
| See status | `git status` | `git status` |

---

## Platform-Specific Differences

```
┌────────────────────────────────────────────┐
│  WINDOWS COMMAND PROMPT                    │
├────────────────────────────────────────────┤
│  pwd        →  cd (alone) or echo %cd%    │
│  ls         →  dir                        │
│  cat        →  type                       │
│  cp         →  copy                       │
│  mv/rename  →  move                       │
│  rm         →  del                        │
│  rmdir      →  rmdir                      │
│                                           │
│  Paths use:  C:\ (backslash)             │
│  Special:    Use cd: or cd /d C: to      │
│              change drives               │
└────────────────────────────────────────────┘

┌────────────────────────────────────────────┐
│  WINDOWS POWERSHELL                        │
├────────────────────────────────────────────┤
│  Accepts both CMD and Unix commands!      │
│  pwd        →  pwd or cd (alone)          │
│  ls         →  ls (Unix-style)            │
│  cat        →  cat                        │
│  cp         →  cp                         │
│  mv         →  mv                         │
│  rm         →  rm                         │
│                                           │
│  Paths use:  Both / and \ work            │
│  BONUS:      Accepts Unix commands! ✅   │
└────────────────────────────────────────────┘

┌────────────────────────────────────────────┐
│  MACOS/LINUX TERMINAL                     │
├────────────────────────────────────────────┤
│  pwd        →  pwd                        │
│  ls         →  ls                         │
│  cat        →  cat                        │
│  cp         →  cp                         │
│  mv         →  mv                         │
│  rm         →  rm                         │
│  rmdir      →  rmdir                      │
│                                           │
│  Paths use:  / (forward slash)           │
│  Special:    ~ is your home              │
│  Bonus:      Most compatible with        │
│              tutorials online ✅         │
└────────────────────────────────────────────┘
```

---

## Avoid These Command Combinations!

```
⚠️  DANGEROUS!                    WHY?
═══════════════════════════════════════════════
rm -rf /                         Deletes ENTIRE system
rm -rf C:\                       Deletes ENTIRE system
rm -rf *                         Deletes everything here
sudo rm -rf /                    Same but with super powers
format C:                        Formats your main drive
dd if=/dev/zero of=/dev/sda     Overwrites your hard drive

RULE: Before rm, always:
1. pwd (confirm location)
2. ls (confirm what's here)
3. THINK (really sure?)
4. Then rm (PERMANENT!)
```

---

## The Mental Model

**Think of your file system like a city:**

```
CITY STRUCTURE:
├─ Main Directory (city center)
│  ├─ Documents (street)
│  │  ├─ Work (building)
│  │  │  └─ Report.docx (room)
│  │  └─ Personal (building)
│  ├─ Pictures (street)
│  └─ Projects (street)

COMMANDS ARE DIRECTIONS:
├─ pwd = "Where am I?" (current intersection)
├─ ls = "What's nearby?" (what's on this street)
├─ cd Documents = "Go to Documents street"
├─ mkdir Work = "Build a building here"
├─ touch Report.docx = "Create a room"
├─ cp Report.docx Report_backup.docx = "Duplicate room"
├─ mv Report.docx Work/ = "Move building elsewhere"
└─ rm Report.docx = "DEMOLISH the room" (GONE!)

GIT = TIME MACHINE:
├─ git init = "Start recording history"
├─ git add = "Record snapshot of now"
└─ git commit = "Label snapshot with name"
```

---

## Debug Decision Tree

```
ERROR or STUCK? Follow this:

1. Did I read the error message?
   ├─ YES → What does it say? Google it
   └─ NO → Read it now! Usually tells you the issue

2. Am I in the right folder?
   ├─ Not sure? → Type: pwd
   ├─ Wrong place? → Type: cd correct_place
   └─ Right place? → Continue

3. Do the files I expect exist?
   ├─ Not sure? → Type: ls (or dir on Windows)
   ├─ Don't see them? → Create them or navigate to them
   └─ See them? → Continue

4. Is the command typed correctly?
   ├─ Check → Spelling
   ├─ Check → Spaces
   ├─ Check → Quotes and special characters
   └─ Try again more carefully

5. Still stuck?
   ├─ Google the error message
   ├─ Copy and paste EXACT error text
   ├─ Read Stack Overflow answers
   ├─ Ask on GitHub Discussions
   └─ Take a break (sometimes it helps!)
```

---

## Progressive Mastery Levels

```
LEVEL 1: BEGINNER (Days 1-5)
├─ pwd, ls, cd
├─ mkdir, touch
├─ cat, cp, mv, rm
├─ git init, add, commit
└─ Understanding structure

LEVEL 2: INTERMEDIATE (Weeks 2-4)
├─ Advanced git (branches, merge)
├─ Pipes and redirection (|, >)
├─ Scripting basics
├─ File permissions (chmod)
└─ Environment variables

LEVEL 3: ADVANCED (Month 2+)
├─ bash scripting
├─ Regular expressions
├─ Process management
├─ Network commands
└─ System administration

YOU ARE HERE: ↓ (after this week)
    LEVEL 1 ✅ → Ready for LEVEL 2!
```

---

## Your Brain After This Guide

```
BEFORE:
  "What is the command line?"
  [confused brain] 😵

AFTER:
  ┌──────────────────────────────────┐
  │ • I can navigate files           │
  │ • I can create things            │
  │ • I can organize my work         │
  │ • I can track changes with Git   │
  │ • I know what's safe & unsafe    │
  │ • I can find help when stuck     │
  │ • I can build real projects      │
  │ • I'm ready for more learning!   │
  └──────────────────────────────────┘
  [confident brain] 🧠✨
```

---

*Print this map and pin it near your workspace!*

**Use this visual guide when:**
- You forget how commands fit together
- You want to plan your workflow
- You need a quick reference
- You're helping someone else learn

**Remember:** Every expert programmer uses these same basic commands daily. You're now part of that community! 🎉
