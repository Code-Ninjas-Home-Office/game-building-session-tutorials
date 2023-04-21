# Catch the Ninja Stars

info.onCountdownEnd(function () { 

    game.gameOver(true) 

}) 

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) { 

    sprites.destroy(otherSprite) 

    info.changeScoreBy(1) 

}) 

let mySprite2: Sprite = null 

game.splash("Catch as many ninja stars as you can in 10 seconds!") 

scene.setBackgroundColor(4) 

let mySprite = sprites.create(assets.image`myImage`, SpriteKind.Player) 

controller.moveSprite(mySprite) 

mySprite.setStayInScreen(true) 

info.setScore(0) 

info.startCountdown(10) 

music.play(music.melodyPlayable(music.baDing), music.PlaybackMode.UntilDone) 

effects.confetti.startScreenEffect() 

game.onUpdateInterval(1000, function () { 

    mySprite2 = sprites.create(assets.image`myImage1`, SpriteKind.Food) 

    mySprite2.setPosition(randint(0, 160), randint(0, 120)) 

}) 

```assetjson 

{ 

  "README.md": " ", 

  "assets.json": "", 

  "images.g.jres": "{\n    \"image1\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAA8PAAAAAAAA8AAAAPAPAAD//wDwDwAA8L/9D///D/D//xH/////////8f/////////b/////wD///H/////////Ef//////8L/9D///D/AA//8A8A8AAAAAAAAA8A8AAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"myImage\"\n    },\n    \"image3\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAP8AAAAAAADwDwAAAAAAAL8PAAAAAA8Azw8AAAAA//+s/A8AAADwyzrK+wAAAAD/rPz/DwAAAADPDwAPAAAAAL8PAAAAAAAA/wAAAAAAAPAPAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"displayName\": \"myImage1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myImages\"\n    }\n}", 

  "images.g.ts": "// Auto-generated code. Do not edit.\nnamespace myImages {\n\n    helpers._registerFactory(\"image\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"image1\":\n            case \"myImage\":return img`\n. . . . . . f f f f f . . . . . \n. . . . . f f f f f f f . . . . \n. . f . f f f f f f f f f . . . \n. . . f f b f f f f f b f . . . \n. . f . f d 1 1 b 1 1 d f . . . \n. . . . f f 1 f d f 1 f f . . . \n. . . . . f f f f f f f . . . . \n. . . . . . f f f f f . . . . . \n. . . . . f f f f f f f . . . . \n. . . . f f f f f f f f f . . . \n. . . . f f f f f f f f f . . . \n. . . f . f f f f f f f . f . . \n. . . f . f f f f f f f . f . . \n. . . . . . f f f f f . . . . . \n. . . . . . f f . f f . . . . . \n. . . . . f f f . f f f . . . . \n`;\n            case \"image3\":\n            case \"myImage1\":return img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . f f . . . . . . . . . \n. . . . . . f f . . . . . . . . \n. . . . . . f b f . . . . . . . \n. . . . . . f c f . . . f . . . \n. . . . f f c a c f f f f . . . \n. . . f b c a 3 a c b f . . . . \n. . f f f f c a c f f . . . . . \n. . f . . . f c f . . . . . . . \n. . . . . . f b f . . . . . . . \n. . . . . . . f f . . . . . . . \n. . . . . . . . f f . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`;\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"animation\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"song\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n", 

  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><variables><variable id=\"`:Vg]@wd^~pi/1fGUHw4\">mySprite</variable><variable id=\"QG(CAAdKF[v;,/Xw*a0[\">mySprite2</variable><variable type=\"KIND_SpriteKind\" id=\"hX,;PFQjdZ?o]d#t|ElQ\">Player</variable><variable type=\"KIND_SpriteKind\" id=\".wUWs(QqK:l%fbd:AMw:\">Projectile</variable><variable type=\"KIND_SpriteKind\" id=\"ek[)C?O?wa}hfjZ9={qy\">Food</variable><variable type=\"KIND_SpriteKind\" id=\"5Pg%{$fo9Y^-J!53ixHG\">Enemy</variable><variable type=\"KIND_SpriteKind\" id=\"IXLi|R1g52p0Oc5XM!Lk\">Object</variable></variables><block type=\"pxt-on-start\" x=\"0\" y=\"0\"><statement name=\"HANDLER\"><block type=\"gameSplash\"><mutation xmlns=\"http://www.w3.org/1999/xhtml\" _expanded=\"0\" _input_init=\"true\"></mutation><value name=\"title\"><shadow type=\"text\"><field name=\"TEXT\">Catch as many ninja stars as you can in 10 seconds!</field></shadow></value><value name=\"subtitle\"><shadow type=\"text\"><field name=\"TEXT\"></field></shadow></value><next><block type=\"gamesetbackgroundcolor\"><value name=\"color\"><shadow type=\"colorindexpicker\"><field name=\"index\">4</field></shadow></value><next><block type=\"variables_set\"><field name=\"VAR\" id=\"`:Vg]@wd^~pi/1fGUHw4\">mySprite</field><value name=\"VALUE\"><shadow xmlns=\"http://www.w3.org/1999/xhtml\" type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreate\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">assets.image`myImage`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"myImages.image1\"}}</data></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Player</field></shadow></value></block></value><next><block type=\"game_control_sprite\"><mutation xmlns=\"http://www.w3.org/1999/xhtml\" _expanded=\"0\" _input_init=\"true\"></mutation><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"`:Vg]@wd^~pi/1fGUHw4\">mySprite</field></block></value><value name=\"vx\"><shadow type=\"spriteSpeedPicker\"><field name=\"speed\">100</field></shadow></value><value name=\"vy\"><shadow type=\"spriteSpeedPicker\"><field name=\"speed\">100</field></shadow></value><next><block type=\"spritesetsetstayinscreen\"><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"`:Vg]@wd^~pi/1fGUHw4\">mySprite</field></block></value><value name=\"on\"><shadow type=\"toggleOnOff\"><field name=\"on\">true</field></shadow></value></block></next></block></next></block></next></block></next></block></statement></block><block type=\"hudsetScore\" disabled=\"true\" x=\"1060\" y=\"40\"><value name=\"value\"><shadow type=\"math_number\" disabled=\"true\"><field name=\"NUM\">0</field></shadow></value><next><block type=\"gamecountdown\" disabled=\"true\"><value name=\"duration\"><shadow type=\"math_number\" disabled=\"true\"><field name=\"NUM\">10</field></shadow></value></block></next></block><block type=\"hudChangeScoreBy\" disabled=\"true\" x=\"1360\" y=\"60\"><value name=\"value\"><shadow type=\"math_number\" disabled=\"true\"><field name=\"NUM\">1</field></shadow></value></block><block type=\"spritesoverlap\" x=\"1060\" y=\"240\"><value name=\"HANDLER_DRAG_PARAM_sprite\"><shadow type=\"argument_reporter_custom\"><mutation typename=\"Sprite\"></mutation><field name=\"VALUE\">sprite</field></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Player</field></shadow></value><value name=\"HANDLER_DRAG_PARAM_otherSprite\"><shadow type=\"argument_reporter_custom\"><mutation typename=\"Sprite\"></mutation><field name=\"VALUE\">otherSprite</field></shadow></value><value name=\"otherKind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Food</field></shadow></value><statement name=\"HANDLER\"><block type=\"spritedestroy2\"><mutation xmlns=\"http://www.w3.org/1999/xhtml\" _expanded=\"0\" _input_init=\"true\"></mutation><field name=\"effect\">effects.spray</field><value name=\"sprite\"><block type=\"argument_reporter_custom\"><mutation typename=\"Sprite\"></mutation><field name=\"VALUE\">otherSprite</field></block></value><value name=\"duration\"><shadow type=\"timePicker\"><field name=\"ms\">500</field></shadow></value></block></statement></block><block type=\"variables_get\" disabled=\"true\" x=\"1200\" y=\"348\"><field name=\"VAR\" id=\"`:Vg]@wd^~pi/1fGUHw4\">mySprite</field></block><block type=\"gameinterval\" x=\"20\" y=\"480\"><value name=\"period\"><shadow type=\"timePicker\"><field name=\"ms\">1000</field></shadow></value><statement name=\"HANDLER\"><block type=\"variables_set\"><field name=\"VAR\" id=\"QG(CAAdKF[v;,/Xw*a0[\">mySprite2</field><value name=\"VALUE\"><shadow xmlns=\"http://www.w3.org/1999/xhtml\" type=\"math_number\"><field name=\"NUM\">0</field></shadow><block type=\"spritescreate\"><value name=\"img\"><shadow type=\"screen_image_picker\"><field name=\"img\">assets.image`myImage1`</field><data>{\"commentRefs\":[],\"fieldData\":{\"img\":\"myImages.image3\"}}</data></shadow></value><value name=\"kind\"><shadow type=\"spritekind\"><field name=\"MEMBER\">Food</field></shadow></value></block></value><next><block type=\"spritesetpos\"><value name=\"sprite\"><block type=\"variables_get\"><field name=\"VAR\" id=\"QG(CAAdKF[v;,/Xw*a0[\">mySprite2</field></block></value><value name=\"x\"><shadow type=\"positionPicker\"><field name=\"index\">0</field></shadow><block type=\"device_random\"><value name=\"min\"><shadow type=\"math_number\"><field name=\"NUM\">0</field></shadow></value><value name=\"limit\"><shadow type=\"math_number\"><field name=\"NUM\">160</field></shadow></value></block></value><value name=\"y\"><shadow type=\"positionPicker\"><field name=\"index\">0</field></shadow><block type=\"device_random\"><value name=\"min\"><shadow type=\"math_number\"><field name=\"NUM\">0</field></shadow></value><value name=\"limit\"><shadow type=\"math_number\"><field name=\"NUM\">120</field></shadow></value></block></value></block></next></block></statement></block><block type=\"gamecountdownevent\" x=\"1100\" y=\"500\"><statement name=\"HANDLER\"><block type=\"gameOver2\"><value name=\"win\"><shadow type=\"toggleWinLose\"><field name=\"win\">true</field></shadow></value></block></statement></block></xml>", 

  "main.ts": "namespace SpriteKind {\n    export const Object = SpriteKind.create()\n}\ninfo.onCountdownEnd(function () {\n    game.gameOver(true)\n})\nsprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {\n    sprites.destroy(otherSprite)\n})\nlet mySprite2: Sprite = null\ngame.splash(\"Catch as many ninja stars as you can in 10 seconds!\")\nscene.setBackgroundColor(4)\nlet mySprite = sprites.create(assets.image`myImage`, SpriteKind.Player)\ncontroller.moveSprite(mySprite)\nmySprite.setStayInScreen(true)\ngame.onUpdateInterval(1000, function () {\n    mySprite2 = sprites.create(assets.image`myImage1`, SpriteKind.Food)\n    mySprite2.setPosition(randint(0, 160), randint(0, 120))\n})\n", 

  "pxt.json": "{\n    \"name\": \"Catch the Ninja Stars(shortened version of save the computers)\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"images.g.jres\",\n        \"images.g.ts\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.12.29\",\n        \"tag\": \"v1.12.29\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/e3682278e015a20ba1c143cb55ded707029d8938\",\n        \"target\": \"1.12.29\",\n        \"pxt\": \"8.5.40\"\n    },\n    \"preferredEditor\": \"blocksprj\"\n}\n" 
} 

