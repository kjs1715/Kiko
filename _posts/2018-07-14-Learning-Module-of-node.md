# 1. 주요 기본 모듈

<br>

# 2. 전역 객체(global)

<br>

## 2.1 주요 전역 객체

- process
- console
- Buffer (Class)
- require
- \__filename,  __dirname
- module
- exports
- Timeout 함수

<br>

## 2.2 process

<br>

### 2.2.1 어플 프로세스 실행 정보

- env : 어플 실행 환경
- version : Node,js 버전
- arch, platform : CPU와 플렛폼 정보
- argv : 실행 명령 파라미터

### 2.2.2 event

- exit : 어플 종료 이벤트
- beforeExit : 종료 되기 전에 발생하는 이벤트
- uncaughtException : 예외 처리되지 않은 예외 이벤트

### 2.2.3 function

- exit
- nextTick

## 2.3 timer

<br>

- setTimeout : 지연 동작
- setInterval : 반복 동작

## 2.4 console 

<br>

- console.log('log', ...)
- ~.info(...)
- ~.warn(...)
- ~.error(...)

### 2.4.1 custom console

- load type of console

  ```javascript
  var Console = require('console').Console;
  ```

- new Console(stdout[, stderr])

  - stdout : 표준 출력 스트림, info, log
  - stderr : 에러 출력. warn, error

- Error logs

  ```javascript
  var output = fs.createWriteStream('./stdout.log');
  var errorOutput = fs.createWriteStream('./stderr.log');
  var logger = new Console(output, errorOutput);
  ```

- precess timer

  `console.tome(TIMER_NAME)`

  `console.timeEnd(TIMER_NAME)`



블로깅이 너무느리다....나머진 나중에...