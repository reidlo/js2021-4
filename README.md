# 강준모 [201840103]

## [05월 25일]
>[13주차 05/25] 배운 내용 요약 <br>
1. <strong>Express Module - Web Server Module </strong>
- <strong>설치 및 이용</strong>
<ul>설치
<li>terminal에서 npm install express 입력</li>
<li>express의 description지정을 위한 초기화 작업 : npm init (-y) <- default 값</li>
※ npm init을 함으로써 express의 모듈 사용을 위해 필요한 package.json파일 생성<br>
</ul>

2. <strong> 기본 메소드 </strong>
<ul>
<li>express() : 서버 애플리케이션 객체 생성</li>
<li>app.use() : 요청이 왔을 때 실행할 함수 지정</li>
<li>app.listen() : 서버 실행</li>
</ul>

3. <strong>페이지 라우팅</strong>
- <strong>페이지 라우팅(page routing) : client 요청에 적절한 페이지를 제공하는 기술 </strong>
※ 페이지 라우팅 시 토큰 활용 : ':<토큰 이름>' 형태로 설정 / 토큰은 다른 문자열로 변환 입력 가능, request 객체의 params 속성으로 전달<br>
<ul>
<li>get(path,callback) : GET요청 발생시 이벤트 리스너 지정</li>
<li>post(path,callback) : POST요청 발생시 이벤트 리스너 지정</li>
<li>put(path,callback) : PUT요청 발생시 이벤트 리스너 지정</li>
<li>delete(path,callback) : DELETE요청 발생시 이벤트 리스너 지정</li>
<li>all(path,callback) : 모든 요청 발생시 이벤트 리스너 지정</li>
</ul>

4. <strong>response 객체</strong>
<ul>
<li>send() : 데이터 본문을 제공 <b>-가장 마지막에 실행하는 것이 원칙 / 중복실행 불가<b></li>
<li>status() : 상태 코드를 제공</li>
<li>set() : 헤더를 설정</li>
</ul>

5. <strong>Content-Type</strong>
- <strong>Server에서 Content-Type 제공 : 웹 브라우저는 헤더를 확인 / 제공된 데이터의 형태를 확인(MIME이라는 문자열로 제공)</strong>
<ul>
<li>text/plain : 기본적 텍스트</li>
<li>text/html : html 데이터를 의미</li>
<li>text/javascript : js 데이터를 의미</li>
<li>image/png : png 데이터를 의미</li>
<li>audio/mpe : MP3 음악 파일을 의미</li>
<li>video/mpeg : MPEG 비디오 파일을 의미</li>
<li>application/json : json 데이터를 의미</li>
<li>multipart/form-data : 입력 양식 데이터를 의미</li>
<p><b>※ MIME 형식 지정 : type() 메소드 사용</b></p>
</ul>

6. <strong>HTTP Status Code</strong>
- <strong>status code : 서버가 클라이언트에 '해당 경로는 이러한 상태'라고 알려주는 용도</strong>
<ul>
<li>1XX : 처리중 : 100 Continue</li>
<li>2XX : 성공 : 200 OK</li>
<li>3XX : Redirect : 300 Multiple Choices</li>
<li>4XX : Client Error : 400 Bad Request</li>
<li>5XX : Server Error : 400 Internal Server Error</li>
<p><b> ※Status Code 지정 : status() 메소드 사용</b></p>
</ul>

- <strong> Redirect : 3XX, 특수한 상태 코드 </strong>
<ul>
<li>웹 브라우저가 리다이렉트를 확인하면 화면을 출력하지 않음</li>
<li>응답 헤더에 있는 Location 속성을 확인해서 해당 위치로 이동</li>
<li>특정 경로로 웹 브라우저를 인도 할 때 사용</li>
<p><b>※ redirect()메소드를 사용</b></p>
</ul>

7. <strong>request 객체</strong>
- <strong> 주소 분석 </strong>
<ul>
<li>프로토콜 : 통신에 사용되는 규칙 : HTTP, HTTPS..etc</li>
<li>호스트 : 애플리케이션 서버의 위치 : (search)naver.com..etc</li>
<li>URL : 애플리케이션 서버 내부에서 라우트 위치 : search.naver..etc</li>
<li>요청 매개변수 : 추가적인 정보 : ?...=...&...=...(쿼리 문자열)</li>
</ul>

