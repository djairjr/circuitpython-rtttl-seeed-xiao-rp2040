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
In file rtttlsongs.txt I put a big list of songs, one per line:


```py
007:d=4,o=5,b=320:c,8d,8d,d,2d,c,c,c,c,8d#,8d#,2d#,d,d,d,c,8d,8d,d,2d,c,c,c,c,8d#,8d#,d#,2d#,d,c#,c,c6,1b.,g,f,1g.
7Days:d=16,o=6,b=140:g#,d#,8a#5,g#,d#,8a#5,g#,d#,8a#5,g#,d#,8a#5,f,1p5,g#,d#,8a#5,g#,d#,8a#5,g#,d#,8a#5,g#,d#,8a#5,f,1p5,g#,d#,8c,g#,d#,8c,g#,d#,8c,g#,d#,8c,f,1p5,g#,d#,8c,g#,d#,8c,g#,d#,8c,g#,d#,8c,f,1p5,d#,c,8g#5,d#,c,8g#5,d#,c,8g#5,d#,c,8g#5,f,1p5,d#,c,8g#5,d#,c,8g#5,d#,c,8g#5,d#,c,8g#5,f,1p5,d#,c#,8a#5,d#,c#,8a#5,d#,c#,8a#5,d#,c#,8a#5,f,1p5,d#,c#,8a#5,d#,c#,8a#5,d#,c#,8a#5,d#,c#,8a#5,f.
Adams Family:d=8,o=5,b=160:c,4f,a,4f,c,4b4,2g,f,4e,g,4e,g4,4c,2f,c,4f,a,4f,c,4b4,2g,f,4e,c,4d,e,1f,c,d,e,f,1p,d,e,f#,g,1p,d,e,f#,g,4p,d,e,f#,g,4p,c,d,e,f
Agadoo:d=8,o=5,b=125:b,g#,4e,e,e,4e,e,e,e,e,d#,e,4f#,a,f#,4d#,d#,d#,4d#,d#,d#,d#,d#,c#,d#,4e
Alice Cooper-Poison:d=8,o=5,b=112:d,d,a,d,e6,d,d6,d,f#,g,c6,f#,g,c6,e,d,d,d,a,d,e6,d,d6,d,f#,g,c6,f#,g,c6,e,d,c,d,a,d,e6,d,d6,d,f#,g,c6,f#,g,c6,e,d,c,d,a,d,e6,d,d6,d,a,d,e6,d,d6
Alvin and the Chipmonks:d=4,o=5,b=285:g,p,c,c,a,c,c,c,p,b,b,c6,c6,p,c,c,p,a,g,d,2g,d,2p,a,g,d,2g,a,p,g,p,c,c,a,c,c,c,p,b,b,c6,c6,p,c,c,p,a,g,d,2g,d,2p,a,a,g,2a,g,p,2a,b,2a,g,p,c,c,c,c,c,e,e,e,e,2a,g,2a,2g,2a,a,2g,2g.,p,2a,g,2a,g,p,c,c,c,c,c,e,e,e,e,2a,g,2a,2g,2c6,b,2b,1b,2c6
Amazing Grace:d=16,o=5,b=80:8c,2f,a,g,f,2a,8a,8g,2f,4d,2c,8c,2f,a,g,f,2a,8g,8a,2c6.
Axel:d=8,o=5,b=125:16g,16g,a#.,16g,16p,16g,c6,g,f,4g,d.6,16g,16p,16g,d#6,d6,a#,g,d6,g6,16g,16f,16p,16f,d,a#,2g,4p,16f6,d6,c6,a#,4g,a#.,16g,16p,16g,c6,g,f,4g,d.6,16g,16p,16g,d#6,d6,a#,g,d6,g6,16g,16f,16p,16f,d,a#,2g
Ba Ba Black Sheep:d=8,o=5,b=150:c,4p,c,4p,g,4p,g,4p,4a,4b,4c6,4a,4g,4p,f,4p,f,4p,e,4p,e,4p,d,4p,d,4p,4c
Back to the Future:d=16,o=5,b=200:4g.,p,4c.,p,2f#.,p,g.,p,a.,p,8g,p,8e,p,8c,p,4f#,p,g.,p,a.,p,8g.,p,8d.,p,8g.,p,8d.6,p,4d.6,p,4c#6,p,b.,p,c#.6,p,2d.6
Barbie Girl:d=8,o=5,b=125:g#,e,g#,c#6,4a,4p,f#,d#,f#,b,4g#,f#,e,4p,e,c#,4f#,4c#,4p,f#,e,4g#,4f#
Batman:d=8,o=5,b=180:d,d,c#,c#,c,c,c#,c#,d,d,c#,c#,c,c,c#,c#,d,d#,c,c#,c,c,c#,c#,f,p,4f
Be bopalula:d=8,o=5,b=180:a,p,a,e,g,p,a,p,a,p,a,p,g,p,a,4p,a,a,e,g,p,a,p,a,p,a,p,g,p,a
Benny Hill:d=16,o=5,b=125:8d.,e,8g,8g,e,d,a4,b4,d,b4,8e,d,b4,a4,b4,8a4,a4,a#4,b4,d,e,d,4g,4p,d,e,d,8g,8g,e,d,a4,b4,d,b4,8e,d,b4,a4,b4,8d,d,d,f#,a,8f,4d,4p,d,e,d,8g,g,g,8g,g,g,8g,8g,e,8e.,8c,8c,8c,8c,e,g,a,g,a#,8g,a,b,a#,b,a,b,8d6,a,b,d6,8b,8g,8d,e6,b,b,d,8a,8g,4g
Bethoven:d=4,o=5,b=160:c,e,c,g,c,c6,8b,8a,8g,8a,8g,8f,8e,8f,8e,8d,c,e,g,e,c6,g.
Birdy Song:d=16,o=5,b=100:g,g,a,a,e,e,8g,g,g,a,a,e,e,8g,g,g,a,a,c6,c6,8b,8b,8a,8g,8f,f,f,g,g,d,d,8f,f,f,g,g,d,d,8f,f,f,g,g,a,b,8c6,8a,8g,8e,4c
Black Bear:d=4,o=5,b=180:d#,d#,8g.,16d#,8a#.,16g,d#,d#,8g.,16d#,8a#.,16g,f,8c.,16b4,c,8f.,16d#,8d.,16d#,8c.,16d,8a#.4,16c,8d.,16a#4,d#,d#,8g.,16d#,8a#.,16g,d#,d#,8g.,16d#,8a#.,16g,f,f,f,8g.,16f,d#,g,2d#
Bod:d=8,o=5,b=250:a,b,a,4c#6,a,4c#6,c#6,4b,16a,16b,16a,e,4p,e,f#,e,4g,4g,4g,4f#,e,2p,a,b,a,4c#6,a,4c#6,c#6,4b,16a,16b,16a,e,4p,e,f#,e,4g,4g,4g,4g,g#,a,b,4e,4p,a,c#6,a,p,f#,e,4p,a,c#6,a,p,f#,e,2p,4f#,4a,4a,4b,4c6,b,a,p,a,b,a,4c#6,a,4c#6,c#6,4b,16a,16b,16a,e,4p,e,f#,e,4g,4g,4g,4g#,a
Bolero:d=16,o=5,b=80:c6,8c6,b,c6,d6,c6,b,a,8c6,c6,a,4c6,8c6,b,c6,a,g,e,f,2g,g,f,e,d,e,f,g,a,4g,4g,g,a,b,a,g,f,e,d,e,d,8c,8c,c,d,8e,8f,4d,2g
Borteus:d=16,o=5,b=160:b,p,c6,p,d6,b,g,e,b,g,e,c,g,e,c,a4,4p,c6,p,d6,p,e6,c6,a,f,c6,a,f,d,a,f,d,b4,2p,g6,e6,c6,a,f,d,b4,c6,a,f,d,b4,f,d,b4,f,4e.
BSP:d=8,o=5,b=170:d6,p,c6,p,a,a,c6,c6,d6,d6,c6,a,4p,d6,p,e6,e6,d6,p,b,b,d6,p,e6,p,d6,b,p,d6,d6,d6,d6,p,c6,p,a,a,c6,c6,d6,d6,c6,a,2p,g,g,a,a#,b,d,e,4g.
Camberwick Green:d=16,o=5,b=63:8d,d,8a,a,g,a,g,8d.,8d,g,8a,c6,b,a,g,a,b,c6,2d6,p,c6,b,a,4g,f#,e,4d.,8e.6,4b.,8a.,8d,d,8a,a,g,a,g,8d.,8d,g,8a,c6,b,a,g,a,b,c6,2d6,p,c6,b,a,4g,f#,e,4d.,8e.6,4b.,8a.,8d,g,8e,a,8f#,b,8e,a,8d,g,8e,a,8f#,b,8e,a,8d,g,2e
Canon:d=8,o=5,b=80:d,f#,a,d6,c#,e,a,c#6,d,f#,b,d6,a,c#,f#,a,b,d,g,b,a,d,f#,a,b,f#,g,b,c#,e,a,c#6,4f#6,f#,a,4e6,e,a,4d6,f#,a,4c#6,c#,e,4b,d,g,4a,f#,d,4b,d,g,4c#.6
Cantina:d=8,o=5,b=250:a,p,d6,p,a,p,d6,p,a,d6,p,a,p,g#,4a,a,g#,a,4g,f#,g,f#,4f.,d.,16p,4p.,a,p,d6,p,a,p,d6,p,a,d6,p,a,p,g#,a,p,g,p,4g.,f#,g,p,c6,4a#,4a,4g
Captain Pugwash:d=16,o=5,b=160:g,g,g,g,8p,g,g,g,8g,d6,8b,g,8b,d6,8g6,d6,8b,g,d,d,d,d,8p,d,d,d,8d,a,8f#,d,8f#,a,8d6,a,8f#,d,g,g,g,g,8p,g,g,g,8g,d6,8b,g,8b,d6,8g6,p,8g,p,8d,g6,8f#6,e6,8d6,c6,8b,a,g,8p,8b,p,8g,p,8b,c6,d6,d6,d6,d6,8p,d6,d6,d6,8d6,p,8e6,f#6,8g6,f#6,8e6,d6,8c6,b,8c6,d6,8e6,d6,8c6,b,8a,g,8f#,g,8a,g,8f#,d,8e,f#,g,g,g,g,8p,g,f,g,g,8p,g,e,g,g,8p,g,d#,g,g,8p,8d,g6,8f#6,e6,8d6,c6,8b,a,g,8p,8b,p,4g
Chariots of Fire:d=16,o=5,b=85:8c#,f#.,g#.,a#.,4g#,4f,8p,8c#,f#.,g#.,a#.,2g#,8p,8c#,f#.,g#.,a#.,4g#,4f,8p,8f,f#.,f.,c#.,2c#
Coca Cola:d=16,o=5,b=125:f#6,p,f#6,p,f#6,p,f#6,p,4g6,f#6,p,4e6,p,e6,p,8a6,4f#6,4d6
Colonel Bogey:d=8,o=5,b=140:g,e,4p,p,e,f,g,e6,p,e6,p,2c6,g,e,4p,p,e,f,e,g,p,g,p,2f,f,d,4p,p,d,e,f,g,e,4p,p,e,f#,e,d,g,p,e,f#,d,p,a,g.,16f#,g,a,g,f,e,d
Dallas:d=8,o=5,b=125:e,4a.,e,4e.6,a,4c#6,b,c#6,4a,4e,4a,4f#6,4e6,c#6,d6,2e.6,p,e,4a,4f#6,4e6,c#6,d6,4e6,b,c#6,4a,4e,4a,c#6,d6,4b.,a,2a
Dangerman:d=4,o=6,b=355:a.,8g,a,8a,p,8a5,8p,d,p,a.,8g,a,8a,p,8a5,8p,d,p,a,a,a#,a#,a#,a#,a#,a#,a#,c7,2a,p,8a5,8p,d,p,a.,8g,a,8a,p,8a5,8p,d,p,a.,8g,a,8a,p,8a5,8p,d,p,a,a,a#,a#,a#,a#,a#,a#,a#,c7,2d7,p,8a5,8p,d,p,a.,8a,2a#.,8a#5,8p,d#,2p,a#,2a#,2f#,2d#,a#.,8a#,2b.,8b5,8p,e,2p,b,2b,2g,2e,b.,8d7,1e.7,e7,8e7,8e7,e7,f7,f7,f7,f7,f7,f7,f7,d7,e.7,8p,b,1e.7
Death March:d=4,o=5,b=100:4c,16p,c,8c,32p,2c,d#,8d,32p,d,8c,32p,c,8b4,32p,2c.
Deep Purple-Lazy:d=8,o=5,b=160:d.4,f4,16d4,g4,16f4,d.4,f4,16d4,g4,16f4,d4
Deep Purple-Smoke on the Water:d=4,o=4,b=112:c,d#,f.,c,d#,8f#,f,p,c,d#,f.,d#,c,2p,8p,c,d#,f.,c,d#,8f#,f,p,c,d#,f.,d#,c
Digimon:d=8,o=5,b=112:c,g,f#,p,16c,16c,g,f#,g,16c,16c,g,f#,g,a#,a#,4p,c,g,f#,p,16c,16c,g,f#,g,16c,16c,g,f#,d#,4c
Don't Care:d=16,o=5,b=125:f,e,f,e,f,e,8d,e,d,e,d,e,d,c,d,4d
Dragonballz:d=16,o=5,b=140:4f6,48f.6,4g#6,4c7,48f.7,4g#6,4c7,48f.7,2p,2f6,2f,2f6,48f.,48f.,48f.,48f.,48f.,48f.,32p,48d#.6,48d#.,48d#.6,48d#.,48d#.,48d#.,48d#.,48d#.,48d#.,32€,48f.6,48f.,48f.6,48f.,48f.,48f.,48f.,48f.,48f.,6p,8f,8f7,8f6,8f,8f7,48f.6,48f.6,48f.6,48f.6,48f.6,48f.6,48f.6,p,a#,a#,p,c6,c,c6
Dream:d=8,o=4,b=220:c3,4p.,c,4p,d#3,p,d#,d#3,p,d#,p,d#3,p,f3,4p.,f,4p,g3,p,g,g3,p,a#3,p,c,p,c3,p,f5,p,c,p,c5,d#3,f5,d#,d#3,p,d#,f5,d#3,g5,f3,p,f5,p,f,p,f5,g3,g5,g,g3,p,a#3,p,c,p,c3,g5,f5,p,c,g5,c5,d#3,f5,d#,d#3,p,d#,f5,d#3,g5,f3,g,f5,p,f,g5,f5,g3,g5,g,g3,p,a#3,d#5,c,p,c3,g5,f5,c5,c,g5,c5,d#3,f5,d#,d#3,g5,d#,f5,d#3,g5,f3,g,f5,d#5,f,g5,f5,g3,g5,g,g3,f5,a#3,d#5,c,c5,c3,g5,f5,p,c,g5,c5,d#3,f5,d#,d#3,p,d#,f5,d#3,g5,f3,g,f5,p,f,g5,f5,g3,g5,g,g3,p,a#3,d#5,c,p,c3,p,f5,p,c,p,c5,d#3,f5,d#,d#3,p,d#,f5,d#3,g5,f3,p,f5,p,f,p,f5,g3,g5,g,g3,p,a#3,p,c,p,c3,4p.,c,4p,d#3,p,d#,d#3,p,d#,p,d#3,p,f3,4p.,f,4p,g3,p,g,g3,p,a#3,p,c
Duelling Banjos:d=8,o=5,b=200:c#,d,4e,4c#,4d,4b4,4c#,4a4,4b4,4p,16c#6,16p,16d6,16p,e6,p,c#6,p,d6,p,b,p,c#6,p,a,p,4b,4p,4a4,4a4,4b4,4c#,4a4,4c#,4b4,4p,a,p,a,p,b,p,c#6,p,a,p,c#6,p,b
Dustman:d=16,o=5,b=140:8a.,a,b,p,c6,p,8c#6,4p,8e6,c#6,p,c#6,p,c#6,p,c#6,p,c#6,p,4c#6,c#6,p,c#6,p,c#6,p,d6,p,c#6,p,4b,b,p,b,p,b,p,b,p,b,p,b,p,b,p,8b.,p,e6,e6,e6,p,d6,p,c#6,p,b,p,4a
Entertainer:d=8,o=5,b=140:d,d#,e,4c6,e,4c6,e,2c.6,c6,d6,d#6,e6,c6,d6,4e6,b,4d6,2c6,4p,d,d#,e,4c6,e,4c6,e,2c.6,p,a,g,f#,a,c6,4e6,d6,c6,a,2d6
Fairground:d=8,o=6,b=225:c,c,b5,c,16d,4p,2d,16p,16e,4p,2e,16p,16g,4p,1f,p,8f,f,e,d,c,p,c#,d,p,c#,2c,8c,c,c,c,c,p,c#,d,p,c#,2c,8c,c,b5,c,16d,4p,2d,16p,16e,4p,2e,16p,16g,4p,1f,p,8f,f,e,d,4e,e,e,f,f#,4g,g5,g5,a5,b5,16c,p,b5,16c,p,b5,2c,8c5,4c5,c5,2c5,4e5,g5,4d.,p,4d.,p,4d.,4p,c,c,a5,c,4d.,4p,a#5,a#5,g5,a#5,4d.
Fawlty Towers:d=8,o=5,b=125:16b,16c6,d6,c#6,d6,c#6,d6,g6,4e6.,d6,c6,b,c6,b,c6,b,c6,f#6,4d6.,c6,b,a,g,f#,g,f#,g,d6,c6,b,c6,b,a,g,f#,g,e,f#,4d,c6,d6,b,c6,4a
Figaro:d=8,o=5,b=250:d,c#,d,c#,d,4p,32p,d,c#,d,e,f#,e,f#,g,a,g#,a,g#,a,4p,32p,a,g#,a,a#,b,a,g,f#,e,d#,e,f#,g,f#,e,d,c#,d,e,d,c#,a4,b4,c#,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,1p,4p,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,1p,4p,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6,d,d6.
Final Countdown:d=16,o=5,b=125:b,a,4b,4e,4p,8p,c6,b,8c6,8b,4a,4p,8p,c6,b,4c6,4e,4p,8p,a,g,8a,8g,8f#,8a,4g.,f#,g,4a.,g,a,8b,8a,8g,8f#,4e,4c6,2b.,b,c6,b,a,1b
Flintstones:d=8,o=5,b=200:g#,4c#,p,4c#6,a#,4g#,4c#,p,4g#,f#,f,f,f#,g#,4c#,4d#,2f,2p,4g#,4c#,p,4c#6,a#,4g#,4c#,p,4g#,f#,f,f,f#,g#,4c#,4d#,2c#
Flute:d=8,o=5,b=160:16a,16g,16a,16a#,c6,c6,c6,c6,c6,c6,c6,c6,4f.,4p,32f,16e,16f,16g,a,a,a,a,a,a,a,a,4d.,4p,16d,16c,16d,16e,f,f,f,c,g,g,g,c,a,f,a,c6,f6,c6,d6,a#,c6,f,a,c6,f6,c6,d6,a#,4c6,4p,4f.,f,4a4,4p,4e,4p,f,g,f,a,a#,a,f,g,f,d,e,d,c#,d,c#,a4,b4,a4,c#,d,c#,e,f,e,f,g,f,a,a#,a,f,g,f,d,e.
Fraggle Rock:d=8,o=5,b=112:c6,16c6,c6,16c6,a,2p,b,b,a,g,16e6,d6,c6,16a,g,c6,16c6,c6,16d6,a,2p,b,16b,a,16b,c6
Friends:d=4,o=5,b=80:c,g,a#4,f,c,g,a#4,8a#,8e,c,g,a#4,f,c,g,a#4,8a#,8e
Fruit and Nut:d=16,o=5,b=70:d,c#,d,c#,d,p,c#,p,e,p,32d,32f#,32a,32d6,8f#.6,p,g6,f#6,g6,f#6,e6,d6,a,f#,8d.,32f#,32d6,8c#.6,p,b,b4,b4,32b4,32c#,b4,p,a4,p,b,b4,b4,32b4,32c#,b4,p,a4,p,d6,d,d,d,d,c#,e,d,d,c#,b4,a4,8g6,32e6,32c#6,32g,32e,d,c#,d,c#,d,p,c#,p,e,p,32d,32f#,32a,32d6,8f#.6,32p,g6,f#6,g6,f#6,e6,d6,a,f#,8d.,32f#,32d6,8c#.6,p,b,b4,b4,32b4,32c#,b4,p,a4,p,b,b4,b4,32b4,32c#,b4,p,a4,p,b,b4,8b4,8c#,32p,8c#,8d.
Funky Town:d=8,o=4,b=125:c6,c6,a#5,c6,p,g5,p,g5,c6,f6,e6,c6,2p,c6,c6,a#5,c6,p,g5,p,g5,c6,f6,e6,c6
Futurama:d=8,o=5,b=112:e,4e,4e,a,4a,4d,4d,e,4e,4e,e,4a,4g#,4d,d,f#,f#,4e,4e,e,4a,4g#,4b,16b,16b,g,g,f#,f#,4e,4e,a,4a,4d,4d,e,g,f#,4e,e,4a,4g#,4d,d,f#,f#,4e,4e,e,4a,4g#,4b,16b,16b,g,g,f#,f#,p,16e,16e,e,d#,d,d,c#,c#
GB National Anthem:d=4,o=5,b=90:g,g,a,f#.,8g,a,b,b,c6,b.,8a,g,a,g,f#,g.,8a,8b,8c6,d6,d6,d6,d.6,8c6,b,c6,c6,c6,c.6,8b,a,b,8c6,8b,8a,8g,b.,8c6,d6,8e6,8c6,b,a,g.
Ghost Busters:d=8,o=5,b=145:16c6,32p,16c6,e6,c6,d6,a#,2p,32c6,32p,32c6,32p,c6,a#,c6
Greensleaves:d=4,o=5,b=140:g,2a#,c6,d.6,8d#6,d6,2c6,a,f.,8g,a,2a#,g,g.,8f,g,2a,f,2d,g,2a#,c6,d.6,8e6,d6,2c6,a,f.,8g,a,a#.,8a,g,f#.,8e,f#,2g
Halloween:d=8,o=5,b=180:d6,g,g,d6,g,g,d6,g,d#6,g,d6,g,g,d6,g,g,d6,g,d#6,g,c#6,f#,f#,c#6,f#,f#,c#6,f#,d6,f#,c#6,f#,f#,c#6,f#,f#,c#6,f#,d6,f#
Have I Got News for You:d=16,o=5,b=100:8a,g,e,8g,e,d,c,d,e,8a,c6,8a,g,e,8c6,a,g,8d6,c6,a,c6,d6,8e6,8d6,8c6,8b,c6,8e6,8d6,c6,b,8a,a,e,g,8a,2a,a,g,a,8a,g,e,g,a,g,a,8c6,a,g,e,a,g,a,8a,g,e,g,a,g,e,8g,8a,a,g,8a,8a,8g,8a,8c6,8a,8c6,8d#6,8c#6,8a#,8f#,4e.
Hawaii 5 0:d=16,o=6,b=240:8g#5,p,8g#5,p,8b5,p,4d#,p,2c#.,p,2g#5.,p,8g#5,p,8g#5,p,8f#5,p,4b5,p,1g#5,4p.,8g#5,p,8g#5,p,8b5,p,4d#,p,2c#,8p,2g#.,8p,8f#,p,8f#,p,8d#,p,4b5,p,1g#.,4p,2b,p,8a,8g#,8f#,8e,8d#,8c#,8d#,8b5,2c#,4p,8c#,p,8b,8a,8g,8f#,8d#,8c#,8b5,8c#,4d#,8c#,p,4b5,p,4c#.,p,2g#,4p,8f#,p,8f#,p,8d#,p,4b5,p,1c#6
Heman:d=8,o=6,b=160:g,g,g,4g,4e,g,a,g,f,4g,4c,g,a,g,f,4g,4e,c,2d.,4p,4e.,4a5,4c,e,f#,e,d,4e,4a5,e,f#,e,d,4e,4a5,g5,2a5
Henrys Cat:d=8,o=6,b=355:g,p,d,p,d7,p,b5,p,16b5,16b,p,16c,16g,p,d,p,g,p,d,p,d7,p,b,p,16b5,16g,p,16c,16a,p,c,p,b,p,c,p,g,p,d,p,d7,p,b5,p,16b5,16b,p,16c,16g,p,d,p,g,p,d,p,d7,p,b,p,16b5,16g,p,16c,16a,p,c,p,b,p,c,p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16b5,b,16p,16c,c7,16p,16c#,d7,16p,16d,d#7,16p,16e7,e
Hitchcock:d=16,o=5,b=200:c,p,f4,8p,8f,32g,32p,f,32p,e,32p,d,32p,e,8p,f,32p,g,8p.,c,p,f4,8p,8f,32g,32p,f,32p,e,32p,d,32p,e,8p,f,32p,g,8p.,c,p,f4,8p,g#,32p,8c6,p,a#,32p,g#,8p,c6,32p,8d#6,p,c#6,32p,c6,8p,d#6,32p,8g6,p,f6,32p,e6,32p,c#6,32p,c6,32p,a#,32p,g#,32p,g,32p,8f4
Hunter:d=4,o=5,b=500:a#4,c#,f,a#,c#6,f6,a6,f6,d#6,c#6,c6,a#,d#,f#,a#,c#6,2f6,2d#6,p,f#,a,c6,d#6,2f#6,2f6,d#6,c#6,c6,a#4,c#,f,a#,2c#6,2a#.
If I Were a Rich Man:d=8,o=5,b=160:g,f,g,f,e,p,4c,4p,e,f,g,f,g,f,e,f,g,a,a#,a,a#,a,2g.,4p,4g#,4g,4f#,4f,d#,d,c,d,4d#,4p,d#,d,c,d,4d#,4c,4g,4p
Itchy and Scratchy:d=8,o=5,b=160:c6,a,4p,c6,a6,4p,c6,a,c6,a,c6,a6,4p,p,c6,d6,e6,p,e6,f6,g6,4p,d6,c6,4d6,f6,4a#6,4a6,2c7
Jackson:d=8,o=5,b=120:b,e6,g#6,a6,g#6,e6,b,a,g#,a,4b.,4p,16b,16b,e6,g#6,a6,g#6,e6,b,a,g#,a,4b.,p,16b,16b,c#6,16c#6,e6,16e6,f#.6,16e6,e6,p,16e6,16e6,c#6,c#6,e6,e6,f#6,e6,f#6,4g#.6,1p,4b,4b,b,16f#6,16f#6,16f#6,f#.6,g#6,f#6,e6,e6,e6,c#6,e6,e6,c#6,f#6,4e6,4e.6,1p,b,e6,g#6,a6,g#6,e6,b,a,g#,a,4b.,4p,16b,16b,e6,g#6,a6,g#6,e6,b,a,g#,a,4b.,p,16b,16b,c#6,16c#6,e6,16e6,f#.6,16e6,e6,p,16e6,16e6,c#6,c#6,e6,e6,f#6,e6,f#6,4g#.6,1p,4b,4b,b,16f#6,16f#6,16f#6,f#.6,g#6,f#6,e6,e6,e6,c#6,e6,e6,c#6,f#6,4e6,4e.6.
Jesus Christ Superstar:d=8,o=5,b=100:f,d,2a#4,4g,d#,2a#4,4g#,f,g#,4g,f,d#,4f,d,4a#4.
Jingle Bells:d=4,o=5,b=170:b,b,b,p,b,b,b,p,b,d6,g.,8a,2b.,8p,c6,c6,c6.,8c6,c6,b,b,8b,8b,b,a,a,b,2a,2d6
Kiss:d=4,o=5,b=140:8d4,8e4,f.4,8g4,f4,e4,d4,c4,2d4,8d4,8c4,2d4,8d4,8e4,f.4,8g4,f4,e4,c4,e4,2d.4
Knight Rider:d=32,o=5,b=63:16e,f,e,8b,16e6,f6,e6,8b,16e,f,e,16b,16e6,4d6,8p,4p,16e,f,e,8b,16e6,f6,e6,8b,16e,f,e,16b,16e6,4f6
Led Zepelin-Stairway to Heaven:d=8,o=5,b=63:a4,c,e,a,b,e,c,b,c6,e,c,c6,f#,d,a4,f#,e.,16c,a4,4e,c,a4,e,g4,a4,4a4
Let it be:d=8,o=5,b=100:16e6,d6,4c6,16e6,g6,a6,g.6,16g6,g6,e6,16d6,c6,16a,g,4e.6,4p,e6,16e6,f.6,e6,e6,d6,16p,16e6,16d6,d6,2c.6.
Let it Snow:d=8,o=5,b=120:c,c,c6,c6,4a#,4a,4g,4f,2c,c,16c,4g.,f,4g.,f,4e,2c,4d,d6,d6,4c6,4a#,4a,2g.,e.6,16d6,4c6,c.6,16a#,4a,a#.,16a,2f.,4c,c6,c6,4a#,4a,4g,4f,2c,c.,16c,4g.,f,4g.,f,4e,2c,4d,d6,d6,4c6,4a#,4a,2g.,e.6,16d6,4c6,c.6,16a#,4a,a.,16g,2f.
Light My Fire:d=8,o=5,b=140:b,16g,16a,b,d6,c6,b,a,g,a,16f,16a,c6,f6,16d6,16c6,16a#,16g,g#,g,g#,16g,16a,b,c#6,16b,16a,16g,16f,e,f,4a
Macarena:d=8,o=5,b=180:f,f,f,4f,f,f,f,f,f,f,f,a,c,c,4f,f,f,4f,f,f,f,f,f,f,d,c,4p,4f,f,f,4f,f,f,f,f,f,f,f,a,4p,2c.6,4a,c6,a,f,4p,2p
Magic Roundabout:d=16,o=5,b=100:4c6,c6,p,8c6,4g,4g,4a,a,p,8a,2f,4a#,a,p,8a,4f,8f.,4b.,b,p,8b,2g
Match of the day:d=8,o=5,b=100:c,f,a,c.6,16a,a,a,a,4a,a#,c.6,16a,g,a,a#,c,e,g,a#.,16g,g,g,g,4g,a,a#.,16g,f,g,a,c,f,a,c.6,16a,a,a,a,4a,a#,c.6,16a,a#,c6,4d6,d6,e6,f6,16f6,e6,16e6,d6,f6,c6,c6,d6,c6,16a#,a,16a,g,4f
Metsa:d=4,o=5,b=230:a4,d,e,f,e,d,1a,p,a4,d,e,f,e,d,1a#,g,a,a#,a#,a,g,1a,p,a4,c#,e,g,f,e,1d,p,d.6,8c6,2c.6,8e,8p,d.6,8a#,2a.,8c,8p,a#.,8a,2g.,8e,8p,a.,8g,2f.,8p,a,a,2a,g,f,2e,e,f,e,a4,a#4,a4,2f,e,2d.,p,d6,c#6,d6,p,a,g#,a,p,f,e,f,p,d,c#,2d.,2a#,a,g,a#,d6,2a.,p,a4,c#,d,2e.,a4,d,e,2f.,a4,c#,e,2f,e,2d..
Mission Impossible:d=16,o=5,b=100:32d,32d#,32d,32d#,32d,32d#,32d,32d#,32d,32d,32d#,32e,32f,32f#,32g,g,8p,g,8p,a#,p,c6,p,g,8p,g,8p,f,p,f#,p,g,8p,g,8p,a#,p,c6,p,g,8p,g,8p,f,p,f#,p,a#,g,2d,32p,a#,g,2c#,32p,a#,g,2c,p,a#4,c
Monty Python:d=8,o=5,b=180:d#6,d6,4c6,b,4a#,a,4g#,g,f,g,g#,4g,f,2a#,p,a#,g,p,g,g,f#,g,d#6,p,a#,a#,p,g,g#,p,g#,g#,p,a#,2c6,p,g#,f,p,f,f,e,f,d6,p,c6,c6,p,g#,g,p,g,g,p,g#,2a#,p,a#,g,p,g,g,f#,g,g6,p,d#6,d#6,p,a#,a,p,f6,f6,p,f6,2f6,p,d#6,4d6,f6,f6,e6,f6,4c6,f6,f6,e6,f6,a#,p,a,a#,p,a,2a#
Mozart:d=16,o=5,b=125:16d#,c#,c,c#,8e,8p,f#,e,d#,e,8g#,8p,a,g#,g,g#,d#6,c#6,c6,c#6,d#6,c#6,c6,c#6,4e6,8c#6,8e6,32b,32c#6,d#6,8c#6,8b,8c#6,32b,32c#6,d#6,8c#6,8b,8c#6,32b,32c#6,d#6,8c#6,8b,8a#,4g#,d#,32c#,c,c#,8e,8p,f#,e,d#,e,8g#,8p,a,g#,g,g#,d#6,c#6,c6,c#6,d#6,c#6,c6,c#6,4e6,8c#6,8e6,32b,32c#6,d#6,8c#6,8b,8c#6,32b,32c#6,d#6,8c#6,8b,8c#6,32b,32c#6,d#6,8c#6,8b,8a#,4g#
Mr Benn:d=8,o=6,b=200:a5,g#5,g5,p,c,e,p,g,2f#,g,a,g,p,e,c,p,g5,2f#5,g5,a5,g5,p,e,d#,p,f,e,d,c,e,g,a,2a#.,p,c,d,e,f,g,a,p,g#,a,p,c,2d,e,f,4g.,4e.,4c.,p,e,d,e,d,c,b5,c,4d.,4p,a,g,a,g,f,g,f,e,f,e,d,b5,a5,g5,p,c,e,p,g,2f#,g,a,g,p,e,c,p,g5,2f#5,g5,a5,g5
Mr Men:d=4,o=5,b=112:a,8d.6,16e6,8f#.6,16g6,8f#.6,16e6,f#6,a,b,d6,p,b,c#6,e6,1a,8g.,16f#,8g.,16f#,g,d6,1f#,8e.,16d#,8e.,16d#,e,b,2d#,g#,f#,f#,8b.,16c#6,8d#.6,16e6,8d#.6,16c#6,d#6,f#,g#,b,p,g#,a#,c#6,1f#6,p,g#6,8f#.6,16d#6,8b.,16g#,2b,2c#6,2b.
Munsters:d=8,o=5,b=160:d,f,d,g#,a,4d6,a#,a,2g,f,g,4a,a4,g#4,a4,b4,4c#,2d,4p,4c,4c6,4c6,2c6,a#,a,a#,g,a,4f,4p,4g,4g,2g,f,e,f,d,e,2c#,4p,4d,f,d,g#,a,4d6,a#,a,2g,f,g,4a,a4,g#4,a4,b4,4c#,2d
Muppet:d=8,o=5,b=250:c6,4c6,4a,4b,a,4b,4g,4p,4c6,4c6,4a,b,a,p,4g.,4p,4e,4e,4g,4f,e,4f,c6,c,d,4e,e,e,p,e,4g,2p,4c6,4c6,4a,4b,a,4b,4g,4p,4c6,4c6,4a,b,4a,4g.,4p,4e,4e,4g,4f,e,4f,c6,c,d,4e,e,4d,d,4c
Muppets:d=4,o=5,b=250:c6,c6,a,b,8a,b,g,p,c6,c6,a,8b,8a,8p,g.,p,e,e,g,f,8e,f,8c6,8c,8d,e,8e,8e,8p,8e,g,2p,c6,c6,a,b,8a,b,g,p,c6,c6,a,8b,a,g.,p,e,e,g,f,8e,f,8c6,8c,8d,e,8e,d,8d,c
Napoli:d=16,o=4,b=63:f.,g.,g#.,a#.,c.5,g#,8c5,8c.5,8p,a#.,c.5,c#.5,a#.,c#.5,a#.,8f5,8f.5,8p,f.5,g.5,g#.5,g.5,f.5,g.5,8c5,8c.5,8p,a#.,c.5,a#.,g#.,g.,8g#,8f.
New Year:d=8,o=5,b=125:a4,4d.,d,4d,4f#,4e.,d,4e,f#,e,4d.,d,4f#,4a,2b.,4b,4a.,f#,4f#,4d,4e.,d,4e,f#,e,4d.,b4,4b4,4a4,2d,16p
Nut cracker Suite:d=16,o=5,b=76:16g6,e6,8g6,8p,f#6,p,d#6,p,e6.,p.,d6,d6,d6,8p,c#6,c#6,c#6,8p,c6,c6,c6,8p,b,e6,c6,e6,b,4p,g,e,8g,p,f#,p,c6,p,8b,8p,g6,g6,g6,8p,f#6,f#6,f#6,8p,e6,e6,e6,8p,d#6,f#6,e6,f#6,d#6,4p.,g6,e6,g6.,32p,f#6,p,d#6,p,e6,p,d6,d6,d6,p,c#6,c#6,c#6,p,c6,c6,c6,p,b,e6,c6,e6,b,2p,
Nut march:d=8,o=5,b=140:a#,p,a#,a#,a#,c6,p,c6,p,d6,p,a#,p,2c6,a#,p,a#,a#,16a#.,c6,16p,c6,p,d6,p,a#,p,4c.6,16p,16c,g#,16p,16a#,g#,16p,16g,f,16p,16d#,d,16p,16a#4,g,16p,16g#,g,16p,16f,d#,16p,16d,c,16p,16d#,d,16p,16c,b4,16p,16f,d#,16p,16d,c,16p,16g,g#,16p,16g,f,16p,16d#,16a#,p,32f,32g#,16a#.
Oh Little Start of Bethlehem:d=8,o=5,b=120:16c.,16p,f,p,f,p,4f,4g,a,g,a,a#,c.6,16p,4a,4a#,a,16f.,g.,16p.,g,p,2f.,16c.,16p,f,p,f,p,4f,4g,a,g,a,a#,c.6,16p,4a,4a#,a,16f.,g.,16p,32p,g,p,2f.
On Ilckley Moor:d=8,o=5,b=100:d,g.,16g,g,d,4g,p,a,b.,16b,b,a,4b,p,b,4a,4g,4g,4f#,2g
On the 12th Day of christmas:d=8,o=5,b=150:d,d,4g,g,g,4g,g,g,a,b,c6,a,4b.,p,4d6,a,b,c6,a,d6,d6,a,b,c6,a,4d6,4e6,4d.6,p,d6,c6,b,a,4g,a,b,4c6,4e,4e,4d,g,a,b,c6,4b,4a,2g.
Oxygen:d=8,o=5,b=140:c6,p,g,d#,g.,p,2c,4p,4c6,p,g,d#,g.,p,2c,4p,4a#.,16p,a,g,a.,p,2d,4p,4c6,p,g,d#,g.,p,2c,4p,4c6,p,g,d#,g.,p,2c,4p,4a#.,16p,a,g,a.,p,2d,4p,a.,16g.,f.,2c,p,a.,16g.,f.,2c
Pager:d=8,o=5,b=160:d6,16p,2d6,16p,d6,16p,2d6,16p,d6,16p,2d6.
Phantom:d=8,o=5,b=120:4d6,d6,4a6,a6,4b6,g6,4a6,a6,4d6,d6,4a6,a6,a6,g6,f6,4e6,e6,4d6,d6,4a6,a6,4b6,g6,4a6,a6,4d6,d6,4a6,a6,f6,e6,c#6,4d6,d6.
Piccolo:d=8,o=5,b=320:d6,4g6,4g,4g6,d6,e6,d6,b,4g,4d,g,a,b,c6,4d6,4g6,1d6,4d6,4g6,4g,4g6,d6,e6,b,4g,4d,f,g,a,b,4c6,4f6,1c6
Pienian:d=8,o=5,b=160:a4,a4,d,d,f#,f#,2d,f#,f#,e,d,4c#,e,a4,c#,c#,e,e,2c#,e,e,d,c#,4d,f#,d,4g,b,b,4g,b,g,4a,4f#,4f#,p,f#,e,e,e,e,p,e,f#,g#,a,4a4,4a4,b4,c#,d,d,f#,f#,2d,f#,f#,e,d,4c#,4e,4a,4p,4c#,4p,4d.
Pilipom:d=16,o=5,b=160:e,p,e,p,g,p,g,p,b4,c#,d,p,g,p,g,p,e,p,e,p,g,p,g,p,b,g,b,e6,8d#6,8p,d#6,d6,b,a#,d#6,d6,b,a#,d#6,d6,b,a#,b,c6,d6,d#6,b,a#,g,f#,e,d#,c,b4,e,f#,d#,b4,8e,p
Pingu:d=4,o=6,b=285:g,p,e,p,f,e,d,p,g,p,e,p,f,a,g,p,a,c7,b,a,g,c7,g,f,e,f,e,d,g,g,p,f,e,p,g,p,c7,c
Pinky and the Brain:d=16,o=6,b=200:b.5,p,8e.,p,d#.,p,8e.,p,g.,p,4d#.,4p,b.5,p,8e.,p,d#.,p,8e.,p,g.,p,4d#.,4p,4e,8p,8e.,p,g.,p,8a#.,p,4a#,8p,a#.,p,8b.,p,a.,p,4g,8p,4f#,4p,e.,p,8a.,p,g#.,p,8a.,p,b.,p,4g#,4p,e.,p,8a.,p,g#.,p,8a.,p,b.,p,4g#,4p,c.,p,8b.5,p,8b.5,8p,b.5,p
Polka:d=16,o=5,b=140:d,c#,d,e,f,e,f,f#,g,f#,g,a,a#,a,g,a#,a,a4,c#,e,a,g,f,e,f,e,d,c#,d,a4,b4,c#,d,c#,d,e,f,e,f,f#,g,f#,g,a,a#,a,g,a#,a,a4,c#,e,a,g,f,e,d,4p,2c#,8d,8a4,8d
Popcorn:d=16,o=5,b=160:a,p,g,p,a,p,e,p,c,p,e,p,8a4,8p,a,p,g,p,a,p,e,p,c,p,e,p,8a4,8p,a,p,b,p,c6,p,b,p,c6,p,a,p,b,p,a,p,b,p,g,p,a,p,g,p,a,p,f,8a,8p,a,p,g,p,a,p,e,p,c,p,e,p,8a4,8p,a,p,g,p,a,p,e,p,c,p,e,p,8a4,8p,a,p,b,p,c6,p,b,p,c6,p,a,p,b,p,a,p,b,p,g,p,a,p,g,p,a,p,b,4c6
Popeye:d=8,o=6,b=160:a5,c,c,c,4a#5,a5,4c,2p,c,d,a#5,d,4f,d,2c,p,c,d,a#5,d,f,e,d,c,d,c,a5,f5,a5,c,d,c,4a#5,g5,2f5
Porsaita:d=8,o=5,b=200:4g,g,a,g,f,e,f,4g,4e,d,e,4f,4d,c,d,4e,4c,4g,g,a,g,f,e,f,4g,4e,d,e,4f,4d,4g,2c,4c6,4g.,f,e,d,2c,4c6,4g.,f,e,d,2c.
Postman Pat:d=16,o=5,b=100:f#,p,a,p,8b,8p,f#,p,a,p,8b,8p,f#,p,a,p,b,p,d6,d6,c#6,c#6,a,p,4b.,8p,32f#,g,p,a,p,b,p,g,p,8f#.,8e,8p,32f#,g,p,a,p,32b.,32b.,g,p,8f#.,8e,8p,32f#,g,p,a,p,b,p,g,p,f#,p,e,p,d,p,c#,p,2d
Postman Pat:d=16,o=5,b=100:f#,p,a,p,8b,8p,f#,p,a,p,8b,8p,f#,p,a,p,b,p,d6,d6,c#6,c#6,a,p,4b.,8p,48f#.,g,r,a,p,b,p,g,p,8f#.,8e,8p,48f#.,g,p,a,p,32b.,32b.,g,p,8f#.,8e,8p,48f#.,g,p,a,p,b,p,g,p,f#,p,e,p,d,p,c#,p,2d
Prima:d=16,o=5,b=200:4c6,8p,g.,p,2g.,8p,e.,p,4f,p,a.,p,4g,p,c.,p,2c.,4p,e.,p,4f,p,a.,p,4g,p,c,p,2c.,p,c.,p,8c.,8d.,e.,p,1e.,4p,4c6,8p,g.,p,2g.,8p,e.,p,4f,p,a.,p,4g,p,c.,p,2c.,p,e.,p,4f,p,a.,p,4g,p,c,p,2c.,p,c.,p,8c.,8d.,e.,p,1c..
QuoFNigt:d=8,o=5,b=160:16a,16g,16a,16a#,c6,c6,c6,c6,c6,c6,c6,c6,4f.,4p,32f,16e,16f,16g,a,a,a,a,a,a,a,a,4d.,4p,16d,16c,16d,16e,f,f,f,c,g,g,g,c,a,f,a,c6,f6,c6,d6,a#,c6,f,a,c6,f6,c6,d6,a#,4c6,4p,4f.,f,4a4,4p,4e,4p,f,g,f,a,a#,a,f,g,f,d,e,d,c#,d,c#,a4,b4,a4,c#,d,c#,e,f,e,f,g,f,a,a#,a,f,g,f,d,e.
Rhubarb and Custard:d=8,o=5,b=180:e,f,g,4d#.,e,f,g,4d#.,e,f,g,4a#,a#,2g.,e,f,g,4d#.,e,f,g,4d#.,4e,e,4d,d,2c.
Rich Man's World:d=8,o=6,b=112:e,e,e,e,e,e,16e5,16a5,16c,16e,d#,d#,d#,d#,d#,d#,16f5,16a5,16c,16d#,4d,c,a5,c,4c,2a5,32a5,32c,32e,a6
Ring High:d=16,o=6,b=350:b5,d,b5,d,b5,d,b5,d,d,f,d,f,d,f,d,f,f,a,f,a,f,a,f,a.
Ring Low:d=16,o=5,b=355:b4,d,b4,d,b4,d,b4,d,d,f,d,f,d,f,d,f,f,a,f,a,f,a,f,a
Rudolph the Red Nosed Raindeer:d=8,o=5,b=250:g,4a,g,4e,4c6,4a,2g.,g,a,g,a,4g,4c6,2b.,4p,f,4g,f,4d,4b,4a,2g.,g,a,g,a,4g,4a,2e.,4p,g,4a,a,4e,4c6,4a,2g.,g,a,g,a,4g,4c6,2b.,4p,f,4g,f,4d,4b,4a,2g.,g,a,g,a,4g,4d6,2c.6,4p,4a,4a,4c6,4a,4g,4e,2g,4d,4e,4g,4a,4b,4b,2b,4c6,4c6,4b,4a,4g,4f,2d,g,4a,g,4e,4c6,4a,2g.,g,a,g,a,4g,4c6,2b.,4p,f,4g,f,4d,4b,4a,2g.,4g,4a,4g,4a,2g,2d6,1c.6.
Rugrats:d=8,o=7,b=100:c,d,e,f.,g.,a,p,a,g,f,e.,d.,c,p,c,d,e,d.,c.,b6,p,b6,c,d,c.,b.6,a6,p,c,d,e,f.,g.,a,p,a,g,f,e.,d.,c,p,c,d,e,d.,c.,b6
Rule Britania:d=8,o=5,b=100: e.,e,f,4f,e,f.,16e,d.,16c,2b4,4g,4f,16e,16c,16f,16d,g,f,4e,d.,16c,4c
Santa Clause is Coming Tonight:d=4,o=5,b=200:g,8e,8f,g,g.,8g,8a,8b,c6,2c6,8e,8f,g,g,g,8a,8g,f,2f,e,g,c,e,d,2f,b4,1c,p,g,8e,8f,g,g.,8g,8a,8b,c6,2c6,8e,8f,g,g,g,8a,8g,f,f,e,g,c,e,d,2f,b4,1c,p,c6,d6,c6,b,c6,a,2a,c6,d6,c6,b,c6,2a.,d6,e6,d6,c#6,d6,b,b,b,8b,8c6,d6,c6,b,a,g,p,g.,8g,8e,8f,g,g.,8g,8a,8b,c6,2c6,8e,8f,g,g,g,8a,8g,8f,2f,e,g,c,e,d,2f,d6,1c6.
Scale:d=32,o=5,b=160:c,d,e,f,g,a,b,c6,b,a,g,f,e,d,c
Scarlet:16d6,16a,16a#,16d#6,16d,32d,16e,32d,16e,8f,8g,32a.,32a#.,32g.,8a.,16a,32a.,32a#.,32g.,a (Tempo 50)
Scatman:d=16,o=5,b=200:8b,b,32p,8b,b,32p,8b,2d6,p,c#.6,p.,8d6,p,c#6,8b,p,8f#,2p.,c#6,8p,d.6,p.,c#6,b,8p,8f#,2p,32p,2d6,p,c#6,8p,d.6,p.,c#6,a.,p.,8e,2p.,c#6,8p,d.6,p.,c#6,b,8p,8b,b,32p,8b,b,32p,8b,2d6,p,c#.6,p.,8d6,p,c#6,8b,p,8f#,2p.,c#6,8p,d.6,p.,c#6,b,8p,8f#,2p,32p,2d6,p,c#6,8p,d.6,p.,c#6,a.,p.,8e,2p.,c#6,8p,d.6,p.,c#6,a,8p,8e,2p,32p,f#.6,p.,b.,p.
Scooby Doo:d=8,o=6,b=160:e,e,d,d,2c,d,4e,2a5,a5,4b5,4g5,4e,d,4c,d,2e,4p,e,e,d,d,2c,d,4f,2a5,a5,4b5,4g5,4e,d,2c
Sesame Street:d=4,o=5,b=160:2c6,a,2f,8f,8g,a,p,2c6,a,1f,p,2c6,a,2f,8f,8g,a,2b,c6,2d6,p,8c6,8d6,d#6,d6,c6,a,g,8g,8a,a#,a,8g,8c,8c,1c
Simpsons:d=8,o=5,b=160:c.6,4e6,4f#6,a6,4g.6,4e6,4c6,a,f#,f#,f#,2g,p,p,f#,f#,f#,g,4a#.,c6,c6,c6,4c6
Smurfs:d=4,o=5,b=200:2c6,f.6,8c6,d6,a#,2g,c.6,8a,f,a,2g,p,16g,16a,16a#,16b,2c6,f.6,8c6,d6,a#,2g,c.6,8a,a#,e,2f,p,16g,16a,16a#,16b,2c6,f.6,8c6,d6,a#,2g,c.6,8a,f,a,2g,p,16g,16a,16a#,16b,2c6,f.6,8c6,d6,a#,2g,c.6,8a,a#,e,2f.,1p
Soap:d=8,o=5,b=125:g,a,c6,p,a,4c6,4p,a,g,e,c,4p,4g,a,c6,4p,4b,4p,a,g,e,c#,2p,4p,a,c6,2p,4p,a,g,2p,a,g,e,4c
Sorcerers Apprentice:d=18,o=6,b=125:4c,4g,g.5,a.5,b.5,c.,12p,d#.,c.,12p,d#.,d.,c.,b.5,c.,12p,d#.,c.,12p,d#.,d.,c.,b.5,c.,12p,d#.,c.,d#.,d.,c.,d.,d#.,d.,f.,d#.,d.,12p,f#.,c.,12p,d#.,d.,f.,d#.,d.,12p,f#.,c.,12p,d#.,d.,d#.,f.,g.,g.,g.,g.,g.,g.,2g.
South Park:d=8,o=5,b=125:e,e,e,16e,e,16e,p,e,e,e,e,e,16p,16e,e,2p,g,g,4g,16b,16b,b,e,a#,16g,16g,g,16f#,16f#,f#,e
Spiderman:d=4,o=6,b=200:c,8d#,g.,p,f#,8d#,c.,p,c,8d#,g,8g#,g,f#,8d#,c.,p,f,8g#,c.7,p,a#,8g#,f.,p,c,8d#,g.,p,f#,8d#,c,p,8g#,2g,p,8f#,f#,8d#,f,8d#,2c
Star Trek:d=16,o=5,b=63:8f.,a#,4d#.6,8d6,a#.,g.,c.6,4f6
Star Wars:d=8,o=6,b=180:f5,f5,f5,2a#5.,2f.,d#,d,c,2a#.,4f.,d#,d,c,2a#.,4f.,d#,d,d#,2c,4p,f5,f5,f5,2a#5.,2f.,d#,d,c,2a#.,4f.,d#,d,c,2a#.,4f.,d#,d,d#,2c
Super Man:d=8,o=6,b=180:g5,g5,g5,4c,c,2g,p,g,a.,16g,f,1g,p,g5,g5,g5,4c,c,2g,p,g,a.,16g,f,a,2g.,4p,c,c,c,2b.,4g.,c,c,c,2b.,4g.,c,c,c,b,a,b,2c7,c,c,c,c,c,2c.
Sweeney:d=8,o=6,b=125:16a5,c,4a5.,4p.,16a5,e,2d,4p.,p,4c,c,16a5.,c,4e.,d,16a5,4c,d,16a5,c,4a5.,4p.,16a5,e,2d,4p.,p,4e,e,16d#.,e,4f.,4c,4b5,4a5,2f.,4c,g,1f
Take On Me:d=8,o=5,b=160:f#,f#,f#,d,p,b4,p,e,p,e,p,e,g#,g#,a,b,a,a,a,e,p,d,p,f#,p,f#,p,f#,e,e,f#,e,f#,f#,f#,d,p,b4,p,e,p,e,p,e,g#,g#,a,b,a,a,a,e,p,d,p,f#,p,f#,p,f#,e,e5
Tarzan:d=8,o=5,b=120:e,f,g,16c6,g,16c6,16g,16c6,g,4d6,g,g.,4c6,4p,f,g,a,16c6,a,16c6,16a,16c6,a,4d6,g,g.,4c6,4p,e,f,g,16c6,g,16c6,16g,16c6,g,4d6,g,g.,4c6,4p,f,g,a,16c6,a,16c6,16a,16c6,a,4d6,g,g.,4c6.
Teenage Dirt Bag:d=4,o=5,b=200:d#6,e6,g#6,g#6,2f#6,2e6,2g#6,2d#6,2d#6,2e6,d#6,e6,g#6,g#6,2f#6,2e6,2g#6,2d#6,2d#6,2e6,2e6,g#6,g#6,2f#6,2e6,2g#6,2d#6,2d#6,e6,2d#6,2e6
Teenage Turtles:d=8,o=6,b=100:g5,a5,g5,a5,g5,16a5,g.5,a5,a#5,c,a#5,c,a#5,16c,a#.5,c,d#,f,d#,f,d#,16f,d#.,f,16c,16c,16c,16c,a#5,4c,16c7,16c7,16c7
Tele Tubbies:d=4,o=5,b=125:16g.,p,16g,e,4g.,p,4a,2f.,16g.,p,16g,e,4g.,p,2d.,16g.,p,16g,e,4g.,p,4a,2f.,2g,2b,2c.6.
Thankyou:d=4,o=5,b=180:e6,e6,e6,8f6,d6,c6,d.6,p,8p,8b,c6,e6,b,8e6,a.,p,e6,e6,e6,8f6,d6,c6,d.6,p,8p,g6,a6,e6,8d6,e6,p,g6,g6,g6,8e6,d6,c6,e6,d6,p,8c6,8d6,e6,8f6,e6,d6,e6
The A Team:d=8,o=5,b=132:4d#6,a#,2d#6,16p,g#,4a#,4d#.,p,16g,16a#,d#6,a#,f6,2d#6,16p,c#.6,16c6,16a#,g#.,2a#.
Thomas The Tank:d=8,o=7,b=250:c,p,d,p,e,p,2f,4g,2a,2c#,4a5,4p,4a5,4p,4a5,4p,16c#,d.,4a#6,4d,4c,4p,4c6,4p,4c6,16c#,d.,4a#6,4a#6,d,4c,4c6,b6,c,b6,c,p,4c.,p,4c,4c6,4c6,p,b6,c,b6,c,p,4c#.,p,4c#,4c#6,4c#6,4g#6,4a#6,4b6,4c,4g#6,4d#,4d#6,4a#6,4c6,4c,4d#6,2c#,4c#6,4p,4c#6,4c#,4c,4b6,a#6,a#5,a#6,p,c#,a#5,c#,p,f#,a#5,f#,4a#.,4a#6,g#6,c#6,g#6,p,c#,c#6,c#,p,f,c#6,f,4g#.,4g#6,f#6,d#6,f#6,p,a#6,d#6,a#6,p,d#,d#6,d#,4f#.,4p,16e,f.,p,4f,c#,d#,p,4c#,4p,4c#6
Thunder Birds:d=8,o=4,b=125:g#5,16f5,16g#5,4a#5,p,16d#5,16f5,g#5,a#5,d#6,16f6,16c6,d#6,f6,2a#5,g#5,16f5,16g#5,4a#5,p,16d#5,16f5,g#5,a#5,d#6,16f6,16c6,d#6,f6,2g6,g6,16a6,16e6,4g6,p,16e6,16d6,c6,b5,a.5,16b5,c6,e6,2d6,d#6,16f6,16c6,4d#6,p,16c6,16a#5,g#5,g5,f.5,16g5,g#5,a#5,c6,a#5,g5,d#5
Tigger:d=8,o=5,b=200:d#,d,d,d,d,c,d,d#,2d#,d#,d,d,d,d,c,d,4d#.,4p,d#,4d,d,d,c,d,d#,2d#,d#,d,d,d,d,c,d,4d#.,4p,d#,4g#,g#,4g,g,4g#,g#,4g,g,f.,g.,a.,f.,4a#.,2p,d#,d#,d#,f,f,f,g,g,g,g#,g#,g#,4a#,g#,4g,f,4d#,2p
Time to say good bye:d=16,o=5,b=80:8c,d,e,d,e,f#,g,f#,g,a,g,e,a,b,4c6,4b
Titanic:d=8,o=6,b=120:c,d,2e.,d,c,d,g,2g,f,e,4c,2a5,g5,f5,16d5,16e5,2d5,p,c,d,2e.,d,c,d,g,2g,e,g,2a,2g,16d,16e,2d.
To The Dump To The Dump To The Dump Dump Dump:d=8,o=5,b=270:c,c,4c,c,c,4c,c,c,f,p,g,p,4a,c,c,4c,c,c,4c,a,a,g,p,e,p,4c,c,c,4c,c,c,4c,c,c,f,p,g,p,4a,f,a,1c6,a,g,f,p,a.,p,f
Toccata:d=16,o=5,b=160:a,g,1a,g,f,e,d,2c#,p,2d,2p,a,g,1a,8e.,4f,2c#,2d
Tones:d=8,o=5,b=500:b,16p,b,2p,g,16p,g,2p,d6,16p,d6,2p,d,16p,d.
Top Cat:d=16,o=5,b=125:8g,8c6,p,g,8c6,c6,8g,8c6,p,8c6,g,g,f#,g,g#,a,a#,b,8c6,8c6,p,g,4g,48g#.,48a.,48a#.,48b.,c6,p,c6,8c6,a,8b,a,8g,8c6,p,8c6,p,d#,8e,g,8a,c6,8p,c6,8c6,a,8b,a,8g
Transformers:d=16,o=6,b=285:e7,f7,e7,d#7,4d7,4p,d,d,d,d,d,d,d,d,e,e,e,e,f,f,f,f,f,f,f,f,8a7,8a#7,8a7,8p,4d7,2p,d,d7,d,d7,d,d7,d,d7,e,e7,e,e7,f,f7,f,f7,f,f7,f,f7,a5,a5,a5,a5,a#5,a#,a#5,a#,a#5,a#,a#5,a#,a#5,a#,a#5,a#,4p,8d,8p,4e,4f,4p,4f,4p,2g,4a,4a#,4p,g,g7,g,g7,g,g7,g,g7,4e,4g,4a,4p,f,f7,f,f7,f,f7,f,f7,4e,4f,4g,4p,e,e7,e,e7,e,e7,e,e7,e,e7,e,e7,4p,4d,4c#,8e,8p,4d,2d,d,d7,d,d7,d,d7,d,d7
Trim Phone:d=16,o=5,b=350:a,b,a,b,a,b,a,4p,a,b,a,b,a,b,a,b,a.
Tubular Bells:d=4,o=5,b=280:c6,f6,c6,g6,c6,d#6,f6,c6,g#6,c6,a#6,c6,g6,g#6,c6,g6,c6,f6,c6,g6,c6,d#6,f6,c6,g#6,c6,a#6,c6,g6,g#6,c6,g6,c6,f6,c6,g6,c6,d#6,f6,c6,g#6,c6,a#6,c6,g6,g#6,c6,g6,c6,f6,c6,g6,c6,d#6,f6,c6,g#6,c6,a#6,c6,g6,g#6
Under the Sea:d=4,o=6,b=200:8d,8f,8a#,d7,d7,8a#,c7,d#7,d7,a#,8a#5,8d,8f,a#,a#,8c,a,c7,a#,p,8d,8f,8a#,d7,d7,8a#,c7,d#7,d7,a#,8a#5,8d,8f,a#,a#,8c,a,c7,16a#,16d,16a#,16d,16a#,16d,16a#
USA National Anthem:d=8,o=5,b=120:e.,d,4c,4e,4g,4c6.,p,e6.,d6,4c6,4e,4f#,4g.,p,4g,4e6.,d6,4c6,2b,a,4b,c6.,16p,4c6,4g,4e,32p,4c
Van Halen-Eruption:d=32,o=5,b=120:c#6,16c#,e,g#,16c#,e,g#,16c#,e,g#,16c#,e,c#6,16c#,e,g#,16c#,e,g#,16c#,e,g#,16c#,e,a,16c#,e,a,16c#,e,a,16c#,e,a,16c#,e,a,16c#,e,a,16c#,e,a,16c#,e,a,16c#,d#,a,16d#,f#,a,16d#,f#,a,16d#,f#,a,16d#,f#,a,16d#,f#,a,16d#,f#,b,16d#,f#,b,16d#,f#,b,16e,g#,b,16e,g#,b,16e,g#,b,16e,g#,b,16e,g#,b,16e,g#,b,16e,g#,b,16e,g#,c6,16e,g,b,16e,g,b,16e,g,b,16e,g,b,16e,g,b,16e,g,d6,16e,g,d6,16e,f#,d6,16f#,a,d6,16f#,a,d6,16f#,a,d6,16f#,a,d6,16f#,a,d6,16f#,a,e6,16f#,a,e6,16f#,a,e6,16b,g#,e6,16b,g#,e6,16b,g#,e6,16b,g#,e6,16b,g#,e6,b,16g#,e6,b,16g#,e6,b,16g#,e6,16g#.,e6,g#,16b,e6,16b.,e6,b,16d6,e6,a#,16c#6,e6,a#,16c#6,e6,a,16c6,e6,a,16c6,e6,g#,16b,e6,g#,b,d6,e6,b,16d6,e6,b,16d6,e6,a#,16c#6,e6,a#,16c#6,e6,a,16c6,e6,a,16c6,e6,g#,16b,e6,g#,16b,d6,a,16c6,d6,a,16c6,d6,g#,16b,d6,g#,16b,d6,g,16a#,d6,g,16a#,d6,f#,a,16d6,f#,a,16c6,g,16a#,c6,g,16a#,c6,f#,16a,c6,f#,16a,c6,f,16g#,c6,f,16g#,c6,e,16g,c6,e,16g,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,e,16g,b,e,16g,b,e,16g,b,e,16g,b,e,16g,b,e,16g,b,e,16g,b,e,16g,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,e,16g,b,d#,16f#,b,4e,4a#4,4e.3
Vanessa Mae:d=16,o=5,b=140:c6,b,8c6,g,p,g,p,d#,p,d#,p,c,p,c,p,c6,b,8c6,g#,p,g#,p,f,p,8f,c,p,c,p,c6,b,8c6,g,p,g,p,d#,p,d#,p,c,p,c,p,g,f,d#,d,c,d,d#,c,d#,f,8g,8p,8d6,c6,d6,a#,d6,a,d6,g,d6,d6,p,d6,p,d6,p,8d6,c6,d6,a#,d6,a,d6,g,d6,d6,p,d6,p,d6,p,g,f,d#,d,c,d,d#,c,d#,f,4c.
Verve:d=8,o=5,b=80:b4,d,b4,c,a4,c,p,f,c,f,p,e,c,e,p,b4,d,b4,c,a4,c,p,f,c,f,p,e,c,e
Walk of Life:d=8,o=5,b=160:4g.,32p,4g,4p.,d,e,4g,e,4d,4c.,4c,2p,d,e,4g.,4g,4p.,d,e,4g,e,4d,4c.,4c
Waltons:d=4,o=5,b=120:8d,8d,g,a,b,1b.,2p,8d,8d,g,a,b,2b,1c#.6,8a,8a,e6,d6,c#6,2d.6,1a,p,8a,8a,a,b.,8c6,1b.,2p,8d,8d,g,a,b,1b.,2p,8d,8d,g,a,b,2b,1c#.6,8a,8a,e6,d6,c#6,2d.6,1a,p,8a,8a,a,b.,8a,1g.,2p,a,2b,d6,2e.6,2f.6,2g6,8e6,8e6,g6,f6,e6,1d.6,2p,8d6,8d6,f6,e6,d6,1a.,2p,8a,8b,c6,d6,c6,1b.,2p,a,2b,d6,2e.6,2f.6,2g.6,g6,f#6,e6,2g.6,1d6,p,8d6,8d6,g6,f6,e6,1c.6,2p,8a,8a,d6,c6,b,1g.,2p,8d,8d,g,a,b,1b.,2p,8d,8d,g,a,b,2b,1c#.6,8a,8a,e6,d6,c#6,2d.6,1a,p,8a,8a,a,b.,8a,1g..
Wannabe:d=8,o=5,b=125:16g,16g,16g,16g,g,a,g,e,p,16c,16d,16c,d,d,c,4e,4p,g,g,g,a,g,e,p,4c6,c6,b,g,a,16b,16a,4g
We Wish you a Merry Christmas:d=8,o=5,b=140:4d,4g,g,a,g,f#,4e,4c,4e,4a,a,b,a,g,4f#,4d,4f#,4b,b,c6,b,a,4g,4e,4d,4e,4a,4f#,2g
While Shepards Watch:d=16,o=5,b=120:4a,8p,32p,a,p,8g.,32p,4f,8a#.,p,8a#.,p,8a.,p,4g,32p,8a.,32p,8c.6,p,32p,8c.6,p,8b,8p,2c.6,4a,4p,8p,c.6,32p,4a#,8a.,32p,4g,32p,8f.,32p,4e,4a,4g,32p,8f.,p,8f.,p,8e.,p,2f.
Winne the pooh:d=4,o=5,b=125:8e,16d,e,d,p,8e,16d,e,d,p,8c,16c,8a#,16a#,8a,16a,g,f,e,d,d#,8e,16d,e,d,p,8e,16d,e,d,p,8c,16c,8a#,16a#,8a,16a,g,2f
Wolf Whistle:d=16,o=5,b=900:8a4,a#4,b4,c,c#,d,d#,e,f,f#,g,g#,a,a#,b,c6,8c#6,d6,d#6,e6,f6,4p,4p,a4,a#4,b4,c,c#,d,d#,e,f,f#,g,g#,a,a#,b,a#,a,g#,g,f#,f,e,d#,d,c#,c,b4,a#4,a4
Wombles:d=8,o=5,b=100:c,16d,f,16p,f,16d,c,16p,c,16d,f,4a,p,16a,a#,16a,g,a,16g,f,g,16d,f,4e,p,c,16d,f,16p,f,16d,c,16p,c,16d,f,4a,p,a#,16a,g,a,16g,f,g,16d,f
YMCA:d=8,o=5,b=160:c#6,a#,2p,a#,g#,f#,g#,a#,4c#6,a#,4c#6,d#6,a#,2p,a#,g#,f#,g#,a#,4c#6,a#,4c#6,d#6,b,2p,b,a#,g#,a#,b,4d#6,f#6,4d#6,4f.6,4d#.6,4c#.6,4b.,4a#,4g#
Zorba (Give it time!):d=16,o=5,b=125:16c#6,2d6,2p,c#6,2d6,2p,32e6,32d6,32c#6,2d6,2p,c#6,2d6,2p,b,2c6,2p,32d6,32c6,32b,2c6,2p,a#,2b,4p,8p,32c6,32b,32a,32g,32b,2a,2p,32a,32g,32f#,32a,1g,1p,8c#6,8d6,8d6,8d6,8d6,8d6,8d6,8d6,8c#6,8d6,8d6,8d6,8d6,8d6,e6,d6,c#6,e6,8c#6,8d6,8d6,8d6,8d6,8d6,8d6,8d6,8c#6,8d6,8d6,8d6,8d6,8d6,e6,d6,c#6,e6,8b,8c6,8c6,8c6,8c6,8c6,8c6,8c6,8b,8c6,8c6,8c6,8c6,8c6,d6,c6,b5,d6,8b,8c6,8c6,8c6,8c6,8c6,8c6,8c6,8b,8c6,8c6,8c6,8c6,8c6,8c6,8c6,c#6.,d6.,d6.,d6.,d6.,d6.,d6.,d6.,c#6.,d6.,d6.,d6.,d6.,d6.,32e6.,32d6.,32c#6.,32e6.,c#6.,d6.,d6.,d6.,d6.,d6.,d6.,d6.,c#6.,d6.,d6.,d6.,d6.,d6.,32e6.,32d6.,32c#6.,32e6.,b.,c6.,c6.,c6.,c6.,c6.,c6.,c6.,b.,c6.,c6.,c6.,c6.,c6.,32d6.,32c6.,32b5.,32d6.,b.,c6.,c6.,c6.,c6.,c6.,c6.,c6.,b.,c6.,c6.,c6.,c6.,c6.,c6.,c6.,

```
