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
: 아두이노에서 LED를 컨트롤하기 위해서 <b>pinMode(), digitalWrite(), delay() 함수가 사용된다.
