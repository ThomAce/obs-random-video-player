# obs-random-video-player
## About
Play random videos from specific folder in OBS.

The solution gives you an easy-to-implement way to create continuous, randomly played videos in OBS studio. You don't need specific tools.

### Issue

In OBS, there is no proper inbuilt function to continuously play random videos with fade effect between each videos. You can use either one single video or add multiple elements manually or using VLC player to reach these goals. However, these are not straight-forward solutions, yet complicated. And most of the cases not even give the expected results... Also found problem that I had to put extra care on video files with audio because it could cause unwanted effect as well. The another problematic point I faced with the above solutions is that if a video could not be played (for whatever reason), the video could stuck and had to initiate manual actiton to fix it while live stream is on.

### Solution

Built a simple HTML page (HTML + CSS + JavaScript) which is compatible with OBS and can play video files in random order with short fade (by changing opacity of the top layer back and forth) between each videos. The HTML can be added to OBS studio and can be used as a continuous video element during your record or live stream, or simply using it as your "Be Right Back" screen.

### What this solution gives you?

- Minimum required administrative effort to implement
- Easy integration with OBS
- No executables needs to be downloaded
- No ads
- Only MP4 files can be played at the moment
- Fade between video elements
- Automatic continuous play in case of a file can not be played
- All video muted
- No special permission needed
- Completely free :)

## Requirements

- No special requirements needed

## How to setup

- Download the latest obs-random-video-player.html
- Copy / save it to a folder where your movie files are placed
- Execute the following command depends on your system type:
- 
  Windows:
  - open a command prompt
  - navigate to your video folder
  - execute command: dir *.mp4 /b > videos.txt
- 
  Linux:
  - open console
  - navigate to your video folder
  - execute command: ls -a *.mp4 > videos.txt   
- Open OBS
- Choose your desired scene and add new Browser element (name it as you wanted...) 
- Select "Local file", then browse the HTML file
- Type with and height according to your needs
- Engage Shutdown source when not visible to save some resources
- Engage Refresh browser scene becomes active
- Click OK and you are done!

  
![kép](https://github.com/ThomAce/obs-random-video-player/assets/34764511/4e4f5688-6f02-4fc4-84b5-d242ca2e4b5f) ![kép](https://github.com/ThomAce/obs-random-video-player/assets/34764511/f2175db9-5f65-46d3-9704-c98e62750485)


![kép](https://github.com/ThomAce/obs-random-video-player/assets/34764511/2febfd28-7ae6-4ff0-94d0-bb4d628b0317)
![kép](https://github.com/ThomAce/obs-random-video-player/assets/34764511/83581be8-9017-4caf-ae37-665622750dd8)


## Known issues, limitations:

- Certain cases some videos might stutter (some frame drops) during fading between two videos. - Check your video driver and capabilities of your system and video files. Recompressing the videos for matching the stream requirements helps a lot.
- Only MP4 can be played
- Only FADE transition is available at the moment
- Only random play order is available at the moment
- If you open the HTML with your browser, it might not work. Take it easy: In OBS it will work. :)
