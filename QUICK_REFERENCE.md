# 🎯 Quick Reference Card: 20 Essential Commands

**Print this, laminate it, keep it near your desk!**

---

## Navigation Commands

| Command | What It Does | Example |
|---------|-------------|---------|
| `pwd` | Show current folder | `pwd` |
| `ls` | List files (macOS/Linux) | `ls` |
| `dir` | List files (Windows) | `dir` |
| `cd` | Go to a folder | `cd Documents` |
| `cd ..` | Go up one level | `cd ..` |
| `cd ~` | Go home (Mac/Linux) | `cd ~` |
| `cd -` | Go to previous folder | `cd -` |

## File Commands

| Command | What It Does | Example |
|---------|-------------|---------|
| `mkdir` | Create folder | `mkdir my_project` |
| `touch` | Create empty file | `touch file.txt` |
| `cat` | View file (Mac/Linux) | `cat file.txt` |
| `type` | View file (Windows) | `type file.txt` |
| `cp` | Copy file | `cp old.txt new.txt` |
| `copy` | Copy (Windows) | `copy old.txt new.txt` |
| `mv` | Move/rename | `mv old.txt new.txt` |
| `move` | Move (Windows) | `move old.txt new.txt` |
| `rm` | Delete file ⚠️ | `rm file.txt` |
| `del` | Delete (Windows) | `del file.txt` |

## Git Commands

| Command | What It Does | Example |
|---------|-------------|---------|
| `git init` | Start tracking | `git init` |
| `git add` | Stage changes | `git add .` |
| `git commit` | Save version | `git commit -m "message"` |
| `git log` | View history | `git log` |
| `git status` | See changes | `git status` |

## Bonus Tricks

| Trick | What It Does | How |
|-------|-------------|-----|
| Tab completion | Complete file names | Type start, press TAB |
| Command history | Repeat old commands | Press UP ARROW |
| Clear screen | Clean workspace | Type: `clear` |
| Get help | Learn about command | Type: `command --help` |
| Stop command | Halt running process | Press: **Ctrl+C** |

---

## Platform Quick Guide

### 🪟 Windows Command Prompt/PowerShell
```
Navigate: cd C:\Users\YourName\Documents
Create:  mkdir new_folder
List:    dir  (or ls in PowerShell)
View:    type file.txt
Delete:  del file.txt ⚠️
```

### 🍎 macOS Terminal
```
Navigate: cd ~/Documents
Create:   mkdir new_folder
List:     ls
View:     cat file.txt
Delete:   rm file.txt ⚠️
```

### 🐧 Linux Terminal
```
Navigate: cd ~/Documents
Create:   mkdir new_folder
List:     ls
View:     cat file.txt
Delete:   rm file.txt ⚠️
```

---

## Common File Extensions

| Extension | What It Is | Can View with `cat`/`type`? |
|-----------|-----------|---------------------------|
| `.txt` | Text file | ✅ Yes |
| `.md` | Markdown (fancy text) | ✅ Yes |
| `.json` | Data format | ✅ Yes |
| `.py` | Python code | ✅ Yes |
| `.js` | JavaScript code | ✅ Yes |
| `.html` | Web page | ✅ Yes |
| `.exe` | Program (Windows) | ❌ No (binary) |
| `.jpg` | Image | ❌ No (binary) |
| `.zip` | Compressed file | ❌ No (binary) |

---

## Safety Checklist Before Dangerous Commands

Before using **delete/move/copy commands**:

- [ ] Did I run `pwd` to confirm where I am?
- [ ] Did I run `ls` to see what I'm about to affect?
- [ ] Did I double-check the file name for typos?
- [ ] Did I back up important files?
- [ ] Am I 100% sure about what I'm doing?

**If you answered no to ANY, don't do it yet!**

---

## What Commands Look Like by OS

Same `ls` command, different output:

**macOS/Linux output:**
```bash
$ ls
Documents
Pictures
Projects
file.txt
```

**Windows (Command Prompt) output:**
```cmd
C:\Users\Sarah> dir
Documents             <DIR>
Pictures             <DIR>
Projects             <DIR>
file.txt              2,048 bytes
```

**Windows (PowerShell) output:**
```powershell
PS C:\Users\Sarah> ls
Documents             <DIR>
Pictures             <DIR>
Projects             <DIR>
file.txt              2,048 bytes
```

---

## Remember: Ctrl+C is Your Escape Button!

**Stuck or confused?** Press **Ctrl+C** (or **Cmd+C** on Mac)

It stops almost any command and gives you your prompt back.

---

## Emergency Command Cheat Sheet

| Problem | Solution |
|---------|----------|
| "I don't know where I am" | Type: `pwd` |
| "I don't see my file" | Type: `ls` to verify |
| "Command is frozen" | Press: **Ctrl+C** |
| "I don't understand an error" | Read it carefully + Google it |
| "I made everything wrong" | Breathe. Check Git: `git status` |
| "I need help about a command" | Type: `command --help` |

---

## Your First Week (TL;DR)

**Day 1:** Practice `pwd`, `ls`, `cd` - just moving around

**Day 2:** Add `mkdir`, `touch` - create stuff, don't delete yet

**Day 3:** Try `cp` and `mv` - practice with test files

**Day 4:** Learn `git init`, `git add`, `git commit` - version control practice

**Day 5:** Combine everything - create a project, commit, push to GitHub

**Week 2+:** Practice, practice, practice!

---

## Troubleshooting: Common Beginner Mistakes

**"Command not found"**
- Typo in command name? Check spelling
- Program not installed? Install it first
- On Windows? Use `dir` instead of `ls` (or use PowerShell)

**"Permission denied"**
- You don't have permission to access this
- Use something else if possible
- Or use `sudo` with caution (advanced)

**"Path not found" / "No such file or directory"**
- Folder or file doesn't exist
- Check spelling
- Run `ls` to see what files ARE there

**"File exists" / "Already exists"**
- You're trying to create something that already exists
- Rename it differently
- Or delete the old one first (carefully!)

---

## Key Takeaway

**The terminal is just a text-based way to tell your computer what to do.**

Once you know a few commands, you can do almost anything!

- Don't memorize - **Google is your friend**
- Don't be afraid - **errors don't break your computer**
- Do practice - **the more you use it, the easier it gets**

---

## Keep Learning

- Official documentation for each tool
- YouTube channels: "Command Line Tutorial"
- Practice sites: OverTheWire.org (fun challenges)
- Stack Overflow: When you're stuck on something specific

**You've got this!** 🚀

*Bookmark or print this reference - you'll use it constantly!*
