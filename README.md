*Modification of original plugin by [AleDel](https://github.com/AleDel/Spout-UE4) with UE versions 4.19+.*

**This was tested with:**
* 4.19
* 4.20
* 4.21

# Spout-UE4
This is a [Spout](http://spout.zeal.co/) Plugin for Unreal Engine. It allows you to send and receive textures using Spout framework.

Sender and Receiver only DirectX 11.

# Installation and Use

Put code in _Plugins_ folder (for example "_yourproject/Plugins/SpoutUE4_"). For detailed instructions please refer to [Lightact support page](https://support.lightact-systems.com). There's plenty of User Guides and Video Tutorials on integrating this plugin with your UE4 project.

# Info

the **Spout sender** node has two options: 
  * **Game Viewport** sends the image of the viewport, but please note that it doesn't work in standalone or packaged game.
  * **TextureRenderTarget2D** in which case you should create a _SceneCaptureComponent2D_ and a *Render target 2D* which you should reference in the node.

use **Close Sender** node to close spouts

![CaptureSpout2](http://aledel.github.io/Spout-UE4/images/10senders.jpg)
A test of sending 10 sender to Touchdesigner 1024x768 either one, the performance is good.

# Install Example

* Create new C++ *First Person* project
* unzip ExampleSpout.zip in the "Content" folder of your project
* unzip code plugin in folder "Plugins" as mentioned above, if there is no "Plugins" folder, create it
* restart project
* load Spout scene
* if you encounter compile errors you have to delete and re-insert identical nodes

[ExampleSpout.zip](http://aledel.github.io/Spout-UE4/exampleSpoutUE4/ExampleSpout.zip)

![CaptureSpout2](http://aledel.github.io/Spout-UE4/images/spout2.jpg)
This image corresponds to the "Spout" scene. 

# Packaged game
To make this plugin work in a packaged game you have to disable using 'pak' files. You do that by:
1. going to File->Package project->Packaging settings
2. once there uncheck 'Use Pak File' checkbox

# Issues
If you get missing Spout.dll error when trying to launch the game manually copy Spout.dll from:
[gameName]\Plugins\SpoutUE4\ThirdParty\Spout\lib\amd64

to: 
[gameName]\Binaries\Win64

**If someone knows how to fix this, please let me know!**

