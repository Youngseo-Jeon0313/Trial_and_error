일단 mongodb의 cluster를 깔고 연결을 해줘야 한다. 이 때 network access가 되고 있어야 함을 잊지 말자ㅠㅠ
나는0.0.0.0/0  (includes your current IP address)로 해줬는데 이게 개발(development)시에는 괜찮지만 배포 시에는 굉장히 안됨

:sparkles:   
스키마 만든 후에 꼭 서버 실행하는 곳에 require해주기ㅠㅠㅠ   
스키마 만들 때 굳이 id 칸 안 만들어도 자동 생성되니까 걱정하지 않아도 됨!
    
   
아무래도 html로 client가 crud 한 내용을 server로 그대로 받으려면.. html port번호가 같아야 한다.. 근데 나는 port가 이미 실행중이라는 에러를 받았는데ㅠㅠㅠ 이걸 극복하려면 cors를 써야하나..??ㅜㅜㅜ

404error -> server가 없어요ㅠㅠ 내가 server를 실행시키지도 않고 계속 거기에다가 보낼라고 그래서 나온 에러

:sparkles: :sparkles:    
data type error : cannot read property &#39;date&#39; of undefined
-> 결국 500 error 나옴
새 템플릿이 렌더링될 때 실행할 날짜-시간 선택기를 초기화를 시켜줘야 된다..? 라는 생각에서 일단 출발한다.   
일단 놀랍게도 이게 javascript / react 개발 시 제일 많이 보이는 에러라고 한다.   

여기서 알아야할 사실은 state가 비동기적이며 처음 렌더링(마운팅)하기도 전에 동작한다는 것이다. 이 때의 state는 정의되지 않았기 때문에 당연히 undefined다.
때문에 값을 읽을 수 없다는 에러가 출력되는 것이다.
   
해결방법?   
1. useState("") 이런식으로 useState안에 초기값을 알려준다. 타입은 다양할 수 있음. [] {} null(이건 모를 때) '' 가능
2. &&연산자와 조건문을 잘 사용하자. && 연산자를 사용하면 && 앞뒤로 false 값을 찾고, false가 없다면 뒤에 있는 값을 출력한다. 앞, 뒤 모두 true면 뒤에 있는 값을 출력해주는 원리이며 이를 응용하면 되겠다. 조건식에 false가 있는 경우 null이 되고 렌더링하지 않으며, 렌더링하지 않으니 오류도 출력되지 않는다.
3. console log에서 나는 에러는 if (data) 나 data? 를 이용해서 있냐 없냐고 물어보면서 가져오기
4. useRef 사용하기(리렌더링을 트리거하지 않음)