8. <strong>미들웨어</strong>
- <strong>미들웨어 설정 메소드 : use()</strong>

- <strong> 정적 파일 제공 - 웹 페이지에서 변경되지 않는 요소(이미지, 음악, js파일, css파일 등)를 쉽게 제공<br>→ app.use(express.static('파일경로'))</strong>
- <strong> morgan 미들웨어 - 사용할 수 있는 외부 모듈 확인 </strong>



## [05월 18일]
> [12주차 05/18] 배운 내용 요약 <br>
1. <strong>Node.js - ServerSiding JavaScript Program</strong>
- <strong>전역 변수/함수/객체 : 모든 곳에서 사용할 수 있는 것들</strong><br>
<ul>문자열 자료형의 전역 변수
<li>__filename : 현재 실행 중인 코드의 파일 경로를 나타냄</li>
<li>__dirname : 현재 실행 중인 코드의 폴더 경로를 나타냄</li>
</ul>

2. <strong>process 객체 : Node.js는 process 전역 객체를 제공</strong><br> 
※ process 객체는 프로세스 정보를 제공, 제어할 수 있게 하는 객체<br>
<ul><strong>1.process 객체의 속성</strong>
    <li>env : 컴퓨터 환경 정보를 나타냄</li>
    <li>version : Node.js 버전을 나타냄</li>
    <li>versions : Node.js와 종속된 프로그램 버전을 나타냄</li>
    <li>arch : 프로세서의 아키텍처를 나타냄</li>
    <li>platform : 플랫폼을 나타냄</li>
</ul>

<ul><strong>2.process 객체의 메소드</strong>
    <li>exit([exitCode =0]) : 프로그램 종료 </li>
    <li>memoryUsage() : 메모리 사용 정보 객체 리턴</li>
    <li>uptime() : 현재 프로그램이 실행된 시간을 리턴</li>
</ul>

<ul><strong>3.Node.js의 이벤트 연결 메소드</strong>
    <li>on(<이벤트 이름>, <이벤트 핸들러>) : 이벤트를 연결</li>
    <li>process 객체의 이벤트 : exit(프로세스 종료시 발생) / uncaughtException(예외가 일어날 시 발생)<li>
</ul>

