# HTTP

HTTP는 분산, 협업, 하이퍼미디어 정보 시스템을 위한 인터넷 프로토콜 스위트의 응용 계층 프로토콜이다. HTTP는 짧은 대기 시간 요청을 위한 간단한 메커니즘으로 시작되었다.

HTTP는 월드 와이드 웹 아키텍쳐용으로 만들어졌으며 전 세계 하이퍼텍스트 시스템의 확장성 요구 사항을 지원하기 위해 시간이 지남에 따라 발전했다.

HTTP 요청의 대상을 "리소스"라고 한다. HTTP는 리소스의 특성을 제한하지 않고 리소스와 상호 작용하는 데 사용할 수 있는 인터페이스를 정의할 뿐이다. 요청 메소드와 몇 가지 요청 수정 헤더 필드(request-modifying header fields)에 요청 의미론(request semantics)을 부여하는 것으로 리소스의 식별을 분리할 수있다.

리소스는 요청 메서드의 의미 체계와 일치하지 않는 방식으로 요청을 처리할 수 없다. 리소스의 URI가 안전하지 않은 의미론(semantics)을 암시할 수 있지만 클라이언트는 안전한 메서드로 요청을 처리할 때 리소스가 안전하지 않은 작업을 피할 것으로 기대할 수 있다. 정의된 의미 체계가 기본적으로 읽기 전용인 경우 요청 메서드는 "안전한" 것으로 간주된다. 즉, 클라이언트는 대상 리소스에 안전한 방법을 적용한 결과로 인해 원본 서버에서 상태 변경을 요청하거나 기대하지 않는다. 안전한 방법을 합리적으로 사용하면 원본 서버에 피해, 재산 손실 또는 비정상적인 부담이 발생하지 않을 것으로 예상된다.

해당 메서드를 사용하는 여러 개의 동일한 요청이 서버에 미치는 효과가 단일 요청에 대한 효과와 동일한 경우 요청 메서드는 "멱등성"으로 간주된다. 클라이언트가 서버의 응답을 읽을 수 있기 전에 통신 실패가 발생하면 요청이 자동으로 반복될 수 있기 때문에 멱등 메서드가 구별된다. 클라이언트는 메서드에 관계없이 요청 시맨틱이 실제로 멱등적이라는 것을 알 수 있는 수단이 없거나 원래 요청이 적용되지 않았음을 감지할 수 있는 수단이 없는 한 비 멱등적 메서드로 요청을 자동으로 재시도해서는 안된다.

### - 참고문서

"HTTP" wikipedia, last modified: 2023년 4월 20일, https://en.wikipedia.org/wiki/HTTP accessed: 2023년 4월 25일

"RFC 9110" IETF Datatracker, https://datatracker.ietf.org/doc/html/rfc9110#name-purpose accessed: 2023년 4월 25일

<Comment />