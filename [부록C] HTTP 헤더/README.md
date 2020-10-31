## HTTP 완벽가이드

### 🎧 헤더 레퍼런스
HTTP 에서 통신하기 위해 어떠한 헤더를 사용하고 있는지 알아보자

#### Accept
주로 클라이언트가 서버에게 바라는 것이 있을 때 사용하는 헤더들  
* `Accept` : 서버에게 자신이 받을 수 있는 Media Type을 선언하는 헤더, application/json
* `Accept-Charset` : 서버에게 자신이 받을 수 있는 어떤 문자 집합을 받아들이는지 명시하는 헤더, utf-8
* `Accept-Encoding` : 어떤 인코딩을 받아들일 수 있는지 명시하는 헤더, gzip
* `Accept-Language` : 어떤 언어를 받아들일 수 있는지 명시하는 헤더, en
* `Accept-Range` : 주어진 리소스에 대해 받아들일 수 있는 범위를 명시하는 헤더, 0-11 | bytes

#### Content
주로 클라이언트가 서버에게 요청하는 방식에 대해 설명하는 헤더들
* `Content-Type` : 메세지에 담긴 미디어타입을 명시하는 헤더, application/json
* `Content-Encoding` : 메세지에 어떤 인코딩이 적용되어 있는지 명시, gzip
* `Content-Language` : 어떤 언어로 작성했는지 명시하는 헤더, en
* `Content-Range` : 특정 범위를 전송해달라는 요청의 응답으로 사용하는 헤더, bytes 500-900 / 5400
* `Content-Length` : 메세지의 전체 길이나 크기를 명시하는 헤더, 2417
* `Content-Location` : 엔티티에 대응하는 URL을 전달하기 위해 사용하는 헤더, http://~~
* `Content-MD5` : 메세지 본문에 대해 무결성 검사를 제공하기 위한 헤더, md5-digest


#### 인증 및 쿠키
인증 또는 쿠키와 관련된 헤더들
* `Authorization` : 클라이언트가 자신을 인증하기 위해 서버로 전송하는 헤더, Bearer DEIDFJWEZX~,
* `Cache-Control` : 메세지를 어떻게 캐싱할건지 알려주는 헤더, no-cache
* `Cookie`, `Cookie2` : 클라이언트의 신원 추적을 위한 헤더
* `Expires` : 응답이 더 이상 유효하지 않게 되는 일시를 명시하는 헤더, Thu, 03 Oct 1997
* `WWW-Authenticate` : 인증 스킴을 이용한 인증요구를 하기 위해 사용하는 헤더


#### 기간 및 조건
주로 응답이나 요청의 기간이라는 제한이 있는 경우 관련된 헤더들
* `Age` : 응답에 대한 생성 후 경과된 시간을 정의(초), 60
* `If-Modified-Since` : 해당 시간 이후로 변경되어 있으면 액션을 취하라는 헤더
* `If-Match` : 해당하는 엔티티 태그가 있는지 조건 검색을 하기 위한 헤더
* `If-None-Match` : 해당 조건이 매치되지 않는 경우 액션을 취하기 위한 헤더
* `Date` : 메세지가 생성된 날짜와 시간을 알려주는 헤더
* `Last-Modified` : 해당 엔티티가 마지막으로 변경된 시간을 나타내는 헤더
* `Retry-After` : 해당 리소스에 대하여 다시 언제 시도할 수 있는지 명시하는 헤더


#### 프록시
Proxy와 관련된 헤더들
* `Proxy-Authenticate` : WWW-Authenticate의 Proxy 버젼
* `Proxy-Authorization` : Authorization의 Proxy 버젼
* `Proxy-Connection` : Connection의 Proxy 버젼

#### 그 외

* `User-Agent` : 클라이언트가 자신의 신원을 나타내기 위한 헤더
* `Transfer-Encoding` : 
* `Vary` : 어떤 헤더가 서버측과의 협상에서 사용되었는지 나타내는 헤더, User-Agent
* `ETag` : 메세지에 담겨있는 엔티티를 위한 엔티티 태그를 제공하는 헤더
* `Connection` : 해당 요청이 끝나면 어떻게 연결을 유지할 것인지 나타내는 헤더, keep-alive
* `Allow` : 어떠한 HTTP 메서드가 지원되는지 나타내는 헤더, GET