<ul><strong>4.그 외 메소드</strong><br>
Event: 'exit'<br>
Event: 'uncaughtException'<br>
Signal Events<br>
process.stdout<br>
process.stderr<br>
process.stdin<br>
process.argv<br>
process.execPath<br>
process.execArgv<br>
process.abort()<br>
process.chdir(directory)<br>
process.cwd()<br>
process.env<br>
process.exit([code]) - code == 1이면 강제종료<br>
process.getgid()<br>
process.setgid(id)<br>
process.getuid()<br>
process.setuid(id)<br>
process.getgroups()<br>
process.setgroups(groups)<br>
process.initgroups(user, extra_group)<br>
process.version<br>
process.versions<br>
process.config<br>
process.kill(pid, [signal])<br>
process.pid<br>
process.title<br>
process.arch<br>
process.platform<br>
process.memoryUsage()<br>
process.nextTick(callback)<br>
process.maxTickDepth<br>
process.umask([mask])<br>
process.uptime()<br>
process.hrtime()<br>
process.on('이벤트 이름', () => {<br>
    함수 기능 <br>
}</ul><br>


3. <strong>os 모듈 사용 : const os = require('os');</strong>

<ul><b>- os모듈의 메소드</b>
    <li>hostname() : 운영체제의 호스트 이름 리턴</li>
    <li>type() : 운영체제의 이름을 리턴</li>
    <li>platform() : 운영체제의 플랫폼을 리턴</li>
    <li>arch() : 운영체제의 아키텍처를 리턴</li>
    <li>release() : 운영체제의 버전을 리턴</li>
    <li>uptime() : 운영체제가 실행된 시간을 리턴</li>
    <li>loadavg() : 로드 에버리지 정보를 담은 배열 리턴</li>
    <li>totalmem() : 시스템의 총 메모리를 리턴</li>
    <li>freemem() : 시스템의 사용 가능한 메모리를 리턴</li>
    <li>cpus() : CPU의 정보를 담은 객체를 리턴</li>
    <li>getNetworkInterfaces() : 네트워크 인터페이스의 정보를 담은 배열 리턴</li>
</ul>

4. <strong>url 모듈 사용 : const url = require('url');</strong>

<ul><b>- url 모듈의 메소드 </b>
    <li>parse(urlStr[.parseQuerystring=false,slashesDenoteHost=false]) : URL 문자열을 URL 객체로 변환해 리턴</li>
    <li>format(urlObj) : URL 객체를 URL 문자열로 변환해 리턴</li>
    <li>resolve(form,to) : 매개변수를 조합하여 완전한 URL 문자열을 생성해 리턴</li>
</ul>

5. <strong>File System 모듈 : const fs = require('fs');</strong>

<ul><b>- file system의 메소드</b>
    <li>fs.readFileSync(<파일 이름>) : 동기적으로 파일을 읽어들임</li>
    <li>fs.readFile(<파일 이름>, <콜백 함수>) : 비동기적으로 파일을 읽어들임</li>
    <li>fs.writeFileSync(<파일 이름>) : 동기적으로 파일 작성</li>
    <li>fs.writeFile(<파일 이름>,<문자열>,<콜백 함수>) : 비동기적으로 파일 작성</li>
</ul>

<ul><b>- 파일 처리와 예외 처리</b>
    <li>동기 코드 예외 처리 : try catch 구문 사용</li>
    <li>비동기 코드 예외 처리 : 콜백함수의 첫 번째 매개변수 error 사용</li>
    <strong> ※ fs.readFileSync()를 사용, 없는 파일을 지정해 강제 예외 발생</strong>
</ul>

<strong> ※ 동기와 비동기의 실행 결과는 같지만 내부 실행 구조는 다름</strong>

6. <strong>비동기 처리의 장점</strong>
<ul>
    <li>웹 서버를 C++로 제작하면 속도는 빠르지만, 개발과 유지보수가 난해</li>
    <li>프로그래밍 언어 자체는 느리지만 큰 의미가 없다고 판단,개발 속도와 유지보수성이 좋은 프로그래밍 언어를 사용</li>
    <li>javascript는 C++,JAVA 보다 느리지만 Node.js를 사용하면 손쉽게 비동기 처리구현이 가능해져서 빠른 처리가 가능</li>
</ul>

7. <strong> Node Package Manager(npm) : npm을 사용, 모듈을 쉽게 설치 및 활용 가능</strong>

<ul><b>- 외부 모듈 종류</b>
    <li>request : npm install request / const request = require('request');<br><b>※request로 가져온 웹 페이지는 단순한 HTML 문자열이므로 parsing을 통한 데이터의 정보화 필요</b></li>
    <li>cheerio : npm install cheerio / const cheerio = require('cheerio');<br><b>※가져온 웹 페이지의 특정 위치에서 손쉽게 데이터 추출</b></li>
    <li>async : npm install async / const async = require('async');<br>
    <b>※parallel()메소드를 사용하여 다수의 비동기 처리시 발생하는 속칭 '콜백 지옥'을 병렬처리 하여 해결</li>
</ul>

## [05월 11일]
> [11주차 05/11] 배운 내용 요약 <br>
1. Date 객체
- 생성 방법<br>
1.new Date() : 현재 시간으로 Date 객체 생성<br>
2.new Date(유닉스 타임)<br>
→ 유닉스 타임(1970년 1월 1일 00시 00분 00초 부터 경과한 밀리초)으로 Date 객체 생성<br>
3.new Date(시간 문자열) : 문자열로 Date 객체 생성<br>
4.new Date(<년>, <월-1>, <일>, <시간>, <분>, <초>, <밀리초>)<br>
→ 시간요소(년, 월-1, 일, 시간, 분, 초, 밀리초)를 기반으로 Date 객체 생성<br>
5.getOO() 형태 메소드, setOO() 형태 메소드<br>
→ {FullYear, Month, Day, Date, Hours, Minutes, Seconds, Milliseconds}<br>
→ get메소드 : 시스템 상으로 설정된 값을 가져옴 / set메소드 : 직접 값을 설정함<br>
6.getTime() : 유닉스 타임을 (1000x60x60x24)으로 나눈 값<br>
2. Array 객체
- 기본 메소드 : 대부분 파괴적 메소드로 자기 자신을 변경<br>
1.pop() : 배열의 마지막 주소에 있는 값을 제거.<br>
2.shift() : 배열의 첫번째 주소에 있는 값을 제거 후 반환.<br>
3.unshift() : 배열의 첫번째 자리에 새로운 요소 추가 후 변경된 배열의 길이를 반환.<br>
4.push() : 배열의 마지막에 새로운 요소를 추가 후 변경된 배열의 길이를 반환<br>
5.concat() : 두개의 배열을 합쳐주는 함수.<br>
6.reverse() : 배열을 역순으로 재배치.<br>
7.splice() : 배열의 특정 위치에 배열 요소를 추가하거나 삭제.<br>
8.sort() : 배열을 정렬.<br>
9.join() : 배열의 모든 요소를 연결해 하나의 문자열로 만듬.<br>
10.slice() : 배열의 지정한 부분을 리턴<br>

- 모질라 레퍼런스 - Array<br>
1.forEach() : 배열의 요소들을 하나씩 뽑아 반복<br>
2.map() : 콜백 함수에서 리턴하는 것들을 기반으로 새로운 배열 생성<br>
→ 화살표 함수 사용<br>
EX) let foo = [1, 30, 40, 50, 100];<br>
    let bar = foo.map((item, index) => {<br>
    return item +100;<br>
});<br>
console.log(bar); ---> [101, 130, 140, 150, 200]<br>
3.filter() : 콜백 함수에서 true를 리턴하는 것들을 기반으로 새로운 배열 생성<br>
→ 화살표 함수 사용<br>
EX) let foo = [1, 30, 40, 50, 100];<br>
    let foobar = foo.filter((item, index) => {<br>
    return item % 2 ==0;<br>
});<br>
console.log(foobar); ---> [30, 40, 50, 100]<br>

