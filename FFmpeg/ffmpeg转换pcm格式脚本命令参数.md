```
#!/bin/bash
for i in *; do
    echo "$i"
    ffmpeg -i "$i" -acodec pcm_s16le -ac 1 -ar 8000 "${i%.*}.wav"
    # -i "$i" 输入文件
    # -acodec pcm_s16be  大段数据格式
    # -acodec pcm_s16le  小端数据格
    # -ac 1 单声道
    # -ar 8000 采样率 8k
done
```
