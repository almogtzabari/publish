---
Aliases:
- How to trim a video using FFmpeg (for dummies)
- Back to How to trim a video using FFmpeg (for dummies)
---

# How to trim a video using FFmpeg (for dummies)
**Navigation**
[[ffmpeg|Back to FFmpeg]]

---

In order to split a video file using [[FFmpeg]] follow these steps:
1. [[how_to_set_up_ffmpeg_on_windows_for_dummies|Set up FFmpeg on your Windows machine]] and open the terminal.
2. Copy the file you want to trim to the `bin` folder (explained [[how_to_set_up_ffmpeg_on_windows_for_dummies|here]] in step 2).
3. In the terminal, type `ffmpeg -i source.mp4 -ss 0 -t 70 -c copy part1.mp4`. 

Let's break down the command from step 3:
- `source.mp4` is your file name. For example: `my_video.mkv`.
- `-ss 0` means start from second number `0`.
- `-t 70` means end at second number `70` (=1 minute and 10 seconds).
- If you wish to cut your video at `28:40` use the formula $28\cdot 60+40=1,720$.
- `-c copy` means to copy all input streams - all parameters related to audio, video (resolution for example), subtitles, etc.
- `part1.mp4` is the name of the output file (what name to give to the trimmed video file).


