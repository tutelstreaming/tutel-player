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

<img src="https://user-images.githubusercontent.com/124169586/216693786-7512b145-dfcc-49b0-a295-33ab098f8fa3.png" width="35%">

2) Files -> Settings -> Video
- Set "Base (Canvas) Resolution" to your Monitor's Native Resolution
- For example: 1920x1080, 2560x1440, 3440x1440, 3840x2160, etc
- Set "Output (Scaled) Resolution" to match the "Base (Canvas) Resolution"
- Downscale Filter should be grayed out if the above two settings match
- The reason why you want these to match is because this is a recording feature and makes your stream look pixaleted at times.
- Set "Common FPS Values" to either 30 (recommended) or 60
- While 60 FPS provides a smoother experience, it can make the overall stream look more pixelated.

![video_settings](https://user-images.githubusercontent.com/124169586/216694799-270182ed-d014-4879-a275-14f9f2d051ee.png)

3) Files -> Settings -> Output
- Writing out an explanation for all these settings for three different types of hardware can get wordy.  Please reference the pictures for your hardware specific settings. (AMD/NVIDIA, or CPU-based Encoding)
- Please note that only H264 streaming is supported by OvenMediaEngine.  HEVC/H265 or AV1 will not work.
- Also note that KeyFrames needs to be 1s (second) and B-Frames must be set to 0.

- For different resolutions, use the "Rescale Output" option to lower or increase the resolution of your stream.

----------

NVIDIA Hardware Encoding

![image](https://user-images.githubusercontent.com/124169586/216698618-4fd81b74-545e-4258-8b3f-c5a4b948d57b.png | width=100)
<img src="[https://camo.githubusercontent.com/...](https://user-images.githubusercontent.com/124169586/216698618-4fd81b74-545e-4258-8b3f-c5a4b948d57b.png)" width="100"/>

----------

AMD Hardware Encoding

![output_settings_amd](https://user-images.githubusercontent.com/124169586/216698718-35b90165-1992-4583-86be-4be3427bb0fc.png)

----------

CPU-Based Software Encoding

![output_settings_h264](https://user-images.githubusercontent.com/124169586/216699557-bed07be8-f96a-4a3d-aa57-7809ca0e9aac.png)

----------