3. underscore.js 라이브러리 → script 태그를 사용
4. JSON 객체 : 자바스크립트 객체를 사용한 데이터 표현 방법
- 제약 사항
1.모든 key와 문자열은 더블 퀘터이션("") 사용<br>
2.숫자, 문자열, boolean 자료형만 사용<br>
- 메소드
1.JSON.stringify() : 문자열 리턴<br>
2.JSON.parse() : 객체 리턴<br>

5. 예외처리
→ 예외(Exception) : 실행에 문제가 발생하면 자동 중단됨에 의해 발생한 오류<br>
→ 예외 처리(Exception Handling) : 오류에 대처할 수 있게 하는 것<br>
- 기본 예외처리<br>
EX) TypeError : 정의 되지않은(undefined) 자료형을 일반적인 객체/함수 처럼 다룰 시에 발생<br>
→ 예외처리 : 사전에 해당 데이터가 undefined인지 조건문을 사용<br>
- try catch finally 구문
1.try : 예외가 발생할 예상되는 구문 입력<br>
2.catch : 예외 발생시에 예외처리<br>
3.finally : 관계없이 무조건 실행(catch구문에서 return값이 있거나 더 이상 수행 불가시 사용)<br>
- 고급 예외처리
EX) RangeError : 배열 생성시 길이를 음수로 지정할 때 발생<br>
→ try catch finally 구문 사용<br>
EX) try {<br>
const array = new Array[-2000]<br
} catch {<br>
    console.log("예외 발생");<br>
}finally {<br>
    console.log("finally 구문 실행");<br>
}<br>
- 예외 객체 : Exception = e / EX) e.name, e.message<br>
- 예외 강제 발생 : throw 키워드 사용 / throw 키워드 뒤에는 문자열 또는 Error 객체 입력<br>
※ 자세한 예외 출력은 Error 객체 사용(어떤 파일의 몇번째 줄에서 예외 발생했는지도 확인가능)<br>


## [05월 04일]

