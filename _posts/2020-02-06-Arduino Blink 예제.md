LED
: ![다이오드](https://user-images.githubusercontent.com/59801728/73821630-b2e56280-4837-11ea-89d0-20ecd700a3c5.PNG)<br>
LED는 전기에너지를 빛 에너지로 변환한 발광 다이오드이다.<br>
LED는 단자 마다 극성을 가지고 있어 +, - 를 구분하여 사용해야 한다.<br>
+를 애노드 -를 캐소드 라고 부른다.<br><br>
![다이오드 설명](https://user-images.githubusercontent.com/59801728/73821628-b1b43580-4837-11ea-99ec-c4ec3ee6323e.PNG)<br>
LEDL에서 극성의 구분은 긴 다리가 +, 짧은 다리가 -이다.


저항 (Resistor)
: ![저항](https://user-images.githubusercontent.com/59801728/73821761-fd66df00-4837-11ea-9a7a-c2e01cbba7ce.PNG)<br>
저항은 말 그대로 전기의 흐름을 방해하는 부품이다.<br>
저항을 사용하여 회로의 전류 또는 전압의 크기를 바꿀 수 있다.<br><br>
아두이노에서 LEDL를 사용하기 위해서는 저항을 같이 사용해야 한다. LED는 필요 전압과 소모 전류가 있다. LED에 따라 조금 다르지만 보통 아두이노에서 사용되는 LED의 필요 전압은 2V이며, 소모 전류는 10mA 정도 된다. 아두이노 우노보드의 공급 전압이 5V이기 때문에 저항 없이 LED를 사용하여 LED에 손상을 줄 수 있다.<br><br>
적정 저항 값을 계산하는 방법은 옴의 법칙 (V=IR)을 이용하면 된다.<br>
R (필요 저항) = 5V(공급 전압) - 2V(LED 필요 전압) / 10mA(LED 소모 전류) = 300Ω<br>
아두이노에서는 300Ω의 저항을 사용하면 되고 300Ω 저항이 없을 경우 근사치 저항을 사용 하면 된다. 보통 330Ω 저항을 많이 사용한다.


LED 회로 구성하기
: ![LED 회로 구성](https://user-images.githubusercontent.com/59801728/73822217-f391ab80-4838-11ea-9768-4f62f4eaf54f.PNG)<br>


아두이노 함수 알아보기
: 아두이노에서 LED를 컨트롤하기 위해서 <b>pinMode(), digitalWrite(), delay()</b>함수가 사용된다.

pinMode()
: 디지털 핀의 모드를 OUTPUT(출력) 또는 INPUT(입력)으로 설정하는 함수이다.<br><br><br>
<b>-구조</b><br>
pinMode(핀 번호, 모드)<br>
여기서 핀 번호와 모드를 매개변수 또는 인자라고 한다.<br><br>
<b>-매개변수 (인자)</b><br>
핀번호 : 모드를 설정하고자 하는 핀 번호 / 센서가 연결된 핀 번호<br>
모드 : 출력인 경우 OUTPUT, 입력인 경우 INPUT을 입력<br><br>
<b>-사용 예</b><br>
pinMode(13, OUTPUT); //13번 핀을 출력 모드로 설정<br>
pinMode(13, INPUT); //13번 핀을 입력 모드로 설정


digitalWrite()
: 디지털 핀의 전압을 HIGH 또는 LOW로 설정하는 함수이다.<br><br><br>
<b>-구조</b><br>
digitalWrite(핀 번호, 전압)<br>
여기서 핀 번호와 전압을 매개변수 또는 인자라고 한다.<br><br>
<b>-매개변수 (인자)</b><br>
핀번호 : 모드를 설정하고자 하는 핀 번호 / 센서가 연결된 핀 번호<br>
전압 : HIGH 또는 LOW<br><br>
<b>-사용 예</b><br>
digitalWrite(13, HIGH); //13번 핀의 전압을 HIGH로 설정한다.<br>
digitalWrite(13, LOW); //13번 핀의 전압을 LOW로 설전한다.


delay()
: 프로그램 실행을 일정 멈추는 함수<br><br><br>
<b>-구조</b><br>
delay(멈출 시간)<br>
여기서 멈출 시간을 매개변수 또는 인자라고 한다.<br><br>
<b>-매개변수 (인자)</b><br>
멈출 시간 : 단위는 밀리초(msec) 1msec = 0.001초 / 1초 = 1000msec<br><br>
<b>-사용 예</b><br>
delay(1000); //프로그램 실행을 1초 멈춘다.