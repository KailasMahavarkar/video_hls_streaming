# Video Chunking using HLS and FFmpeg


## Description

This project is aimed to show case video chunking using HLS (HTTP Live Streaming) and FFmpeg.

## Installation

To install this project, follow these steps:

1. Step 1: Install FFmpeg
2. Step 2: Create an AWS Account and Configure S3 Bucket and CloudFront
3. Step 3: Use hls.js to Stream Video

refer blog post [here](https://medium.com/@kailasmm/how-to-stream-videos-using-hls-6e807f49b189)


## Encoding Video with FFmpeg

To encode a video using FFmpeg, you can use the following command:

```bash
ffmpeg -i input_video.mp4 -codec copy -vbsf h264_mp4toannexb -f segment -segment_list video.m3u8 -segment_time 5 -segment_format mpeg_ts -segment_list_type m3u8 video%04d.ts
```

This command will take the `input_video.mp4` file and encode it into multiple MPEG-TS segments with a duration of 5 seconds each. The segments will be listed in the `video.m3u8` playlist file.

Make sure to replace `input_video.mp4` with the path to your actual video file. You can also adjust the segment duration and format according to your needs.

For more information on FFmpeg and its options, refer to the [official documentation](https://ffmpeg.org/documentation.html).
















