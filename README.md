# FFMPEG
Video, audio, image, and subtitles editing examples.

## Convert Video to NSTC DVD Format.
```console
ffmpeg -i (nameOfVideo.mp4) -target ntsc-svcd (nameOfVideo).mpg
```
## Merge 2 Videos
```console
ffmpeg -i (nameOfVideo1.mp4) -i (nameOfVideo2.mp4) -filter_complex "[0:v] [0:a] [1:v] [1:a] concat=n=2:v=1:a=1 [v] [a]" -map "[v]" -map "[a]" (nameOfMergedVideo.mp4)
```
## Trim/Extract Audio from Video
```console
ffmpeg -ss 0 -t 7 -i (nameOfAudio.mp3) (nameOfTrimAudio.mp3)
```

| Code                | Meaning              |
| ------------------- |:--------------------:|
| -ss 0               | Start at 0 seconds   |
| -t 7                | Stop after 7 seconds |
| nameOfAudio.mp3     | Input File           |
| nameOfTrimAudio.mp3 | Output file          |
