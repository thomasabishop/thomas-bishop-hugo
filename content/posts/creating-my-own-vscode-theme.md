---
date: 2022-01-01
title: "Creating my own VS Code theme"
categories: ["Projects"]
tags: ["text-editors"]
toc:
  enable: false
---

One of my favourite procrastination techniques is to endlesslly toggle through colour themes within Visual Studio Code, combining them with different fonts and icons to approximate some Platonic ideal of the optimal working environment. However I am never satisfied. There is always some technical or aesthetic aspect that displeases me.

![Alt text](/alien_blood_terminal_colours.png "Alien Blood terminal colours")

Over the last month or so I decided to resolve the issue once and for all by creating my own custom theme. I have always really enjoyed the Alien Blood colours that are one of the default themes of the iTerm 2 terminal emulator for Mac. I decided I would use this as my base and try to construct a fully-fledged syntax and UI scheme from the terminal pallette. This wasn't easy because in general the colour palettes of terminal themes are more austere than those designed for syntax-highlighting. In addition the colors used are typically more contrasting than you would expect or want when highlighting syntax. As a result it took lots of tweaking to try and make the resulting theme visually harmonious (avoiding jarring contrasts that break the visual flow when reading code) but not so homogenous that one cannot at a glance distinguish different syntactic entities.

![Alt text](/alien_blood_syntax_demo.png "Alien Blood VS Code theme showing TypeScript highlighting")

I was able to achieve this without introducing any additional colours to the default Alien Blood palette. The theme can be demoed in the browser [here](https://vscode.dev/theme/ThomasBishop.alien-blood/Alien%20Blood%20) and downloaded from the [extension marketplace](https://marketplace.visualstudio.com/items?itemName=ThomasBishop.alien-blood). You can also view the theme on [GitHub](https://github.com/thomasabishop/alien-blood-vscode).

I'm particularly happy with the rendering of TypeScript and Angular components which is what I am editing the majority of the time at work, similarly with HTML and CSS. However I think there is room for improvement when it comes to plain JavaScript and other filetypes such as shell scripts. In these cases the highlighting is too homogenous and dark but now I have the basic palette completed I can add additional rules for specific programming languages in future releases. I also plan to create an equivalent theme for Vim/Neovim. I tend to use VS Code most of the time but it would be nice to have consistency when I jump into Vim for small edits from the terminal.
