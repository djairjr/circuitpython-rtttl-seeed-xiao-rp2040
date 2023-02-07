# circuitpython-rtttl-seeed-xiao-rp2040
A demo with a big list of RTTTL files to play in A3 Buzzer out of Seeed Xiao Expansion Board
```py
import board
import time
import adafruit_rtttl
fileHandle = open('rtttlsongs.txt')

songs = []
for line in fileHandle:
    songs.append(line)

fileHandle.close()

for song in songs:
    adafruit_rtttl.play(board.A3, song)
    time.sleep(1)
```
