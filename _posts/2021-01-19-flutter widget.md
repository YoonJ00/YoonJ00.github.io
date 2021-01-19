플루터에서 위젯이란?<br>
: 화면을 구성하는 컴포넌트, 위젯의 조합으로 UI가 구성되기 마련.<br>
기본적으로 플루터는 Material 디자인을 표준 디자인으로 채용하지만 iOS의 Cupertino<br>
디자인 또한 사용 가능하다. 주요 임무는 빌드 구현.
![image](https://user-images.githubusercontent.com/59801728/104978892-4793a100-5a46-11eb-84e0-7100238fdcda.png)
<br><br>

플루터의 화면 구성<br>
: 
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
<b>MaterialApp > Scaffold > Center > Text</b>

레이아웃을 구성하는 MaterialApp, Scaffold 위젯, material 다지인의 구성을 잡아준다.
<br><br>

플루서의 위젯 트리<br>
: <b>Widget</b>:  속성에 대한 정보를 포함한다.<br>
<b>Element</b>: 부모, 자식 관계 생명주기 관여(위젯의 생성을 파괴)한다.<br>
<b>Render Object</b>: 크기와 레이아웃을 결정한다.