``` 

## Code Ninjas Game Building Session @showdialog 

**Catch the Ninja Stars!** 

--- 

Welcome to Code Ninjas!  Follow along with a Code Sensei to code a project! 

![Example](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/Catch-ninja-stars-ExProj.gif?raw=true "Project Example") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

 

## ✋ Welcome 

--- 

**Answer:** 

❓ *Have you ever coded before?* 

❓ *Have you ever used MakeCode Aracde?* 

--- 

**MakeCode Overview:** 

Your ``||text:Code Sensei||`` will now explain MakeCode Aracde's interface! 

![Ninja](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/NinjaDisplaying.png?raw=true "Explain Interface") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Set the Background Color  

*Pick a color for your project's background!*  

- :tree: In the Toolbox, click to open ![Scene](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/Scene.png?raw=true "Click Scene")   

- :tree: Drag the ``||scene:set background color||`` block into the ``||loops:on start||`` container in the workspace.  

- :mouse pointer: Click the gray bubble and select a color. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## The Game Window 

As you add code to your project, look at the Game Window on the **right** of your screen to see it update! 

![Game Window](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/GameWindow.png?raw=true "Game Window") 

``||text: Code Sensei:||`` *Do you see your background color in the game window?* 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Create a Sprite 

--- 

🙋 A **sprite** is an object in a program. 

--- 

 

- :paper plane: Open ``||sprites:Sprites||`` and drag ``||variables:set sprite to||`` into *the end* of the ``||loops:on start||`` container.  

- :mouse pointer: Click the gray box and select the ``||sprites:My Assets||`` tab at the top.  

 

![Gallery](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/MyAssets.png?raw=true "Gallery Tab") 

- :mouse pointer: Select the 🥷**ninja**🥷 image. Click ``||loops:Done||`` in the bottom right. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Make the Sprite Move 

*Code the sprite to move with the arrow keys!*  

- :game: Open ``||contoller:Controller||`` and drag ``||controller:move sprite with buttons||`` into *the end* of ``||loops:on start||``.  

- :paper plane:  **Make sure the sprite doesn't move off screen!** Open ``||sprites:Sprites||`` and drag ``||sprites:set sprite stay in screen||`` to *the end* of your code.  

--- 

``||text: Code Sensei:||`` *What happens if it's toggled OFF?* Before clicking Next, set it back to **ON**! 


![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 


## Add a Sprite to Collect 

*Your sprite is looking for ninja stars!*  


- :paper plane: Open ``||sprites:Sprites||`` and drag ``||variables:set sprite to||`` to *the end* of your code. 

- :mouse pointer: Click the gray box and select the ``||sprites:My Assets||`` tab at the top. Select the **ninja star** and click ``||loops:Done||``. 

![Ninja Star](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/ninjaStar.png?raw=true "Ninja Star")  

- :mouse pointer: On the ``||sprites:set sprite||`` block, click ``||sprites:Player||`` and select **Food** from the drop-down menu. 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

## Set Position 

*Code where the ninja star appears.* 

- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:set sprite position||`` to *the end* of your code. 

- :mouse pointer: Click ``||variables:mySprite||`` and select **mySprite2** from the drop-down. 

**Make it appear at a random location.** 

- :calculator: Open ``||math:Math||`` and drag ``||math:pick random||`` into  

``||sprites:sprite position||``'s **x** bubble.    

- :mouse pointer: Set it to pick from `0` to `160`! 

- :calculator: Open ``||math:Math||`` and drag ``||math:pick random||`` into the **y** bubble. 

- :mouse pointer: Set it to pick from `0` to `120`! 

--- 

``||text: Code Sensei:||`` *What does the x position set?  The y?* 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

 

## Create Many Collectibles 

--- 

🙋 **Collectibles** are objects to pick up. *The ninja stars are collectibles!* 

--- 
 

*Make more ninja stars appear.* 

- :circle: Open ``||game:Game||`` and drag ``||game:on game update every||`` onto an empty spot in the coding workspace. 

- :mouse pointer: Drag the two ``||variables:mySprite2||`` code blocks from ``||loops:on start||`` into the ``||game:game update||`` container: 

![Example](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/mySprite2-onUpdate.gif?raw=true "Drag into game update container.") 

--- 

``||text: Code Sensei:||`` *Change the number in* ``||game:on game update every||`` *to see what happens.* 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 


## Pickup Collectibles 

*Make the ninja star disappear when the ninja touches it.* 

- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:on sprite of kind overlaps||`` onto an empty spot on the coding workspace. 

- :mouse pointer: Click the second dropdown ``||sprites:⏷||`` and set it to **Food**.   

- :paper plane: Open ``||sprites:Sprites||`` and drag ``||sprites:destroy sprite||`` into the ``||sprites:on overlap||`` container. 

- :mouse pointer: From the ``||sprites:overlap||`` block, click and drag the ``||variables:otherSprite||`` bubble into the ``||sprites:destroy||`` block's ``||variables:mySprite||`` bubble.   

![Other Sprite](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/otherSprite-destroy.gif?raw=true "Drag othersprite into destroy.") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo")  

## Playtest 

Playtest your game to catch ninja stars! 

![Game Window](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/GameWindow.png?raw=true "Game Window") 

Make any tweaks to **parameters**! 

--- 

🙋 **Parameters** are information you can change to set how a program runs. *Background color is an example of a parameter!* 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

 
## BONUS 

`||arrays:BONUS:||` *Have extra time to learn more?*  **Add a timer and score!** 

**Add score.** 

- :id card: Open ``||info:Info||`` and drag ``||info:set score||`` into the ``||loops:on start||`` container.  *Leave set score at 0.* 

- :id card: Open ``||info:Info||`` and drag ``||info:change score by||`` into *the end* of the ``||sprites:sprite on overlap||`` container.   

--- 

``||text: Code Sensei:||`` *What happens if you change the number in* ``||info:change score||``*?* 

--- 

**Add a timer.** 

- :id card: Open ``||info:Info||`` and drag ``||info:start countdown||`` into the ``||loops:on start||`` container. *Change the timer from 10 to increase or decrease how long the game is!* 

Playtest your changes in the **Game Window**! 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 

##  

🎊 **Congratulations!** 🎊 

Thanks for being a ninja with us today!  We hope to see you soon! 

You rocked!! 

--- 

![Yay](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/YayNinja.png?raw=true "You rock!") 

![Logo](https://github.com/Code-Ninjas-Home-Office/game-building-session-tutorials/blob/master/images/CN-Logo.png?raw=true "CN Logo") 
