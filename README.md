from gpiozero import LED #gpioero라이브러리에서 led클래스 가져오기
from time import sleep #time라이브러리에서 sleep함수 가져오기

carLedRed = 2
carLedYellow = 3
carLedGreen = 4
humanLedRed = 20
humanLedGreen = 21 #다양한 LED핀의 핀번호를 변수로 정의하기

carLedRed = LED(2)
carLedYellow = LED(3)
carLedGreen = LED(4)
humanLedRed = LED(20)
humanLedGreen = LED(21) #핀 번호를 활용하여 LED 객체를 생성하기

try:
    while 1: #무한루프 시작
        carLedRed.value = 0 #0:꺼짐 1:켜짐 
        carLedYellow.value = 0
        carLedGreen.value = 1
        humanLedRed.value = 1
        humanLedGreen.value = 0
        sleep(3.0) #작동하는 시간
        carLedRed.value = 0
        carLedYellow.value = 1
        carLedGreen.value = 0
        humanLedRed.value = 1
        humanLedGreen.value = 0
        sleep(1.0)
        carLedRed.value = 1
        carLedYellow.value = 0
        carLedGreen.value = 0
        humanLedRed.value = 0
        humanLedGreen.value = 1
        sleep(3.0)
    
except KeyboardInterrupt:
    pass #사용자가 CTRL C를 누르면 코드 실해 종료

carLedRed.value = 0
carLedYellow.value = 0
carLedGreen.value = 0
humanLedRed.value = 0
humanLedGreen.value = 0 #코드실행이 종료되면 모든 LED조명은 꺼진다# aiot-
