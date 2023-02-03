Download and Install OBS (Open Broadcaster Software)
https://obsproject.com/

---------------
OBS Setup (all other options not shown in this tutorial can be left to defaults)
1) Files -> Settings -> Stream
- Set "Service" to Custom
- Set "Server" to the URL of your OvenMediaEngine (can also be an IP address)
- For example: "rtmp://example.com/app" or "rtmp://192.168.0.200/app"
- Set "Stream Key" to whatever you have listed in Google Sheets
- For example: "testuser1"

![stream_settings](https://user-images.githubusercontent.com/124169586/216693786-7512b145-dfcc-49b0-a295-33ab098f8fa3.png)

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
- 
