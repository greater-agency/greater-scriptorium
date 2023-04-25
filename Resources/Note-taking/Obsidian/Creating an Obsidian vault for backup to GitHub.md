You don't need to create a new Obsidian vault if you just follow the instructions for [[Cloning this repo and installing Obsidian]]. However, if you want your own vault for your own use, you can learn here how to create a new Obsidian vault for backup to GitHub.

See [[What is an Obsidian vault]] to learn that a vault is just a folder on your hard drive. When you designate a folder as a vault, Obsidian will create a hidden folder containing configuration files that set the Obsidian user interface.

## Create a vault

Here's how you could create a new `my-scriptorium` vault:
- Create a `my-scriptorium` folder on your Mac
- Launch Obsidian
- From the Obsidian default window, select "Open folder as vault" and choose the `my-scriptorium` folder

Alternatively, you can launch Obsidian, choose `File/Open Vault` and select "Create new vault."

## Add Files for GitHub

Before you go further, let's add files so you can backup your vault to GitHub.

GitHub expects a `README.md` file in the directory root. Create one with some informative content like this:

```
This is an archive of Markdown notes. 
```

You'll also need a hidden `.gitignore` file that excludes some files from backup operations.

```
### Obsidian

# to exclude Obsidian workspace settings (including plugin and hotkey configurations)
.obsidian/*

# OR only to exclude workspace cache
# .obsidian/workspace/*

# Exclude plugins
# .obsidian/plugins/*

# This file is used to keep track of last auto backup/pull
.obsidian-git-data

# Exclude Untitled Notes
Untitled*

# Exclude "bad" names
null*

### macOS

# Add below lines to exclude OS settings and caches
.trash/
.DS_Store
```

With a README and `.gitignore` file, you're ready to create a GitHub repository as a backup location for your Markdown files.

## Initialize Git

Before you create a GitHub repository, you'll need to initialize Git in the vault folder.

Open the `my-scriptorium` folder in your Terminal and enter:

```
git init .
git add -A
git commit -m "Initial commit"
```

This creates a hidden `.git` folder and commits all the files in the folder to a local Git repository. Going forward, if you need to, you can rollback changes to any previous Git commit. However, you probably won't use Git version control features for your local Makdown files. You'll just use Git to back up your files to an offsite GitHub repository. 

## Create a GitHub repository

Do you already have a GitHub account? Create a new repository named `my-scriptorium`. It's best if the repo has the same name as the folder on your local drive.

By default, the repository will be public. Switch it to private if you want to keep it private. The defaults are fine for all other settings.

GitHub's next page will show you commands to "push an existing repository from the command line."

```
git remote add origin https://github.com/YourAccount/my-scriptorium.git
git branch -M main
git push -u origin main

```

Don't copy the example above (or if you do, replace "YourAccount" with the correct account name).

Open the `my-scriptorium` folder in your Terminal and copy and paste the commands from the GitHub page.

In the Terminal, you'll see:

```
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

View the main page of the GitHub repository and you'll see the README and two files:

```
.gitignore
README.md
```

Great! You've got your Markdown files in your local `my-scriptorium` folder and a backup in a private repository on GitHub.

But wait. How can you automate the backup so you don't have to use Git commands in the Terminal every time you want to make a back up of yor Markdown files? Fortunately Obsidian community member Denis Olehov created an [Obsidian Git](https://github.com/denolehov/obsidian-git) plugin to automate backups from any Obsidian vault. See the next article, [[Automating Obsidian backups to GitHub]].

