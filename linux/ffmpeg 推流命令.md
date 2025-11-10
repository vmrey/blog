#### linux 推流命令
```sh
ffmpeg -re -i "视频源地址" -c:v copy -c:a aac -b:a 192k -strict -2 -f flv "rtmp://a.rtmp.youtube.com/live2/直播码"
```
