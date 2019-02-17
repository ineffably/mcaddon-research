# mcaddon-research
Research notes for Minecraft Bedrock scripting and addons

## Getting started

I'm doing this on a Windows 10 machine, so all the commands and steps are against that OS.
You should know how to use a command console on Windows. 

- Create your project folders

  Figure out the best place to keep your code on your system. I use a git folder where I store most of my code.  
  ```cd c:\git\ ```
  
  make a folder where you want to store your mcaddons  
  ```mkdir mcworld```

  I'm going to use ```c:\git\mcaddons``` for my addon root as a reference. 

- Download VSCode

  [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
  
- Download Node LTS
   
   [https://nodejs.org/en/download/](https://nodejs.org/en/download/)

- Install Yo
  
  In a dos terminal or your VSCode terminal..
  
  ```npm i -g yo```
 
  This will install a utility framework called `yo` globally so that we can use it to setup projects using the package from the next step.
 
- Install the addon generator

  Install the generator package that yo will utilze for generating our templates and help test deploy and package the addon. source: [generator-minecraft-addon](https://github.com/minecraft-addon-tools/generator-minecraft-addon)

  ```npm i -g generator-minecraft-addon```

  This will install the generator globally so that you can use it from any location.  
  From @AtomicBlom who also has some great sample projects... 
  https://github.com/AtomicBlom
 
- Create your addon project using the generator

  In a terminal:  
  ```yo minecraft-addon```

  follow the prompts (there is a wait)  
  ```
   PS K:\mcaddons> yo minecraft-addon

       _-----_     ╭──────────────────────────╮
      |       |    │ So I heard you'd like to │
      |--(o)--|    │    create a Minecraft    │
     `---------´   │          Addon?          │
      ( _´U`_ )    ╰──────────────────────────╯
      /___A___\   /
       |  ~  |
     __'.___.'__
   ´   `  |° ´ Y `

  ? What will be the name of your addon? demo-A
  ? What will your addon do or provide? Demonstration of creating an addon project
  ? What namespace will you use? demoa
  ? What kind of modules will make up the addon? Behaviors, Resources
  ? Will you be adding scripts? Yes
  ? What language do you want to script in? JavaScript
     create package.json
     create gulpfile.js
     create packs\resources\manifest.json
     create packs\resources\pack_icon.png
     create packs\behaviors\manifest.json
     create packs\behaviors\pack_icon.png
     create packs\behaviors\scripts\client\client.js
     create packs\behaviors\scripts\server\server.js

  I'm all done. Running npm install for you to install the required dependencies. If this fails, try running the command yourself.
  ```
  Above is an example of what it looks like, follow the prompts.

-  Open up your project folder
  
    This has created a project folder with commands already setup in the `package.json` file.
    Use VScode to open the folder the generator created. For more info on `package.json` lookup [npm](https://docs.npmjs.com/creating-a-package-json-file).
    
    Here are the commands it generated for us: 
    ```
      "scripts": {
      "build": "gulp build",
      "watch": "gulp watch",
      "installaddon": "gulp install",
      "uninstalladdon": "gulp uninstall",
      "packageaddon": "gulp package"
    },
    ```
    
    - to install your addon use `npm run install` 
    - to just build your addon for validation `npm run build`
    - to package your addon for sharing `npm run package`

... next up investigating folders structures and some sample addons

## References
  https://minecraft.net/en-us/addons/ 
  https://minecraft.net/en-us/article/scripting-api-now-public-beta  
  https://minecraft.gamepedia.com/Bedrock_Edition_beta_scripting_documentation  
  https://minecraft.gamepedia.com/Bedrock_Edition_beta_add-on_documentation  
  https://minecraft.gamepedia.com/Bedrock_Edition_beta_MoLang_documentation  
  https://minecraft.gamepedia.com/Bedrock_Edition_beta_schemas_documentation  
  https://minecraft.gamepedia.com/Bedrock_Edition_beta_UI_documentation  
  https://minecraft.gamepedia.com/Bedrock_Edition_entity_components

## Resources
  Sample scripting from addons:  
  Turn based game:  https://aka.ms/minecraftscripting_turnbased  
  Mob Arena:  https://aka.ms/minecraftscripting_mobarena  
  
  Behavior and Resource packs (1.9.0)  
  https://aka.ms/behaviorpacktemplate  
  https://aka.ms/resourcepacktemplate  
  
  Dedicated server: has an example of new blocks and addons in a dedicated server format:  
  https://minecraft.net/en-us/download/server/bedrock/   
  
  Blockbench for custom models or twaking current models:  
  https://blockbench.net/
  
  UUID generator:  
  https://www.uuidgenerator.net/
  
  Online block designer:  
  https://codecrafted.net/blockdesigner
  
  Universal Mincraft Editor:  
  https://www.universalminecrafteditor.com/
  
  VSCode:  
  https://code.visualstudio.com/download
  
  Node LTS:  
  https://nodejs.org/en/download/
  
## Videos
  
  Hey, a good example of the setup! Pretty much an example of the steps above!  
  https://www.youtube.com/watch?v=G-piS_3--Kw
