# 웹 브라우저의 통신과정

브라우저의 주요 기능은 사용자가 선택한 자원을 서버에 요청하고 브라우저에 표시하는 것이다. 브라우저는 HTML과 CSS 명세에 따라 HTML 파일을 해석해서 표시하는데 이 명세는 웹 표준화 기구인 W3C에서 정한다.

사용자가 브라우저의 주소 표시줄에 도메인을 입력하고 Enter를 누른다.

도메인에 대한 요청은 일반적으로 케이블 인터넷 공급업체, DSL 광대역 공급업체 또는 기업 네트워크 같은 인터넷 서비스 제공업체(ISP)가 관리하는 DNS 해석기로 라우팅된다. DNS 해석기가 사용자에게 필요한 IP 주소를 확보하여 이 값을 웹 브라우저로 반환한다.

인터넷에 연결된 웹 브라우저 요청 패킷은 일반적으로 TCP/IP 프로토콜을 사용하여 라우터 장비, 인터넷 서비스 제공회사 교환기를 통해 이동되어, 통신 회사 간 경로인 라우팅 테이블을 따라서 연결할 IP 주소가 있는 웹 서버를 찾는다.

브라우저가 인터넷에서 서버를 찾으면 웹 서버와 TCP 연결을 설정하고, HTTP를 통해 평문 통신을 시작한다. HTTP 요청에는 요청 라인, 헤더(또는 요청에 대한 메타데이터) 및 본문이 포함된다.

웹 서버가 요청을 처리하고 응답을 브라우저로 전송하면 브라우저가 전송 받은 콘텐츠를 렌더링한다. 브라우저의 렌더링 엔진은 요청받은 내용을 브라우저 화면에 표시한다.

렌더링 엔진은 HTML 문서를 파싱하고 렌더 트리를 생성하고 정해진 순서대로 화면에 표시된다.

웹은 파싱이 실행되는 동시에 수행되는 동기화(synchronous) 모델이다. 스크립트(script)가 실행되는 동안 문서의 파싱은 중단된다. 스크립트를 "defer"로 표시할 수 있는데 이렇게 되면 문서 파싱은 중단되지 않고 파싱이 완료된 이후에 스크립트가 실행된다. 스타일 시트는 DOM 트리를 변경하지 않기 때문에 문서 파싱을 기다리거나 중단할 이유가 없다. 그러나 스크립트가 문서를 파싱하는 동안 스타일 정보를 요청하는 경우라면 문제가 된다. 따라서 script 태그의 위치에 따라 DOM의 생성이 지연될 수 있으므로 script 태그의 위치를 요소의 가장 아래에 위치시키는 것은 권장된다.

### IP 주소와 DNS
IP 주소(Internet Protocol address, IP address)는 컴퓨터 네트워크에서 장치들이 서로를 인식하고 통신을 하기 위해서 사용하는 특수한 번호이다. 이런 번호는 외우기 어렵기 때문에 DNS가 전화번호부 같은 역할을 한다.

### - 참고문서

"브라우저 동작 원리" poiemaweb, https://poiemaweb.com/js-browser, accessed: 2023년 4월 08일

"웹 브라우저에 URL을 입력하면 어떤 일이 생기나요?" aws.amazon, https://aws.amazon.com/ko/blogs/korea/what-happens-when-you-type-a-url-into-your-browser/, accessed: 2023년 4월 08일

"브라우저는 어떻게 동작하는가?" d2.naver, https://d2.naver.com/helloworld/59361, accessed: 2023년 4월 08일

"DNS란 무엇입니까?" aws.amazon, https://aws.amazon.com/ko/route53/what-is-dns/, accessed: 2023년 4월 08일

"도메인 네임 시스템" wikipedia, last modified: 2022년 2월 26일, https://ko.wikipedia.org/wiki/도메인_네임_시스템, accessed: 2023년 4월 08일


<Comment />