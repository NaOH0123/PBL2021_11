#PBL2021_11

from picamera import PiCamera
from time import sleep

camera=PiCamera()

t = time.time()
print('start')
while True:
    c = time.time()
    if c - t >= 10:
        camera.start_preview()
        sleep(5)
        camera.capture('/home/pi/Desktop/image.jpg')
        camera.stop_preview()
        break
print('end')
