This is a template for adding a new system to [Material Deck](https://github.com/MaterialFoundry/MaterialDeck).<br>
<br>
Download this template: https://github.com/MaterialFoundry/MaterialDeck_SystemTemplate/archive/refs/heads/main.zip<br>
Or clone it: `git clone https://github.com/MaterialFoundry/MaterialDeck_SystemTemplate`<br>
<br>
Below are all the steps you need to take to edit this template.<br>

### module.json
* id: Change to a unique ID that represents the system (lower case only, no spaces)
* title: Give the module a suitable title
* description: Give the module a suitable description
* authors: Add your personal data
* esmodules: Change `materialdeck-template` to whatever you set the id to. For example: `./materialdeck-dnd5e.js`
* relationships: Set the compatibility with the core Material Deck module
* compatibility: Set the compatibility with Foundry VTT
* url: Set to the (github) url of the module
* manifest: Set to the manifest url of the module
* download: Set to the download url of the module

### materialdeck-template.js
* Change the name of this file to what you set it as at 'esmodules' in module.json
* Fill in the 'data' variable

The 'system' class describes the system. It contains all the functions that Material Deck uses.<br>
Go through all functions and fill them in. For inspiration, take a look at how other systems do this: https://github.com/MaterialFoundry/MaterialDeck/wiki/Gaming-Systems<br>
Not all systems will use each function. If a function is unused, leave the function empty, or call a 'return'.<br>

### changelog.md
Keep the changelog up to date so people know what has been changed

### .github\workflows\main.yml
This file will automatically create a release for you if you use GitHub.<br>
<br>
You need to give the correct workflow permissions:
1. Go to the 'Settings' page of your GitHub repository
2. Go to the 'Actions/General' page
3. Scroll down to the 'Workflow permissions' section, and tick 'Read and write permissions'

Before you continue, make sure you change the filename on line 32 from `materialdeck-template.js` to whatever you named the main file.<br>
<br>
You can now head to the 'Releases' page on your GitHub repository, create a new release using the 'Draft a new release' button. Give it a tab and title and press 'Publish release'.<br>
The action defined in .github\workflows\main.yml will now be called. This action will fill in the manifest.json with the correct data, and package the module in a .zip file. When it's done, these files will be added to your release.

### README.md
Lastly, edit this readme