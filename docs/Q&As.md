# Questions and answers

Compilation of our library carpentry workshop notes

#### Q: what is a gitignore file?

we can choose to keep some sensitive files out of git repo using gitignore so that it is not tracked
The gitignore is a text file in the repository directory, and we can specify any files there that we do not want to track - for example, files with sensitive information or temporary files  

!!! Important    
    See common gitignore files here [link](https://github.com/github/gitignore)

Example Python .gitignore file

```gitignore
# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class

# C extensions
*.so

# Distribution / packaging
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
share/python-wheels/
*.egg-info/
.installed.cfg
*.egg
MANIFEST
```



#### Q: does git work with office files?

Most MS Office files (docx, xlsx) are actually saved as a compressed xml file or file(s). However this format doesn't easily facilitate optimal version tracking with git. Long answer is There are projects like pandoc and rezip which tries to accommodate office files in git.

#### Q: Why would we use command-line if this can be done on the interface? 

A: It comes down to preference and workflows for the user's other tasks. In the development/data world it is common to use the terminal because you are "already there."  The interfaces are a viable option, but they may distance you from the processes themselves and/or give you less information for troubleshooting. 

#### Q: is there a best practice for when you want to go from add to commit

A:  think of commit as a thematic update.  Trevor usually commits at the end of the day.  Sounds like some of this is team-determined.
There is some lesson content on reconciliation of conflicts, that won't be covered in detail today, but you can look up.
TIP: Remember to pull - especially if working on a project with many other people. 

#### Q: When do you need to 'fetch' as opposed to 'pull'? 

A: git fetch is similar to pull but doesn't incorporate the changes right into your repository. This is a good way to see and review any changes. When ready to actually bring in the changes (not just look) then git pull.

#### Q: Can you talk a little about branches and how they are used to organize a project? 

A: Branches: when collaborating with others, organizing a project, instead of trying to push changes directly to a repository, make a local copy, turn it into a branch (remove it from the immediate workflow), make changes on that branch, then push over to the remote repository, does not get incorporated immediately like a normal push, but there is a pull request for review before they are incorporated. Cloning vs. forking: cloning: put a repository on our own machine. "Personally I think you can use them synonymously" You don't have to associate a cloned repository with someone's master repository, you can use it for your own purposes. Clone "put it on your machine". Fork: very synonymous. If you want to incorporate your changes, then use a branch. REMEMBER these are somewhat advanced concepts. Take software carpentry Git lesson, walks through additional steps. http://swcarpentry.github.io/git-novice/ 
TIP: this is the branching resource: https://learngitbranching.js.org/

#### Q: In order to practice, can you show us how to share our repositories with fellow classmates?

1. from settings, add a collaboration
2. or, share the link so that they can fork (make copy), make changes and send you a pull request to fetch their chages

#### Q: How do I create more space between the command line and the bottom of my GitBash window? 

I saw Trevor do that a few times today.
clear command might help with screen clutter; You can also type Ctrl + L

#### Q: refusing to push

pull first

#### Q: refusing to pull with upstream message in error 

```bash
git branch --set-upstream-to=origin/main main
```


If  you are using master, use master 

#### Q: Why is "Master" not used anymore in GitHub? 

A: There is movement away from colonialist vocabulary.

#### Q: unrelated histories error

```bash
git pull --allow-unrelated-histories origin main
```

**Q: What is that .git folder?**

A: that’s where git is tracking the change information “.git” is generally a “hidden” file but you can set preferences in explorer or use a flag in the shell to display those files. use ls -a to show hidden files. things that start with a '.' are often hidden by default

**Q: hash reference / hash value?** 

A computed value, the computer is looking at the exact length of the file and creating a mathematical value, it's a technique out of cryptography. Different algorithms calculate the hash values. When git was developed, this was an unambiguous way to reference different changes (although "hash collisions" may occur!) First 7 digits is a shorter reference.

**Q: How do I create a branch in a collaborator's project? Can I do it after cloning?** 

A: asd

**Q: What are the different levels of authorization?** 

A: Gitlab has different levels https://docs.gitlab.com/ee////////user/permissions.html

**Q: A branch is kind of like a breakout group?** A: :) that’s a good analogy - and when you make a “pull request” that is bringing whatever you discussed in the breakout room to the whole group

**Other tools for a little more user-friendly or not-command-line work:**

See [tools](/working-with-git)

* Atom (https://flight-manual.atom.io/)

* SourceTree

* VScode

* Github Desktop

**Q: I don't understand why we need to put quotes around user name and email but not when we make a directory of hello-world.** 

Short answer: There are some things you need quotes around, and some things you don't. :-). In general, when giving a command an argument (like cd), don't need quotes.

**Q: If I'm not signed in to GitHub, will the git commands still work?** 

Yes.

Check if you have git: **git --version** , if you get a response, you are in good shape

Navigate to the new hello-world directory you just made. Type **git init**. see if anything happened, type ls -a, you should see the "hidden files/folders", .git

**git status**.  - what has changed? (probably nothing right now)

**Q: How did you change the default branch name from 'master' to 'main'?** 

A: new versions use main, older versions use master. Previously git used the word 'master' to all primary repositories, they recent changed that to 'main' instead of 'master' but in the curriculum it may still say 'master' because it is a recent change.

**Q: If you edit a file, do git add on it, and edit it some more, will it commit the last changes you made to the file or only the changes when you ran git add?** 

A: it will only commit the changes you performed the add command on

