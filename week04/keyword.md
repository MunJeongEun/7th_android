# Chapter 3 - Thread & Coroutine
## ⚡️Thread
- Thread란 무엇일까요?  
  : 프로그램 내에서 실행되는 가장 작은 작업 단위

- Thread를 사용하는 예시는 무엇이 있을까요?  
  : VI 에디터에서 텍스트 출력과 입력을 동시에 진행

## ⚡️Main Thread와 Worker Thread
- View Control을 담당하는 Thread는 무엇일까요?  
  : Main Thread, 모든 UI 관련 작업은 이 스레드에서 실행되어야 하며, 비동기 작업이 완료된 후 UI를 업데이트해야 할 때는 runOnUiThread() 메서드를 사용하여 Main 스레드에서 작업을 수행

- Worker Thread는 어떤 작업을 담당할까요?  
  : 네트워크 요청, 파일 읽기/쓰기, 복잡한 계산 등 주로 I/O 작업이나 긴 작업을 수행

## ⚡️Single Thread와 Multi Thread
- Single-Thread란 무엇일까요?  
  : 하나의 스레드만 사용하여 작업을 수행하는 방식, 모든 작업이 순차적으로 진행되며, 작업이 완료될 때까지 다른 작업은 대기해야 합니다. 간단한 애플리케이션이나 UI 처리에서 유용하지만, 다중 작업을 동시에 처리할 수 있는 능력이 제한적

- Multi-Thread란 무엇일까요?  
  : 여러 스레드를 동시에 사용하여 작업을 수행하는 방식, 다수의 스레드가 동시에 실행되어 작업을 병렬로 처리할 수 있으며, 이를 통해 프로그램의 처리 성능과 응답성 개선 가능

## ⚡️동기와 비동기
- 동기란 무엇일까요?  
  :두 개 이상의 작업이 서로의 완료를 기다리며 순차적으로 진행되는 방식

- 비동기란 무엇일까요?  
  : 작업이 시작된 후, 다른 작업을 기다리지 않고 즉시 다음 작업을 수행하는 방식

- 동기와 비동기 각각의 장단점은 무엇이 있을까요?  
  - 동기의 장점 : 간단한 로직, 디버깅 용이
  - 동기의 단점 : 응답성 및 성능 저하
  - 비동기의 장점 : 응답성 유지, 효율적인 자원 사용
  - 비동기의 단점 : 복잡한 로직, 디버깅 어려움

- 동기와 비동기를 사용하는 예시에는 무엇이 있을까요?  
  - 동기 예시 : 메인 스레드에서 파일을 읽는 경우, 파일이 읽힐 때까지 프로그램이 대기
  - 비동기 예시 : 네트워크 API 요청을 비동기적으로 수행하여 응답을 기다리는 동안 다른 작업을 수행

## ⚡️Handler
- Android에서 Handler란 무엇일까요?  
  :다른 스레드와 상호작용할 수 있도록 해주는 클래스, 메시지를 전송하고, 수신하며, 처리할 수 있는 기능을 제공

- Handler를 사용하는 이유는 무엇일까요?  
  : Main(UI) 스레드와의 통신

- Handler의 Message란 무엇일까요?  
  : Handler를 통해 전달되는 객체, 작업 식별자, 데이터, 상태 정보를 포함

- Handler를 사용하는 예시에는 무엇이 있을까요?  
  : 백그라운드에서 데이터를 다운로드한 후, Handler를 사용하여 메인 스레드에서 UI를 업데이트

## ⚡️Looper
- Android에서 Looper란 무엇일까요?  
  : 스레드의 메시지 큐를 관리하고 처리하는 데 사용되는 클래스, 큐에 있는 메시지를 처리하는 루프를 제공

- Looper를 활용하는 예시는 무엇이 있을까요?  
  : 특정 스레드에서 Looper를 사용하여 메시지를 처리하고 UI를 업데이트

## ⚡️Coroutine
- Coroutine이란 무엇일까요?  
  : 비동기 코드를 작성하는 데 사용되는 경량 스레드

- Coroutine은 언제 사용할까요?  
  : 비동기 작업, UI 업데이트

- Coroutine의 Dispatcher란 무엇일까요?
  : 코루틴이 실행될 스레드를 결정하는 역할, 작업의 병렬성, 동시성 등을 관리

- Dispatcher의 종류에는 무엇이 있을까요?  
  - Dispatchers.Main : UI 스레드에서 코루틴을 실행
  - Dispatchers.IO : I/O 작업(네트워크 요청, 파일 읽기 등)을 위한 스레드
  - Dispatchers.DefaultUI : 계산 등과 같이 CPU 집약적인 작업을 위한 스레드
  - Dispatchers.Unconfined : 호출한 스레드에서 바로 코루틴을 시작하고, 이후 작업이 실행될 스레드는 작업이 완료된 후에 결정

## 📂실습 인증
강의 섹션 5까지 진행
[Github](https://github.com/MunJeongEun/practice-7th-android.git)