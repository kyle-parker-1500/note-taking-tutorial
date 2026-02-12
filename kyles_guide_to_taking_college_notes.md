# Easy College Notes (For CS Students Mostly)
This is a step by step guide to show you how to *A*, take good notes and *B*, study more efficiently.

## Taking "Effective" Notes ##
In this case, any notes are effective notes, so the style of them doesn't really matter. <br>
I'll attach some of my notes to this document to show you how I generally take notes.

1. You have to first ask yourself: Am *I* a VIM user?
  - The answer may be no at first but let me tell you this:
    - I used to hate sitting down to code, mostly because using a mouse was annoying to say the least, so I picked up VIM (and I'm never going back)
  - Basically your answer should be yes, but I'll account for both cases in-case you're not ready to take the leap
  - If you're not ready click this: [Link](#for-regular-people)

## For VIM Users ##
By the way, I'm including EMACS and other text editor users in this case. (Although if you use them and not VIM what are you even doing tbh)   -> :)

1. Install VIM. I would suggest **NeoVim** for everyone: Essentially it's VIM, just a newer version
  - Here's the [Link](https://neovim.io/doc/install/) for Windows and a blog [post](https://dev.to/ajtech0001/complete-guide-installing-and-configuring-neovim-on-macos-4a9e) for Mac
  - You can also get a NeoVim plugin on both **Intellij** and **VSCode** (which, if you're serious about learning VIM, is a great idea. (It's called immersion))
