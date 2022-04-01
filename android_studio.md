##Gradle??
내게 주어진 오류는 다음과 같다.
==> Could not install Gradle distribution from 'https://services.gradle.org/distributions/gradle-5.4.1-all.zip'

일단 gradle이 뭘까..?? android studio에서 사용되는 gradle이라는 것은 일단 build system이라고 한다. 
내가 아는 build system은 이전에 react 프로젝트를 배포할 시 java 파일, css파일 등등의 것들을 다 한꺼번에 정리해서 압축하는 것이다.
gradle에 대해 막 뒤지다 보면 '플러그인'이라는 용어가 또 나오는데 이 단어 뜻은 추가 기능을 위한 컴퓨터 프로그램 모듈 또는 장치라고 이해하면 된다. 
쉽게 우리가 html에 들어가서 막 노래도 들을 수 있고, 영상도 볼 수 있지 않는가?? 이렇듯이 html에서 그 언어 안에서 할 수 있는 거 외에 다른 것을 불러와서
사용할 수 있도록 도와준다고 보면 된다..

암튼 일단 이 오류는 해결을 했는데, android studio의 특성상 일단 너무 까칠하다. 왜냐?? 일단 자기가 참조하는 파일들에 영어 외에 다른 글자나 특수문자가 있으면 용납을 못한다(하..)
그리고 외부에서 참조하는 것과 C(내 컴퓨터 사용) 사이에도 혼동이 조금 있는 것 같고ㅠㅠ
저 에러가 난 이유는 , 내가 원래 7.0.2 버전의 gradle을 사용하려고 했는데, 내가 가지고 있던 Java JDK가 일단 그 버전을 못 먹어서 그런 것 같고, 그래서 5.4.1로 해서 그냥 아예
오른쪽 위에 있는 gradle 다운 받는 버튼을 눌러서 그냥 내가 따로 zip파일 넣는 거 없이 해결했다... version에 이상이 있는 것은 생각을 못했어서 헤매고 헤매다가 찾은 것 같다

다음 오류는 
==> gradle sync failed: Cause: internal/modules/cjs/loader.js:888 throw err; ^Error: Cannot find module 'C:\Users\20wjs\OneDrive - 占쎈립�뤃占쏙옙鍮녷�⑤벉占쏙옙釉경뤃占�\computer\Health\HealthApp\node_modules\@react-native-community\cli\build\bin.js' at Function.Module._resolveFilename (internal/modules/cjs/loader.js:885:15) at Function.Module._load (internal/modules/cjs/loader.js:730:27) at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:72:12) at internal/main/run_main_module.js:17:47 { code: 'MODULE_NOT_FOUND', requireStack: []} (22 s 741 ms)

이따구의 겁나 긴 오륜데 아무래도 내 onedrive가 onedrive - 한국항공대학교 로 되어 있어가지고 이렇게 에러가 난 것 같다ㅠㅠㅠ 그냥 KAU로 하지 왜 자꾸 한글을 써가지고ㅠㅠㅠ 다음부터는
파일 이름이라던가 글 쓸 때 진짜 한글 절대 안 쓸거다 개빡친다..
암튼 저거 ONEDRIVE 자체 이름을 바꿀라면 일단 관리자 계정으로 ONEDRIVE에 들어가야 되는데 항공대 계정이 그게 안되는 것 같아서 그건 학교에 문의해야 한다고 한다.
(가끔 TEAMS에서 보면 나는 TEAMS 녹음버튼을 못 누르는 게 조금 이상했는데 그거랑 연관이 있는 것도 같다..) 암튼 내일 그래서 학교에 문의해볼라고 한다..!!

https://myaccount.microsoft.com/settingsandprivacy/privacy
https://docs.microsoft.com/ko-kr/microsoft-365/admin/add-users/assign-admin-roles?view=o365-worldwide

결국 너무 화나서 onedrive를 하나 더 사서 이름에 영어 외에 절대 들어가지 않게 만들었다.
근데 컴퓨터 속도가 늘어난 건 내 착각이겠지ㅠㅠ

근데 너무 android를 만져서 그런지 또 오류가 또 났다 또또 또그런다 또
NDK at C:\Users\20wjs\AppData\Local\Android\Sdk\ndk-bundle did not have a source.properties file
이건데.. 오류 해결 방법을 잘 찾아본 다음에 할 거다..
In my case I don't have ndk dir in the local.properties file and also didn't add ndk version in the build.gradle. I just simply deleted the ndk-bundle folder in the android sdk folder. and it worked.이 답변이 제일 맞는듯.. 낼 local.properties 파일을 한 번 보고 그 다음에 이제 해결할 예정이다

오류: unable to load script. make sure you're either running a metro server...
하 이거는 오류 찾아볼 때 살짝 실수할 뻔 했다.
build할 때랑 / 그냥 debug할 때를 살짝 헷갈려서 나락 갈뻔 했다ㅠㅠ
그리고 자꾸 react-native 명령어랑 yarn 명령어가 계속 안 돼서 왜 자꾸 안돼 이럤는데 알고보니까 npx react-native 라고 명령어를 치면 그냥 해결되는 문제였다...
생각보다 에러들에 대한 내용들이(react native라 그런건지) 한국어로 안 나와있어서 그냥 번역해서 영어로 쳤더니 외국인들이 더 잘 알려줬다... 너무 빡틴다..ㅠㅠ

만약에 환경변수/SDK를 변경한 후에도 적용이 안되었을 경우에 컴퓨터 재부팅을 시켜줘야 한다

오류: duplicate resources --- 확장자만 다른동일한 파일명이 있을 경우!
