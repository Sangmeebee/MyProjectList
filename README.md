# 나의 프로젝트

## 1. 패션노트

#### 개요

- 자신의 패션을 평가받고, 남의 패션을 평가해주어 패션으로 경쟁하며 소통 할 수 있는 어플리케이션

#### 기술스택

- Kotlin, Android
- Retrofit2, MVVM(Model-View-ViewModel), RxJava, Java
- Spring Boot
- AWS EC2, AWS S3, AWS RDS

#### 기능
- 평가
  - 남들의 패션을 보고 점수를 매겨보자
- 나의 기록공간
  - 나만의 패션 포트폴리오 만들기
- 랭킹
  - 평가받은 점수로 한 주마다 랭킹이 매겨진다.
  - 랭킹 화면이 한주마다 갱신된다.
- 사진등록
  - 나의 멋지고 예쁜 패션사진을 등록한다.
  - 옷의 스타일과 브랜드를 같이 등록 할 수 있다.
- 검색
  - 스타일, 브랜드, 계정 별로 검색할 수 있다.

#### 기획안 / 모델구조 / 요구사항 분석서
참고 자료 : [패션노트 자료](https://github.com/Sangmeebee/FashionPeople/tree/master/FashionPeople%20%EC%9E%90%EB%A3%8C)

#### 내가 구현한 부분
- 전부

#### 설계

- 프론트엔드
  - 서버와 retrofilt2 라이브러리와 RxJava를 이용하여 데이터를 주고 받았습니다.
  - 이미지는 이미지 명을 DB에 저장하고 파일은 AWS S3에 저장하였습니다.
  - 아키텍쳐는 MVVM을 사용하였습니다.
- 백엔드
  - Spring Boot 프레임워크를 이용하였습니다.
  - DB 구조를 설계했습니다.
  - AWS EC2를 이용하여 배포했습니다.
- 팀구성
  - 2인
- URL
  - [플레이 스토어](https://play.google.com/store/apps/details?id=com.sangmee.fashionpeople)
  - [GIT 주소 (모바일 앱)](https://github.com/Sangmeebee/FashionPeople)
  - [GIT 주소 (서버)](https://github.com/Sangmeebee/FashionPeopleDB)



## 2. 아이가릿 - Eye Got it

#### 개요

- 사물인식을 이용한 시각장애인을 위한 길안내 시스템 어플리케이션

#### 기술스택

- Java, Android
- Google Firebase Realtime Database
- Spring 
- AWS EC2

#### 기능

- 회원가입과 로그인
   - 회원가입 시 보호자와 사용자를 연동한 후 로그인 과정을 거칩니다.

- 경로설정 (보호자)
  - 보호자가 사용자가 자주 가는 몇 가지 경로를 클릭만으로 PIN point와 안내 텍스트를 이용하여 미리 설정합니다.

- 음성으로 경로안내 (사용자)
  - 보호자가 미리 설정해 둔 경로를 사용자는 음성을 통해서 “선택” 하고 음성을 통하여 “안내” 받습니다.

- 위험알림 전송
  - 위험 상황 발생 시 사용자가 화면을 오른쪽으로 drag 함으로써 보호자에게 위험 알림을 전송 할 수 있습니다.
    또한, 사용자의 기기의 심각한 충돌 발생 시 보호자에게 자동으로 위험 알림이 전송됩니다.

- 현재위치 전송
  - 위험 상황을 대비하여 사용자가 화면을 왼쪽으로 drag 함으로써 보호자에게 현재 위치를 전송 할 수 있습니다.

- 신호등 인식과 사물 거리 인식
  - 카메라가 장착된 안경을 사용하여 신호등의 적색신호와 녹색신호를 판별할 수 있습니다.
  - 또한, 물체(장애물)의 위치와 사용자 사이의 거리를 측정 할 수 있습니다.

#### 내가 구현한 부분

- 회원가입과 로그인
  - Firebase RealTime Database를 이용하여 회원가입 로그인 기능을 구현했습니다.
- 경로설정
  - Naver Map API의 Marker의 좌표를 DB에 저장했습니다.
- 경로안내
  - 현재 위치의 자표와 DB에 저장되있는 경로의 좌표를 비교해서 Marker 5m 이내에 사용자가 있는지 비교하는 로직을 구현했습니다.
- 신호등 인식
  - Tensorflow Object Detection API를 사용하여 신호등의 색을 구별했습니다.
  - [신호등 교육과정 정리](https://github.com/Sangmeebee/Tensorflow-ObjectDetectionApi)

#### 팀구성 

- 대학동기 4인

#### URL

- [GIT 주소 (모바일)](https://github.com/Sangmeebee/EyeGotIt)
- [GIT 주소 (웹)](https://github.com/Sangmeebee/EyeGotIt_Web)
