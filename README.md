# mumbleradio
Simple [mumble](https://mumble.info):// music bot.

## Installation

Dependencies: python3.7+.

```
git clone https://github.com/kousu/mumbleradio/
cd mumbleradio
pip install -r requirements.txt
```

## Example

Play a song off YouTube to mumble://mumble.snopyta.org.

```{bash}
./mumbleradio mumble.snopyta.org \
  <(ffmpeg -loglevel quiet \
           -i "$(youtube-dl -g https://www.youtube.com/watch?v=9mWLig0s_9k)" \
           -f wav -acodec pcm_s16le -ac 1 -ar 48000 -)
```
