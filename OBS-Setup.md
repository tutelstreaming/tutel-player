Download and Install OBS (Open Broadcaster Software)
https://obsproject.com/

If you follow this guide, you'll be setup in no time and have the best settings for a low-latency stream.

---------------
OBS Setup (all other options not shown in this tutorial can be left to defaults)
1) Files -> Settings -> Stream
- Set "Service" to Custom
- Set "Server" to the URL of your OvenMediaEngine (can also be an IP address)
- For example: "rtmp://example.com/app" or "rtmp://192.168.0.200/app"
- Set "Stream Key" to whatever you have listed in Google Sheets
- For example: "testuser1"

<img src="https://user-images.githubusercontent.com/124169586/216693786-7512b145-dfcc-49b0-a295-33ab098f8fa3.png" width="40%">

2) Files -> Settings -> Video
- Set "Base (Canvas) Resolution" to your Monitor's Native Resolution
- For example: 1920x1080, 2560x1440, 3440x1440, 3840x2160, etc
- Set "Output (Scaled) Resolution" to match the "Base (Canvas) Resolution"
- Downscale Filter should be grayed out if the above two settings match
- The reason why you want these to match is because this is a recording feature and makes your stream look pixaleted at times.
- Set "Common FPS Values" to either 30 (recommended) or 60
- While 60 FPS provides a smoother experience, it can make the overall stream look more pixelated.

<img src="https://user-images.githubusercontent.com/124169586/216694799-270182ed-d014-4879-a275-14f9f2d051ee.png" width="40%">

3) Files -> Settings -> Output
- Writing out an explanation for all these settings for three different types of hardware can get wordy.  Please reference the pictures for your hardware specific settings. (AMD/NVIDIA, or CPU-based Encoding)
- Please note that only H264 streaming is supported by OvenMediaEngine.  HEVC/H265 or AV1 will not work.
- Also note that KeyFrames needs to be 1s (second) and B-Frames must be set to 0.

- For different resolutions, use the "Rescale Output" option to lower or increase the resolution of your stream.

----------

NVIDIA Hardware Encoding

<img src="https://user-images.githubusercontent.com/58894818/218870903-6bbe604f-6086-4652-892d-8042eab3a825.png" width="40%">

----------

AMD Hardware Encoding

<img src="https://user-images.githubusercontent.com/124169586/216698718-35b90165-1992-4583-86be-4be3427bb0fc.png" width="40%">

----------

CPU-Based Software Encoding

<img src="https://user-images.githubusercontent.com/58894818/218871007-fe913024-cd12-4c3f-8a49-087fe9afef2a.png" width="40%">

----------


Setting Up A Scene

On the bottom left of the main OBS window, Scene 1 should be created by default.  To the right of that window is "Sources".  Click on the "+" sign to add a Source.
Either Select "Game Capture" or "Display Capture" if you wish to stream your entire Monitor Display.

<img src="https://user-images.githubusercontent.com/58894818/218323631-98773625-269f-45da-adcc-2a0a4e265ede.png" width="40%">

By default the Mode is set to "Capture any fullscreen application".  However, if you want it to specifically stream Escape From Tarkov for example, the game needs to be running in order for the selection to be available.

<img src="https://user-images.githubusercontent.com/58894818/218323682-e02fee67-e36c-4140-b8eb-2301220cae0d.png" width="40%">

What the end result should look like.  I have multiple Scenes in this example that when I click on them, it changes what is streamed.  This is useful if you want to have a Scene for Full Desktop Streaming and another for just Full Screen Applications.

<img src="https://user-images.githubusercontent.com/58894818/218323722-c6ffd0e1-b05d-4e88-a6b1-e4cfbbce06e9.png" width="40%">


And that is it! You are now good to click on "Start Streaming" on the bottom right of OBS.