2. After installing NeoVim and getting it working -> you can check if it's working by doing `nvim --version` on both Unix (Mac and Linux) and Windows
3. (Optional) I would also *very* highly recommend you install a plugin manager for NeoVim. This just helps if you want a different look and feel for your NeoVim than the default (which looks boring and doesn't feel good). My current plugin manager is [LazyVim](http://www.lazyvim.org/), because I'm lazy and I like using VIM.
  - Pro tip: After doing this you can ask AI -> mainly Claude to create plugins for you! (This comes directly from Dr. C...'s blog post from a couple years ago) -> AND IT WORKS!
4. If you're not comfortable with using a plugin manager: I would suggest you use either VSCode or Intellij. I personally prefer VSCode because it takes less time to start up normally, and it feels more versatile. But it's really up to you.

### Time to take Notes ###
Now that we're ready to take notes, let me walk you through my typical setup. Since I know most of you are CS majors, I'll try to include a lot of pictures.
1. Launch your terminal. 
  - If you're on *Windows* you should install the *terminal app* ([Link](https://apps.microsoft.com/detail/9N0DX20HK701?hl=en-us&gl=US&ocid=pdpshare)) from the Windows Store and use Powershell with it. Alternatively (to powershell, you should definitely get *terminal*), you can use WSL2 to get a Linux style shell within Windows. Here's the tutorial for installation: [Link](https://learn.microsoft.com/en-us/windows/wsl/install)
  - Linux and Mac users, you're fine. (I bet all you Linux users are excited to be put before Mac in this sentence. It's probably the first time you've ever been picked first for anything... except hackathons :) )
2. Linux shame aside (I use Windows I shouldn't be talking), navigate to a folder that you want to take notes in.
  - These instructions are for those of you who don't know how to navigate through the terminal:
    - `cd directory` - to enter a directory -> *hint:* you can use `cd ..` to go up a directory (to go back to the previous directory) or `cd ../../../../..` to go back many directories. Using this you can go pretty much anywhere in your terminal. If you want to navigate to a different hard drive you can do `cd` to get to your root directory, then `cd drive:` it would look like -> `cd v:` or just `v:` if you're lazy.
    - `mkdir new_name` you can use `mkdir` to 'make directory', the `directory name` shouldn't contain any spaces. Although, I *think* you can include spaces if you do something like `mkdir "new_directory"` but that's bad practice, especially for programmers.
    - If you want to open VSCode from your current directory you can use `code .`, make sure you have an *environment variable* set up for VSCode first. You can also just open any file in VSCode using `code /this/is/a/path/name/directory(or file)`. Keep in mind, if you want to open a file you have to specify the file type.
    - `ls` -> use `ls` to list everything in the current or specified directory. Specified meaning `ls /path/to/dir`
    - `mv` to either move a file or rename -> *moving*: `mv filename.filetype ../previous_directory` or *renaming*: `mv filename.filetype new_filename.filetype`, you can also rename directories with this command.
    - `rm` -> be careful with this one. This is how you delete things: `rm filename.filetype`, if someone tells you to `rm -rf` something DON'T LISTEN TO THEM!! `-rf` is an option that recursively forces all files and all directories to be removed from your current or specified directory all the way down (this is only for Mac and Linux users though... I think).
    - Final thing -> use `pwd` to check your *present working directory*
    - That's basically it for basic terminal commands (these apply to both windows terminal and unix terminals). If you want something more advanced check out some guides online: Here's one -> [Link](https://serverspace.us/support/help/windows-cmd-commands-cheat-sheet/)
3. Now that our basic terminal commands tutorial is over let's get on to notes:
  - Navigate to the folder that you want your notes to be in. I would suggest naming it something like `SCHOOL_NAME/CLASS_NAME/notes` or you can do what I do and just have one directory for all notes `SCHOOL_NAME/CURRENT_SEMESTER/CLASS_NAME/CURRENT_WEEK (or current subject)`
    - Make sure that you are inside the directory that you want to be in. You can check this by doing `pwd` (present working directory)
4. Now we're going to initialize a Git repository. If you don't already have Git -> Git it: [Link](https://git-scm.com/install/) \*Nudge Nudge\* Git it, Git it... Okay I'll stop
  - We do this for 2 reasons: 1. So we can push changes to GitHub and it's remote repository (and access them from anywhere), and 2. So if we f*uck up (yes ik I didn't censor it properly), and want to restore an old version of our notes, we totally can.
    - By the way, this also allows your friends to add their own notes for a repository \**Pyramid Scheme*\*
  - So with my reasoning explained and Git installed: Let's do `git init`, alternatively you can clone a remote repository, but I prefer this method because it's more challenging, and I like challenging others.
  - This initializes a new repository on our local machine, that doesn't implicitly create a repository on GitHub, however. But we'll get to that. 
5. Now let's add some notes, these can be temporary or they can be real notes and you can come back to this tutorial later. Alternatively, you can drag this file into your notes folder.
  - I'll assume you want to learn how to use VIM though.
  - With NeoVim installed: You can navigate to your notes folder and type in `nvim filename.md`. We'll be using *markdown* files for our notes. This is because they're easy to write and we can translate them into beautiful notes just by typing in some symbols. Here's a [Link](https://www.datacamp.com/cheat-sheet/markdown-cheat-sheet-23).
  - That last command should open up a NeoVim terminal! Now, let's do a quick VIM tutorial. This most certainly will not cover everything but it is enough to get you started.

### NeoVim/Vim Tutorial ###
First off, here's a quick online game that you can play to get some of the movements down. [Link](https://vim-adventures.com/)

Vim is definitely much easier once you get the muscle memory down for the movements/commands. If you feel like this is too much, I can assure you, it only gets worse. BUT! Vim is an incredibly powerful text editor (or whatever it's actually called), and in a few months, or even a year, you'll be incredibly glad that you pushed yourself to learn it now. (It's useful in so many applications (also it looks cool)).
- Tip: You can run `vimtutor` in the terminal to learn the first commands too!
- Got that tip from: [Link](https://vim.rtorr.com/)

**Basic NeoVim Commands:**
| Commands | What They Do|
| -------------- | --------------- |
| k | Move Cursor Up |
| j | Move Cursor Down|
| h | Move Cursor Left |
| l | Move Cursor Right |
| esc (escape key) | Enter "Normal" Mode (for moving cursor) |
| : | Command Line Mode (for commands) |
| :w | Write to file (save) |
| :q | Quit file (make sure to write first!) |
| :wq | Write and then quit file |
| i | Insert Mode (for typing) |
| v | Visual Mode (highlighting) |
| w | Move to beginning of next word |
| e | Move to end of current word |
| b | Move to beginning of previous word |
| r | Replace current character |
| R | Keep replacing until esc is pressed |
| dd | Delete full line (and save it until something else is deleted ) |
| dd | Cut |
| dw | Delete word |
| yy | Copy Line |
| p | Paste saved text below cursor (either dd or yy, whichever was performed last) |
| P | Paste saved text above cursor (either dd or yy, whichever was performed last) |
| o | Insert empty line below cursor |
| O | Insert empty line above cursor |
| gg | Go to top of the file |
| G | Go to bottom of the file |
| gul | Make 1 character to the right lowercase |
| gUl | Make 1 character to the right uppercase |
| * | Display all instances of the word the cursor is on (can use n and N to navigate) |
| >> | Indent one line |
| << | Un-indent (idk what it's called) one line |
| / | Search (forward) through the file (you can use N and n to navigate which word you're on) |
These commands typically have limited history saved but they still work (just be careful):
| u | Undo |
| Ctrl+r | Redo |
| "*y | Copy specified text to clipboard |
| "*p | Paste text from clipboard |
Some Commands:
| :%s/word_to_replace/word_to_replace_with/ | Replace one instance of first word with second word |
| :%s/word_to_replace/word_to_replace_with/g | Replace all instances of first word with second word (without asking if it's okay to do so) |
| :%s/word_to_replace/word_to_replace_with/gc | Replace all instances of first word with second word (asks if it's okay) |
| :help | To help you learn all commands |
| :help specific_command | To help you learn one specific command |


Okay that's just about all the VIM commands I know. There's so many more though. So do your research and then come teach me some commands. The more unique the command the more extra credit I'll give you! (Just kidding, I can't give out extra credit).

Keep in mind you can add numbers before any of these commands to affect many more lines.

Side note: If you want to get to full screen in LazyVim on Windows you can use `LAlt+Enter` and press it again to leave.

- Okay! You're in VIM and you know how to use it!!
- Let's learn some markdown things now!

| Symbols | What They Do: | What They Should Look Like |
| --------------- | --------------- | --------------- |
| # | Header 1 (Biggest) | # Header # |
| ## | Header 2 (Second Biggest) | ## Header ## |
| ### | Header 3 (Third Biggest) | ### Header ### |
These Go Up to 6 ###### so I'm moving on. They just keep making the header text smaller.
| \`\` | Inline Code Highlighting (no syntax highlighting) | `code` |
| \`\`\`name of language \`\`\` | Block Code Highlighting (provides syntax highlighting if you provide the language)| ```c++ int x = 0;``` |
| 1. | Ordered List (Can indent) | 1. |
| \- | Unordered List (Can indent) | - |
| \*word\* | Italics | *word* |
| \*\*word\*\* | Bold | **word** |
| \-\[\] | Checklist | -[] (may not display properly) |
| \[\]\(\) | Link Something | [Text For Link Here](Link in here (no quotes needed)) [Link](https://github.com/kyle-parker-1500) |
| \!\[\]\(\) | Display Image | ![Alt Text For Image Here](Path name (no quotes needed)) |

I think that's about it. Like VIM there's many more, but I either haven't learned them or forgot about them. Play around with it though. You can also insert tables, but I'll let you figure that out on your own. LazyVim makes it really easy btw!

By the way! You can also use `<br>` to insert a newline just like html. In fact, you can use quite a few html tags in markdown.

Oh well, you're in CS because you want money right, so do some research.

Now that you know VIM and Markdown properly, write some notes! I'll wait right here.
. <br>
. <br>
. <br>
. <br>
. <br>

Okay, now let's `:wq` (write quit) the file and move on to updating your git repository. (Make sure you're using `:w` often when you write your notes.)

At least as often as when you save your code, if not more. Vim/NeoVim are not the greatest at saving your work if you lose it.

But that's why we have Git!

### The Git Part ###
Now that we have our notes, let's connect them to a GitHub remote repository so we can access our work from anywhere.

1. Go to GitHub and navigate to your account profile. It's typically going to be `https://github.com/your-username/`
  1. Navigate to the `Repositories` tab at the top next to `Overview`
  2. Click on `New` in the top right corner
  3. Give your repository a meaningful name (it makes it easier, trust me). I normally name mine something like: `IronManWasTheBestSupervillanAroundUntilHeTragicallyBecameASuperHeroAndSavedALotOfLivesForSomeReasonIMeanDudeHeDidntHaveToSnap` or something like that.
  4. Choose your repo visibility. Since we're writing notes, I typically make mine private so people don't find my badly written notes when searching for one of my projects
  5. Don't change anything besides that and create the repository.
  6. A window should pop up displaying a link similar to this one: `https://github.com/your-username/your-repo-name.git`
  - Note the `.git`, that's important for setting up your local repository so make sure you have it
  7. Copy the link and go back to your local machine (make sure you open the terminal (or keep it open) to where your notes are being stored)
  8. If you don't know if your notes are in your current directory remember to use `ls` (list) to check
  9. Your local repository should be initialized (remember we did `git init`), so we can now do: `git remote -v` to check if we have any remote repositories connected to our local one
  10. If anything other than absolutely nothing comes up either keep it because you likely know what you're doing OR do `git remote remove origin` (that removes your remote repository link)
  11. Also do `git status`. If, at the top left it says you're on branch `master` then you want to execute this command `git branch -M main` which will rename it to main
  - The reason we do this is because most of GitHub has moved away from using `master` as a root origin branch name
  
  12. Now execute this command: `git remote add origin your-link` for example: `git remote add origin https://github.com/kyle-parker-1500/note-taking-tutorial.git` That's my repository for this tutorial.
  13. It should say something along the lines of: *You didn't fuck up*
  14. Once that's done we want to now pull any changes made to our remote repository. We know there aren't any changes but it's good practice.
  - So do `git pull` to update your current branch (we should be on `main`)
  - If you aren't sure use `git status` to check
  15. Finally, we can stage our changes to be committed with `git add filename` or `git add .` -> this one stages all changes to be committed, the first one only stages specific files
  16. Now that we've staged our changes (you can do `git status` to check if they're staged) we can do `git commit -m "~-[,,_,,]:3 Meaningful Message"`. The `-m` stands for message, but you can omit it to pull up a VIM terminal to type your message to. (I told you VIM was useful!)
  17. Now that we've committed we can do `git push origin main` (for now you're just going to push to main, but you can theoretically push to any remote branch that you want to). This will take our committed changes and merge them into our origin/upstream branch on the remote repo.
  - Something to note: If you're lazy like me and don't want to type out 4 words each time you push, you can do `git push -u origin main`
  - This will set the upstream branch of `main` to be `origin main`, and then each time after that, to push, you can use: `git push` 

You should see a lot of text that says that Git is doing stuff. And then it should say successfully merged or something like that. 

Keep in mind, you could have merge conflicts if you and a friend are working on the same file!

And then you're done! Hope you end up using this method for taking notes in class! Click [Here](#use-ai-to-create-quizzes-for-yourself) to go to the AI Quiz portion of the Tutorial.

## For Regular People ##

## Use AI to Create Quizzes for Yourself ##

