# Network

### [Q] HTTP 특징 및 장단점
[A]

특징 :  데이터를 주고 받기 위한 프로토콜으로, 서버와 클라이언트 모델을 따릅니다.

장점 :  서버 디자인이 간단하다는 점 입니다. 통신이나 상태정보를 따로 관리 할 필요가 없습니다.

단점: 매번 인증을 해줘야 합니다. 예로 쿠키나 세션이 있습니다.

<br>

### [Q] HTTP vs HTTPS
[A]


보안성을 강화시킨것이 https 입니다. 공개키/개인키 암호화 방식을 사용해서 데이터를 암호화 합니다.

<br>

### [Q] TCP vs UDP
[A]

tcp 는 연결형 서비스를 지향하는 프로토콜입니다. 호스트간 / 신뢰성있는/ 데이터흐름을 보장합니다.
udp는 비연결성 서비스를 지향하는 프로토콜입니다. 데이터를 보내는 쪽에서 일방적으로 데이터를 보냅니다.

속도가 빠르다는 장정이 있습니다.

<br>

### [Q] Cookie vs Session
[A]
쿠키는 : 클라이언트 로컬에 저장하는 키와 값으로 저장된 데이터 입니다. 인증 시간을 정할 수 있어 브라우저가 종료되도 데이터가 남아있다는 장점이 있습니다. 단점은 보안에 취약합니다.

세션은 :  로컬이 아닌 서버에 저장합니다. 세션 id를 부여해서 브라우저가 끝날때 까지 유지 시킵니다.


<br>

### [Q] 세션 기반 인증이란?
[A]

세션을 통해 사용자를 인증하고 상태를 유지하기 위해 서버측에 사용자 정보를 저장하는 방식입니다.

특징으로
세션 기반 인증은 클라이언트로부터 요청을 받으면 클라이언트의 상태 정보를 저장함으로 Stateful 한 구조를 가집니다.



<br>

### [Q] Token 기반 인증이란?
[A]

토큰을 통해 사용자 인증 및 권한 부여를 하는 방식으로, 사용자가 로그인 하면 서버에서 토큰을 발급하고 이 토큰을 사용하여 인증 및 접근 권한을 관리하는 인증 방식입니다.


<br>

### [Q] Token 기반 인증의 단점
[A]
 
토큰이 유출 될 수 있는 위험이 있습니다.
그러한 탈취를 예방하기 위한 방법으로는 
https를 사용하거나 토큰 만료시간 설정하거나, 토큰을 갱신하여 보안을 강화하는 방법이 있습니다.

<br>

### [Q] JWT란?
[A]

json 포맷을 이용하여 사용자에 대한 속성을 저장하는 web token을 jwt라고 부릅니다. 정보를 안전하게 전달하기 위해 사용합니다.
해더, 내용 , 서명 으로 구성됩니다.
헤더 : 에는 토큰의 타입과 해쉬 암호화 알고리즘으로 이루어저 있습니다.
내용 : 에는 사용자의 정보를 담습니다.key와 value 한 쌍으로 이뤄져 있습니다.
서명에는 : 유효성 검증에 필요한 암호화 코드가 잇씁니다. 헤더와 내용의 값을 인코딩 합니다.

<br>

### [Q] 트래픽 증가시 해결 방법
[A]

로드 밸런싱이나 캐싱 ,비동기 처리를 고려해볼 수 있습니다.
로드 밸런싱은 로드 밸런서를 사용하여 트래픽을 여러 서버 또는 리소스로 분산시킵니다. 이를 통해 단일 서버에 가해지는 부하를 분산합니다.
캐싱은 정적 콘텐츠 및 데이터를 캐싱해서 반복적인 요청에 대한 응답 시간을 줄입니다.
비동기 처리를 통해 블로킹작업을 최소화 하고 동시에 여러 요청을 처리 할 수 있도록 합니다.

<br>

### [Q] 로드 밸런싱이란?
[A]

네트워크 트래픽 또는 작업을 여러 서버로 균등하게 부낫ㄴ시켜 서버의 부하를 줄이고 가용성을 높히는 기술 입니다. 하드웨어나 소프트웨로 구현되며 , 클라우드 환경에서도 많이 활용됩니다.
<br>

### [Q] CORS (Cross Origin Resource Sharing)
[A]

자신이 서비스 하고 있지 않은 사이트에서 세션을 요청해 획득하기 위해서 , 허용된 origin들만 요청할 수 있도록 만들기 위해 cors 가 필요합니다.

<br>

