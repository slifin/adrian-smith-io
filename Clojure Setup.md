[TOC]

## Clojure Install

The easiest way to install Clojure is to visit: https://clojure.org/guides/getting_started

<img src="https://i.imgur.com/xXVJP8E.png" style="zoom:50%;" />



Follow the instructions for your operation system

<img src="https://i.imgur.com/BJYDuQ3.png" style="zoom:50%">

## Editor

Download Intellji from: https://www.jetbrains.com/idea/download/

<img src="https://i.imgur.com/ARt8QHE.png" style="zoom:50%" />

The Community version is free and suitable for Clojure development

<img src="https://i.imgur.com/WgnX7xj.png" style="zoom:50%" />





## Editor Plugin

When your editor loads you should see a welcome screen something like below

<img src="https://i.imgur.com/FNcKHgV.jpg" style="zoom:50%" />



In order to do Clojure development we need a editor plugin called Cursive https://cursive-ide.com/

To install it press the ⚙️ Configure drop down and click Plugins

<img src="https://i.imgur.com/WYuqsOa.png" style="zoom:50%"/>

Select Marketplace and type "cursive" into the search field, then press the install button

<img src="https://i.imgur.com/oh4GwiU.png" style="zoom:50%" />

Restart Intellji 

## Creating a project

Press "Create New Project" on the welcome screen we saw earlier then select Clojure from the left hand side and then "Deps" then press ok

<img src="https://i.imgur.com/doQzjFC.png" style="zoom:50%" />

Choose a project name

<img src="https://i.imgur.com/swGeeMs.png" style="zoom:50%"/>

Welcome to your new project

<img src="https://i.imgur.com/MBRuVt9.png" style="zoom:50%" />



## Enable parinfer

Open the preferences for Intellji

<img src="https://i.imgur.com/HBz5AFA.png" style="zoom:50%" />

Navigate through Editor > General > Smart Keys > Clojure

and change the "Structural editing style" to Parinfer Indent mode



<img src="https://i.imgur.com/rreEHck.png" style="zoom:50%" />

Clojure parentheses will now balance according to their indentation level in the code

## Hello world

Right click your project and hover over the new menu and select "Clojure Namespace"

<img src="https://i.imgur.com/UETqVzI.png" style="zoom:50%" />

In the box that appears type `src/core` that means create a folder called `src` and create a file called `core` inside the default extension for Clojure files are `.clj`

<img src="https://i.imgur.com/JESYzHT.png" style="zoom:50%" />



Open the newly created file

<img src="https://i.imgur.com/aQJk1V6.png" style="zoom:50%" />

and change the code to:

```clojure
(ns core)

(defn hello-world []
  (println "hello world"))
```



## Using the REPL

To create a REPL right click your project within the file explorer

<img src="https://i.imgur.com/TEiLpbo.png" style="zoom:50%" />

Then click "Create 'REPL for ...'"

Right click the project again and press "Run 'REPL for ...'"

<img src="https://i.imgur.com/dYTXB23.png" style="zoom:50%" />

A new window will appear with the REPL inside

<img src="https://i.imgur.com/gkecuzV.png" style="zoom:50%" />



The REPL is an alive instance of Clojure that can be used to get quick feedback on your program

In order to do so we need to learn how to load code into it:

**Load file into the REPL**

Right click anywhere inside a open Clojure file and hover over REPL and select "Load file in REPL"

<img src="https://i.imgur.com/lKZ6gd0.png" style="zoom:50%" />

You should see something like 

<img src="https://i.imgur.com/hC1Tll9.png" style="zoom:50%" />



**Change REPL namespace to our current namespace**

Right click inside the Clojure file hover over REPL and press "Switch REPL NS to Current file"

<img src="https://i.imgur.com/cWoL2Qe.png" style="zoom:50%" />

That should provide output like

<img src="https://i.imgur.com/WoE0Pb4.png" style="zoom:50%" />



There's two ways we can send some code to the REPL, it can either be written directly in, then press enter with your cursor at the end of the line

<img src="https://i.imgur.com/spKM8H3.png" style="zoom:50%" />

or sent from the source code

<img src="https://i.imgur.com/ovpWj88.png" style="zoom:50%" />



The end result should be something like

<img src="https://i.imgur.com/vsjA9Cx.png" style="zoom:50%" />



## Enhanced Static Analysis

Download https://github.com/borkdude/clj-kondo/releases 

`clj-kondo-lsp-server-2019.11.23-standalone.jar` 

<img src="https://i.imgur.com/ONEjylf.png" style="zoom:50%" />

Download https://github.com/gtache/intellij-lsp/releases

at version of at least `1.6.0`

<img src="https://i.imgur.com/m8Ix5X3.png" style="zoom:50%" />

Press shift twice and type "plugins"

<img src="https://i.imgur.com/6inP663.png" style="zoom:50%" />

Press the cog under plugins and click "Install Plugin from Disk..."

<img src="https://i.imgur.com/nxWczJd.png" style="zoom:50%" />

Select the LSP.zip in the file browser

<img src="https://i.imgur.com/gCUE8lU.png" style="zoom:50%" />

Restart Intellji

------

Under preferences

<img src="https://i.imgur.com/gjiiDLa.png" style="zoom:50%" />

Navigate to Languages & Frameworks > Language Server Protocol > Server Definitions

<img src="https://i.imgur.com/izwkR4B.png" style="zoom:50%" />

Change the select box to `Raw command` add the following under Extension `cli;cljs;cljc;edn` and command you will need to add `java -jar <path to lsp jar file>`

<img src="https://i.imgur.com/hHfkFDe.png" style="zoom:50%" />



Type the following expression into a Clojure file 

```clojure
(inc "test")
```

You should see a red squiggly line underneath if everything has been successful

## Installing Leiningen

Navigate to https://leiningen.org/

<img src="https://i.imgur.com/2vNkAiB.png" style="zoom:50%" />

Install it for your operating system

<img src="https://i.imgur.com/BMHvxEP.png" style="zoom:50%" />

Leiningen will allow you to use many templates for Clojure