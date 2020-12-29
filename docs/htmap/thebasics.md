---
id: thebasics
title: The Basics
sidebar_label: The Basics
---
___
Here we will teach you all of the items of code that are required in order for the plugin to work.  

## Namespaces
namespaces is the folders your plugin is located in after ```src/``` folder

for an example the namespace for a class located in ```src/FirstPlugin/PoggitSucks/``` would be ```FirstPlugin\PoggitSucks```

**note** you need to declare the namespace on top of every class like:

```
<?php
//located in src/X/
namespace X;

class A{}
```

## Plugin


first of all we should know that a plugin extends ```pocketmine\plugin\PluginBase``` that can be done by doing the following ```class x extends pocketmine\plugin\PluginBase```

instead of using ```pocketmine\plugin\PluginBase``` you can import that class at the top of your plugin by doing the following ```use pocketmine\plugin\PluginBase```

lets wrap it up in a single code:
```
<?php
//located in /src/FirstPlugin/
namespace FirstPlugin;

//import the PluginBase class
use pocketmine\plugin\PluginBase;
//you can name the class whatever you want for this tutorial we will be using "Main"
//extending PluginBase
class Main extends PluginBase{

}
```
that simple code above is considered as a plugin, but that plugin does nothing



## Plugin default Functions

there is 3 functions that gets called when pocketmine is trying to load/enable/disable the plugin

**onLoad()** this function gets called when pocketmine is trying to loading the plugin

**onEnable()** this function gets called when pocketmine trying to enabling the plugin

**onDisable()** this function gets called when pocketmine is disabling the plugin

## All in one

lets use all the stuff we learned here in a single code:

```
//located in /src/FirstPlugin/
namespace FirstPlugin;

//import the PluginBase class
use pocketmine\plugin\PluginBase;
//you can name the class whatever you want for this tutorial we will be using "Main"
//extending PluginBase
class Main extends PluginBase{
	public function onLoad(){
		//loading the plugin
	}

	public function onEnable(){
		//loading the plugin
	}
	
	public function onDisable(){
		//disabling the plugin
	}
}
