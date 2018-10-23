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
