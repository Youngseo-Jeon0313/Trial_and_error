일단 mongodb의 cluster를 깔고 연결을 해줘야 한다. 이 때 network access가 되고 있어야 함을 잊지 말자ㅠㅠ
나는0.0.0.0/0  (includes your current IP address)로 해줬는데 이게 개발(development)시에는 괜찮지만 배포 시에는 굉장히 안됨

:sparkles:   
스키마 만든 후에 꼭 서버 실행하는 곳에 require해주기ㅠㅠㅠ   
스키마 만들 때 굳이 id 칸 안 만들어도 자동 생성되니까 걱정하지 않아도 됨!
    
   
아무래도 html로 client가 crud 한 내용을 server로 그대로 받으려면.. html port번호가 같아야 한다.. 근데 나는 port가 이미 실행중이라는 에러를 받았는데ㅠㅠㅠ 이걸 극복하려면 cors를 써야하나..??ㅜㅜㅜ
