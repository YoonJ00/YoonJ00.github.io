플루터에서 위젯이란?<br>
: 화면을 구성하는 컴포넌트, 위젯의 조합으로 UI가 구성되기 마련.<br>
기본적으로 플루터는 Material 디자인을 표준 디자인으로 채용하지만 iOS의 Cupertino<br>
디자인 또한 사용 가능하다. 주요 임무는 빌드 구현.
![image](https://user-images.githubusercontent.com/59801728/104978892-4793a100-5a46-11eb-84e0-7100238fdcda.png)
<br><br>

플루터의 화면 구성<br>
: <br>
-------------------------------------------------------------------------------------------------------<br>
```
void main() {
    runApp(
        MaterialApp(
            home: Scaffold(
                body: Center(
                    child: Text 'Hello'),
                ),
            ),
        ),
    );
}
```
<b>MaterialApp > Scaffold > Center > Text</b><br>
레이아웃을 구성하는 MaterialApp, Scaffold 위젯, material 다지인의 구성을 잡아준다.
<br><br>

플루터의 위젯 트리<br>
: <b>Widget</b>:  속성에 대한 정보를 포함한다.<br>
<b>Element</b>: 부모, 자식 관계 생명주기 관여(위젯의 생성을 파괴)한다.<br>
<b>Render Object</b>: 크기와 레이아웃을 결정한다.
<br><br>
before 버튼을 클릭하면 after로 바뀌게 하는 active.<br><br>
![image](https://user-images.githubusercontent.com/59801728/104985805-24bcb900-5a55-11eb-85b9-300c94a0fc53.png) canupdate()<br>

![image](https://user-images.githubusercontent.com/59801728/104985813-27b7a980-5a55-11eb-9cf1-ef61de04f35a.png) updateRenderObject()<br>

기본 위젯, Stateless/Stateful Widget<br>
:1. 기본 위젯 -> Container(기본 위젯, 속성이 다양하다.)<br>
Row/Column(수직/수평 방향으로 위젯들을 나란히 배치하는 위젯. children 프로퍼티 이용.)<br>
Stack(여러 위젯을 겹치게. children 프로퍼티 이용)<br><br> 2. Stateless Widget/Stateful Widget<br>
->상태를 가지지 않는 위젯. 변화에 무감각하다는 의미. 따라서 상태 변화를 감지하지 않기 때문에 화면을 구성할 때 최초 한 번만 build()함수를 호출한 뒤에 다시 호출하지 않는다. 이와 반대로 Stateful Widget은 어떤 위젯을 사용할지가 생각 후에 사용해야한다.
