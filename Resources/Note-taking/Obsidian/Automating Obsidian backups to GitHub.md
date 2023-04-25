If you followed the instructions for [[Cloning this repo and installing Obsidian]], you don't need to set up automated backups to GitHub. This vault is already set up to push changes to the remote Git repository. However, if you set up another vault for your own use, you can learn here how to automatically backup your Markdown files to GitHub using the [Obsidian Git](https://github.com/denolehov/obsidian-git) community plugin.

Click the settings icon in Obsidian (the gear icon in the navigation ribbon). Or choose "Settings" from the menu. Under "Community plugins" click the button to "Turn on community plugins." Browse community plugins and search for "git." Find and click on "Obsidian Git." Then click "Install." This is not a system-wide setting; you'll need to install a plugin for each separate vault you create in Obsidian (plugins are saved to the hidden `.obsidian` folder in the vault). You can read about the Obsidian Git features and commands. Close the plugin modal.

Next you'll enable and Obsidian Git and configure its settings. Under "Community plugins," scroll down the list of installed plugins to find "Obsidian Git." Click the toggle icon to enable it. A gear will appear which you can click to configure it.

Set the "Vault backup interval" to a reasonable duration. Five minutes might be good. More frequently and you'll save tiny changes as separate commits in your GitHub repository. Less frequently and you might lose recent edits if your local hard drive fails.

Toggle on the setting for "Auto backup after file change." With this setting, Obsidian Git will wait 5 minutes after your last change before initiating a backup. That means you won't get tiny backups every five minutes while you are writing, only one backup 5 minutes after you stop writing.

You might want to set "Auto pull interval" for collaborative work. This setting is useful for shared notes if more than one person is saving notes to the same GitHub repository.

You can tweak the commit messages for manual or automated backups. You can also toggle "List filenames affected by commit in the commit body" and preview the commit message that will appear in the GitHub repository. There are additional configuration settings you might find useful.

Close the Obsidian Git settings. Then close and restart Obsidian and your backups will begin appearing in your GitHub repository about 5 minutes after you've completed any changes to notes.
