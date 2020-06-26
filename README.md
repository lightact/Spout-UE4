*Modification of original plugin by [AleDel](https://github.com/AleDel/Spout-UE4) with UE versions 4.19+.*

**This was tested with:**
* 4.19
* 4.20
* 4.21
* 4.22
* 4.23 
* 4.24
* 4.25

# Spout-UE4
This is a [Spout](http://spout.zeal.co/) Plugin for Unreal Engine. It allows you to send and receive textures using Spout framework.

# Installation and Use

Clone the repository in your Plugin folder.

If you don't know what 'clone' means, then just download the whole repository, unzip it and put the code in _Plugins_ folder (for example "_yourproject/Plugins/Spout-UE4_"). For detailed instructions please refer to [Unreal Engine 4 and Lightact Video Tutorials](https://www.youtube.com/playlist?list=PLcNPGta1d2XDcSsz8zcW0f2lPSawnW3mR). This video is a good step-by-step walkthrough of how to set up your project for use with the plugin.

## Sending Spout

This is done with the **Spout sender** node which has can send texture either from the Game viewport or from a Render Targert 2D: 
  * **Game Viewport** sends the image of the viewport, but please note that it doesn't work in standalone or packaged game.
  * **TextureRenderTarget2D** in which case you should create a _SceneCaptureComponent2D_ and a *Render target 2D* which you should reference in the node.

Use **Close Sender** node to close Spouts. The best way is to connect it to **Event EndPlay** node.

## Working sample

On Lightact website you can download [Lightact & Unreal Engine Sample Project](https://lightact-systems.com/product/lightact-and-unreal-engine/). It has both this and [Lightact plugin](https://github.com/lightact/Lightact-UE4)   enabled.

## Packaged game
To make this plugin work in a packaged game you have to disable using 'pak' files. You do that by:
1. going to File->Package project->Packaging settings
2. once there uncheck 'Use Pak File' checkbox

This is only necessary if you are using the *Mat* pin on the *Spout Receiver* node.

## Troubleshooting
If you are a Lightact user, please refer to [Lightact Answerhub](https://answerhub.lightact-systems.com/).
