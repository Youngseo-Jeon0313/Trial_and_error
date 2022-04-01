알고보니 yarn add가 npm install의 상위버전이라고 한다..(더 빨리 설치된다고)

<View>main page</View> 이런 어이없는 실수를 할 시 View안에 string안됑 라는 영어 오류 메시지가 뜬다. <Text>로 감싸야 한다!
그리고 typescript가 javascript 상위버전이라고 한다ㅠㅠㅠ
  
npm error 나와도 너무 당황하지 마라. . 아니 제발 읽어라ㅠㅠㅠ 그 버전 ^6.2.0 뭐 이런식으로 나오는 건 그냥 흘러보내면 된다고 한다!

v6.. 내가 다운로드받을 때 이런 버전 같은 거 잘 확인해야 하는 것 같다ㅠㅠ 그냥 무작정 인터넷에 나와있는 거 다운로드받지 말고 좀 생각을 하고 다운받자.

생각보다 android 와 ios가 조금 다른 게 있을 수 있다ㅠㅠ 확인하자!
  
그리고 내 컴 존나 느려서 파일에 좀 시간이 지나야 뜨는 경우가 있다... 다운로드받고 이게 생겼는지(?) 확인해보자!!

에러 중에 typescript ts, tsx 등등의 막 이런..
.native|.android.jsx|.native.jsx|.jsx|.android.js|.native.js|.js|.android.ts|.native.ts|.ts|.android.tsx|.native.tsx|.tsx|.android.json|.native.json|.json)
이거는 metro.config.js에서 그 호환식을 써줘야 된다ㅠㅠㅠ
  
component이름은 무조건 대문자로 시작해야 된다!!!!
  
navigate 를 쓰려는 거(onpress 함수가 실행되었을 때 navigation.navigate('')를 실행하게 하려면 그 함수의 파라미터로 {navigation}을 줘야함을 잊지말자!!!(경로 헷갈릴 수 있음 주의)
  
({}) 이거랑 {} 이거랑 {{}} 이거 어떤 거 써야 하는지 헷갈릴 수 이씅ㅁ 