### [Q] 공인 IP vs 사설 IP
[A]

 공인 IP는 전세계에서 고유하며 인터넷을 통해 접근할 수 있는 IP 주소로, 주로 웹 서버, 메일 서버 등과 같은 외부와 통신해야 하는 서버 또는 네트워크 장치에 할당됩니다.
 반면에 사설 IP는 비공개 네트워크 내에서 사용되며 인터넷에서 직접 접근할 수 없습니다. 주로 내부 네트워크에서 호스트와 장치 간 통신에 사용됩니다.

<br>

### [Q] OSI 7 layer와 각 계층
[A]
appication

presentation

session

transport

network

datalink

phtsical

7계층입니다.

a: 사용자가 네트워크에 접근할 수 있도록 도와줌

p:전송된 데이터의 인코딩 및 디코딩 진행

s: 네트워크 상 양쪽의 연결을 관리하고, 연결을 유지시켜줌

t: 데이터를 전송하거나, 그 데이터들을 합산해서 session 계층으로 보냄

n:  전송 데이터의 목적지까지 경로를 찾고 , 전송합니다.

d 물리적 네트워크 사이에 data 전송을 담당함

p: 0 과 1로 구분하는 비트스트림을 전송하는 계층입니다.


<br>

### [Q] Get vs Post 
[A]

get : 데이터를 조회하기 위한 방법으로, 헤더에 데이터를 추가해서 보내는 방식입니다.

post: 데이터를 추가 수정하기위한 방법으로 body에 추가해서 보내는 방식입니다.

<br>

### [Q] Restful API란?
[A]

웹을 통해 데이터를 (요청)하거나 (전송)하는 방법을 제공하는 (인터페이스)입니다.

웹 상에서의 자원을 표현하고, 그 자원의 상태정보를 얻는데 주로 사용됩니다.

<br>

### [Q] HTTP Method 종류
[A]
GET	데이터 조회
POST	요청 데이터 처리(보통 데이터 등록 사용)
PUT	데이터 변경 (해당 데이터가 없으면 생성)
PATCH	일부 데이터만 변경
DELETE	데이터 삭제

<br>

### [Q] Patch vs Put 
[A]
PUT	이랑 다르게 PATCH는	일부 데이터만 변경 합니다.
<br>

### [Q] 브라우저 동작 방식
[A]

 1. 웹 브라우저가 https://www.google.com/images/google.png로 이미지를 요청 해야 한 다는 것을 인지 한다.
    2. 웹 브라우저는 url을 이용해 서버의 ip를 추출한다.
    3. 이미지를 요청하기 위한 HTTP 메세지를 만든다.
    4. 메세지는 get메서드이고 /google.png를 요청하는 메세지이다.
    5. 웹브라우저는 서버와 TCP 컨넥션을 맺는다.
    6. 웹브라우저는 서버에 HTTP요청을 보낸다.
    7. 서버는 메세지를 받고 무슨 내용인지 해석한다. get이라는 메서드이고 /google.png라는 파일을 요청 했다는 것을 인지한다.
    8. 서버는 해당 리소스가 있는지 찾는다.
    9. 찾으면 상태코드가 200인 메세지와 함께 응답 메세지를 작성한다.
    10. 서버는 클라이언트와 TCP컨넥션을 맺는다.
    11. 서버는 클라이언트에 HTTP 응답을 보낸다.
    12. 커넥션이 닫히면 웹브라우저는 사용자에게 이미지를 보여준다.

<br>

### [Q] HTTP status code
[A]

웹 서버가 클라이언트에게 보내는 HTTP 요청에 대한 응답의 상태를 나타내는 3자리 숫자입니다. 

예를 들어, 200번대 코드는 성공을 나타내고, 
400번대 코드는 클라이언트 오류를, 
500번대 코드는 서버 오류를 나타냅니다. 

<br>

### [Q] Web Server vs WAS (Web Application Server)
[A]

web server: 는 정적인 데이터를 처리합니다.이미지나 단순 html을 여는데 사용됩니다.

was는 : 동적인 데이터를 처리합니다. db 연결이나 데이터 조작이 필요한 경우 was를 사용합니다. 

jsp 나 servlet와 같은 것을 실행하기 위해 사용됩니다.

<br>

### [Q] IPv4 vs IPv6
[A]

. IPv4는 32비트 주소 체계를 사용하며, 한정된 주소 공간과 주소 고갈 문제가 있습니다. 
. IPv6는 128비트 주소 체계를 사용하며, 큰 주소 공간을 제공하여 주소 고갈 문제를 해결하고 미래의 인터넷 확장을 지원합니다

<br>
