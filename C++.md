일단 나는 C++은 다른 언어랑은 다르게 visual studio 2019 version을 사용한다.
근데 이게 잘보면 solution안에(프로젝트를 만들어야 된다ㅠㅠ) 외부 종속성,리소스파일(내가 봤을 때 C++/C를 컴파일 하기 위한 제공 수단으로 보인다), 소스파일, 헤더파일로 
이루어져있어서 좀 복잡하다ㅠㅠㅠㅠ

:heart:     
디버깅 / 디버그하지 않고 시작
그냥 디버그하면 출력을 볼 수 없고 끝나버릴 수도 있다..ㅠㅠ

:heart:   
프로젝트 안에 cpp 두개 !
이럴 땐 내가 기존에 만들어놓았던 것을 '프로젝트에서 제외' 시켜야 한다. 
그리고 main함수는 무조건 하나여야 한다!!

:heart:   
형식 지정자가 없습니다.int로 가정합니다.
이때는 int main(){} 으로 함수 이름을 바꿔준다.

:heart:
int main()에서 main에 초록색 줄 생기면서
경고    C6262    함수에서 '40000'바이트의 스택을 사용하는데 이 크기가 /analyze:stacksize '16384'을(를) 초과합니다. 일부 데이터를 힙으로 이동하십시오   
배열크기를 너무 크게 하면 스택이 넘쳐서 오류가 난다. 배열을 전역변수로 선언하면 오류 없어짐.. -> 자료구조 공부 이후 더 생각해보자!!