> [10주차 05/04] 배운 내용 요약 <br>
1. 생성자 함수(구별을 위해 대문자로 시작하는 이름 사용)
- function Product(name,price){
    this.name = name;
    this.price = price;
}
2. 프로토타입 : 생성자 함수로 만든 객체는 프로타입 공간에 메소드를 지정
※ 모든 객체가 공유 하도록 함(해당 함수를 생성자 함수로 사용했을 시)
3. null의 값과 자료형
※ (null을 출력한 값) = null / typeof(null) = object
4. 표준 내장 객체
- 기본 자료형 숫자,문자열,boolean<br>
※ 기본 자료형은 객체가 아니므로 속성과 메소드를 추가할 수 없음
- Number 객체 : 자바스크립트에서 숫자를 표현할 때 사용
※ Number 객체의 메소드<br>
1.toExponential() = 숫자를 자수 표시로 나타낸 문자열 리턴<br>
2.toFixed() = 숫자를 고정소수점 표시로 나타낸 문자열 리턴(소수점 자릿수 자름)<br>
3.toPrecision() = 숫자를 길이에 따라 지수 표시 또는 고정 소수점 표시로 나타낸 문자열을 리턴<br>
※ Number 생성자 함수의 속성<br>
1.MAX_VALUE : 숫자가 나타낼 수 있는 최대 숫자<br>
2.MIN_VALUE : 숫자가 나타낼 수 있는 최소 숫자<br>
3.NAN_VALUE : 숫자로 나타낼 수 없는 숫자<br>
4.POSITIVE_INFINITY : 양의 무한대 숫자<br>
5.NEGATIVE_INFINITY : 음의 무한대 숫자<br>
- String 객체 : 자바스크립트에서 문자를 표한할 때 사용
※ String 객체의 메소드<br>
1.split() : 특정한 기호를 기반으로 문자열을 분해<br>
## [04월 27일]
> [9주차 04/27] 배운 내용 요약 <br>
1. setInterval, setTimeout 복습(clearInterval : Interval을 종료시키는 함수)
2. 익명함수 : 이름을 지정하지 않은 함수 -  화살표 함수, function 키워드
※ 익명함수는 객체 생성을 해야 사용 가능
3. 코딩 순서에 따른 출력 우선순위 - 변수와 함수 관계없이 맨 마지막에 선언된 코드 실행
4. 함수의 실행 우선 순위 - 익명함수 > 선언적 함수
5. this 키워드
6. 자바스크립트의 객체 : 여러개의 자료형을 한번에 저장하는 자료형
※ 배열은 요소에 접근할 때 인덱스를 사용하고, 객체는 키를 사용함
7. 객체의 반복문 - for in을 사용한 반복문
8. 속성과 메소드
→ 요소 : 배열 내부의 있는 값
→ 속성 : 객체 내부에 있는 값
→ 메소드 : 객체의 속성 중 자료형이 함수인 속성
9. 생성자 함수 : 객체를 만드는 함수(대문자로 시작하는 이름 사용)



