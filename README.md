*Modification of original plugin by [AleDel](https://github.com/AleDel/Spout-UE4) in order to make it work with 4.19 and 4.20. This was tested and it works, but please check Issues below*
# Spout-UE4
[Spout](http://spout.zeal.co/) Plugin for Unreal Engine

Sender and Receiver only DirectX 11.

# Installation and Use

Put code in folder Plugins (for example "yourproject/Plugins/SpoutUE4"). For detailed instructions please refer to [Lightact support page](https://support.lightact-systems.com)

# Info

the "spout sender" has two options: 
  * "Game Viewport" that send the image of the viewport (doesn't work in standalone game) 
  * or use a "TextureRenderTarget2D" in this case you should create a "SceneCaptureComponent2D"

use "spout close" blueprint to close spouts

![CaptureSpout2](http://aledel.github.io/Spout-UE4/images/10senders.jpg)
test sending 10 sender to Touchdesigner 1024x768 either one, the performance is good.

# Install Example

* Create new c++ First Person project
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

