With Obsidian as your Markdown editor, you can use the [Obsidian Text Generator Plugin](https://github.com/nhaouari/obsidian-textgenerator-plugin) to send prompts to the OpenAI API and store responses as content in Markdown files. 

For *prompt engineering*, you can use the same plugin for creating prompt templates to set up reusuble prompts for call to the OpenAI API.

You can add extended context to your prompts from a note or linked notes. The plugin will send extended context to the OpenAI API, which will consider both the context and the prompt while generating the response. You can combine prompt templates with extended context for tasks such as classifying, sorting, and reformatting repetitive content.

## Configuration

If you followed the instructions for [[Cloning this repo and installing Obsidian]], you don't need to install the Obsidian Text Generator Plugin. It's already installed and set up in this repository.

However, you'll need to configure the plugin with an OpenAI API key. For security, this repository's `.gitignore` file excludes a file `.obsidian/plugins/obsidian-textgenerator-plugin/data.json` that contains an OpenAI API key. Configuring the plugin with an OpenAI API key will restore the file locally with the OpenAI API key so the plugin can connect with the OpenAI API.

1.  Create an account at OpenAI (if you haven't already) and obtain an API key from their website.
2.  In Obsidian, go to the settings for the Text Generator Plugin.
3.  Enter the API key from OpenAI in the appropriate field.
4. Choose the OpenAI model you will use.

## Installation

If you are setting up a new Obsidian vault and you want to use AI features, you can follow these steps to install the Obsidian Text Generator Plugin.

You can view [illustrated instructions](https://text-gen.com/installing-text-generator-plugin) at text-gen.com.

1.  Go to Obsidian settings (gear icon in the lower-left corner).
2.  Navigate to "Community plugins" and enable "Community Plugins" if not already enabled.
3.  Click "Browse" to open the plugin browser.
4.  Search for "Text Generator" in the search bar.
5.  Click "Install" on the Text Generator Plugin.
6.  After the installation is complete, click "Enable" to activate the plugin.

After installing the plugin, you need to configure it by providing an API key from OpenAI:

1.  Create an account at OpenAI (if you haven't already) and obtain an API key from their website.
2.  In Obsidian, go to the settings for the Text Generator Plugin.
3.  Enter the API key from OpenAI in the appropriate field.
4. Choose the OpenAI model you will use.

To get a better idea of the capabilities of the AI plugin, view the settings for the Text Generator Plugin. See the documentation at [text-gen.com](https://text-gen.com/.

Now, the Text Generator Plugin is installed and configured, and you can start using it with the OpenAI API in Obsidian. See the [Text Generator Plugin](https://text-gen.com/) wiki for usage instructions.

## Templates for AI prompts

The Text Generator Plugin is powerful for single-use requests to the OpenAI API. It's even more powerful with templates.

To install example templates, use the Obsidian power key Command-p and enter "textgen." You'll see a list of Text Generator Plugin commands.  Select "Text Generator: Template Packages Manager." Click "Default Prompts Package" and click the button "Install."

Check the file view (in the sidebar) and you'll see a new foder `textgenerator` containing a folder `prompts`. You can copy and modify the  examples in the `default` folder.

When you want to use a prompt template, use the Obsidian power key Command-p and enter "textgen." Choose "Text Generator: Templates: Generate and Insert." You'll see a list of available templates (here, "templates" means "reusable AI prompts"). For example, choose the template "Summarize." If you have the text cursor on a line by itself, and no text is selected, the plugin will connect to connect to the OpenAI API submitting a prompt defined in the file `textgenerator/prompts/default/summarize` and providing the contents of the current page as context. In a few seconds, a summary of the current page will be inserted at the cursor location.