## [04월 20일]
> [8주차 04/20] 중간고사
## [04월 13일]
> [7주차 04/13] 배운 내용 요약 <br>
1. 함수 생성 방법  - 함수도 하나의 자료형 취급
- 익명 함수 - 이름을 붙이지 않고 함수 생성
※ let <함수 이름(변수)> = function () {}
- 선언적 함수 - 이름을 붙여 함수 생성
※ function <함수 이름> () {}
- 화살표 함수[ECMAScript6] -'하나의 표현식을 리턴하는 함수'를 만들 시 중괄호 생략 가능
※ let 함수 = () => {}
2. 함수의 기본 형태 - 동일한 연산/판단을 써야할 시 사용
※ function <함수 이름><매개 변수> {<함수 코드> , return <리턴 값>}
- 매개 변수가 여러 개인 함수
- 리턴 없는 함수
3. 함수의 기본 활용 형태
- 리턴 하는 함수의 기본 형태
※ function (<매개 변수>, <매개 변수>) {let output = <초깃값>; return output;}
4. 함수 매개 변수 초기화 - 매개 변수를 입력하지 않고 함수 호출(실행하면 undefined가 출력)
5. Callback 함수 - 함수의 매개 변수로 전달되는 함수(함수를 매개변수로 저장 가능)
6. 표준 내장 함수 - 자바스크립트에서 기본적으로 지원하는 함수
- 숫자 변환 함수 - 문자열을 숫자 타입으로 변환시에 사용
parseint() - 문자열을 정수로 변환
parseFloat() - 문자열을 실수로 변환
- 타이머 함수 - '특정 시간 후에' 또는 '특정 시간 마다' 어떤 일을 할 때 사용
※ 시간은 밀리초로 지정, 1초를 나타내려면 1000(밀리초)을 입력
setTimeout(함수, 시간) - 특정 시간 후에 함수를 실행
setInterval(함수, 시간) - 특정 시간 마다 함수를 실행(Ctrl + C 로 함수 종료 가능)
clearInterval(아이디) - 타이머 제거 함수(특정 시간마다 실행하던 함수 호출 중지)
## [04월 06일]
> [6주차 04/06] 배운 내용 요약 <br>
1. for 반복문 복습
2. 역 for 반복문(공식명칭X) - 배열의 요소를 뒤쪽부터 출력
3. for in / for of 반복문 - 객체에 쉽게 반복문 적용 가능
※ for in - index값이 필요할 때 사용, for of - index값이 불필요할 때 사용
4. break 키워드 - 무한반복문의 강제 종료
5. 배열의 method - 데이터를 처리할 때 가장 넓게 사용되는 데이터 타입인 배열을 조작하는 방법.
- pop : 배열의 마지막 주소에 있는 값을 제거.
- shift : 배열의 첫번째 주소에 있는 값을 제거 후 반환.
- unshift : 배열의 첫번째 자리에 새로운 요소 추가 후 변경된 배열의 길이를 반환.
- push : 배열의 마지막에 새로운 요소를 추가 후 변경된 배열의 길이를 반환
- concat : 두개의 배열을 합쳐주는 함수.
- reverse : 배열을 역순으로 재배치.
- splice : 배열의 특정 위치에 배열 요소를 추가하거나 삭제.
- sort : 배열을 정렬.
- join : 배열의 모든 요소를 연결해 하나의 문자열로 만듬.
6. continue 키워드 - 반복문 내부에서 현재 반복을 멈추고 다음 반복을 진행함.
7. scope - 변수를 사용할 수 있는 범위(스코프==블록)
8. Hoisting - 해당 블록에서 사용할 변수를 미리 정리하는 키워드
## [03월 30일]
> [5주차 03/30] 배운 내용 요약 <br>
1. if / else if 조건문 - 중복되지 않은 2~3개 이상의 조건을 구분할 시 사용
2. switch case 조건문 - 비교할 값이 명확할 시 사용<br>
※ case가 끝날때 마다 break로 종료 / switch에 없는 값 입력시 default값 출력
3. 삼항 연산자 - <조건> ? <참> : <거짓>
4. 짧은 초기화 조건문 - '||' 연산자를 불이 아닌 자료에 사용할 경우<br>
※ A || B에서 A가 참이라면 A로 대치 / A || B에서 B가 참이라면 B로 대치
5. eval 함수 - 입력값을 받고 저장하는 함수 / callback함수 - 무한반복 시키는 함수
6. 반복문  - for / while / do while<br>
※ for - 반복횟수가 명확할 때 사용, while - 반복횟수가 불명확할 때 사용
7. 배열 - 여러 개의 자료를 한꺼번에 다룰 수 있는 자료형<br>
※ let 이름 = [자료,자료,자료,자료] - 배열에는 여러 자료형이 섞여 있을 수 있음
---
## [03월 23일]
> [4주차 03/23] 배운 내용 요약 <br>
1. 문자 선택 연산자
2. 템플릿 문자열(Backtit 사용)
3. 참과 거짓의 표현 / 비교 연산자, 논리 연산자
4. 변수(let)
5. 복합 대입 연산자
6. 증감 연산자
7. 자료형 검사(typeof) / Undefined 자료형
8. 강제 자료형 변환(Boolean() 함수(0, nan, "", null, undefined)
9. 자동 자료형 변환
10. 일치 연산자(자료형 검사 포함)
11. 상수(const) - '항상 같은 수'(변수의 반대)
12. if 조건문 / if else 조건문 / 중첩 조건문
---
## [03월 16일]
> [3주차 03/16] 배운 내용 요약 <br>
1. 자바스크립트의 개요
2. node.js 설치
3. javascript프로그램 실행 방법
4. REPL사용법(터미널과 크롬)
5. push 명령
---

<!-- 최근 날짜가 상위로>