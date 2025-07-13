# chatbot 백엔드

# 1. 개요
chatbot_fe와 자연어 처리를 하는 파이썬을 연결


# 2. 기획 이유 및 배경
chatbot 프론트엔드 작업, 파이썬을 통한 모델 학습이 끝났다.<br>
이 두 기능을 엮어 자연어 처리를 하기 위해 필요한 코드를 작성해보자!

# 3. 기능 설명
파이썬과 리액트를 연결하여 챗봇이 정상적으로 작동하도록 한다. <br>
리액트에서 넘어온 JSON파일(이용자가 작성한 문장)을 챗봇에게 전달 <br>
챗봇이 작업하여 출력한 JSON파일을 다시 리액트로 전달<br>

# 4. 코드 리뷰
## ChatService
chatbot_be의 주요 기능

process 메서드
- 이용자의 환경에 맞게 파이썬을 실행하는 코드
- builder을 통해 파이썬 기능을 수행한다.


## ChatController
리액트와 백엔드(자바) 상호작용하기 위해 필요한 코드

@CrossOrigin
역할
- 다른 도메인(출처)에서 이 API에 접근할 수 있도록 허용
사용 이유
- 프론트엔드가 http://localhost:3000에서 실행되고 백엔드가 http://localhost:8080에서 실행된다면,<br>
  브라우저의 CORS 정책에 의해 차단될 수 있다. 이를 허용하기 위해 사용한다.


# 5. 구현 화면
https://github.com/juyonghyeon/quick_draw_fe
