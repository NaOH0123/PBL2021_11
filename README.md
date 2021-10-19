#PBL2021_11

from picamera import PiCamera
from time import sleep
import time

camera=PiCamera()

t = time.time()
print('start')
while True:
    c = time.time()
    if c - t >= 10:
        print('camera start')
        camera.start_preview()
        print('camera start OK')
        sleep(5)
        camera.capture('/home/pi/Desktop/image.jpg')
        print('camera Stop')
        camera.stop_preview()
        print('camera Stop OK')
        break
print('end')
