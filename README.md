# Snior+ (중장년 맞춤형 교육 정보 통합 플랫폼 )

### [통합 깃허브 링크 (클릭)](https://github.com/kimyoo04/seoul-competition-all)

![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/12980764-4a1b-4bae-9bcd-cf63751853f2)




## 팀 구성원

<table>
<tr>
    <th align="center"><a href="https://github.com/kimyoo04"><img src="https://avatars.githubusercontent.com/u/58503130?v=4" width="100px;" alt="kimyoo04"/>         <br /><sub><b>kimyoo04ss</b><br>
    <th align="center"><a href="https://github.com/Pang-dachu"><img src="https://avatars.githubusercontent.com/u/54354769?v=4" width="100px;" alt="Pang-dachu"/>         <br /><sub><b>Pang-dachu</b><br>
    <th align="center"><a href="https://github.com/chae-zero"><img src="https://avatars.githubusercontent.com/u/115343657?v=4" width="100px;" alt="chae-zero"/>         <br /><sub><b>chae-zero</b><br>
    <th align="center"><a href="https://github.com/beginner0107"><img src="https://avatars.githubusercontent.com/u/81161819?v=4" width="100px;" alt="beginner0107"/>         <br /><sub><b>beginner0107</b><br>
    <th align="center"><a href="https://github.com/kawkmin"><img src="https://avatars.githubusercontent.com/u/86940335?v=4" width="100px;" alt="kawkmin"/>         <br /><sub><b>kawkmin</b><br>
</tr>
<tr>
    <td align="center">FrontEnd
    <td align="center">AI Developer
    <td align="center">DX enginer
    <td align="center">BackEnd
    <td align="center">BackEnd
</tr>
</table>

## 목차

1. [개발 기간](#개발-기간)
2. [프로젝트 개요](#프로젝트-개요)
3. [기획서](#기획서)
4. [ERD](#erd)
5. [구현 기능 목록](#구현-기능-목록)
6. [주요 구현 과정](#주요-구현-과정)
7. [배포](#배포)

## 📌개발 기간

23.04.05 ~ 23.05.31 (37일)

## 📌프로젝트 구조

![인프라구조](https://github.com/kimyoo04/seoul-competition-all/assets/58503130/cfa63cf8-2a32-4ef7-8b7b-10ddd3a25623)

## 📌프로젝트 개요

#### 주관 : [2023년 서울 열린데이터광장 공공데이터활용 모바일 앱/웹 경진대회 프로젝트](https://mediahub.seoul.go.kr/gongmo/2000334)

#### 제출 기획서 : [PDF 구글 드라이브 미리보기 & 다운 링크](https://drive.google.com/file/d/1PyE1aSixQyArHl3xXwz65gMs2Vh6I8RT/view?usp=sharing) (20장)

#### 도메인 주소 : [~~도메인 주소 링크~~ ](https://www.seniorplus.site) 비용 문제로 중단

#### 주요 기능

`서울시 50플러스포털 교육정보` 와 `서울시 어르신 취업지원센터 교육정보` 두 데이터 API를 활용한, 중장년층 교육 정보 통합 플랫폼입니다.
주요 기능으론 다음과 같습니다.

1. 실시간으로 최신 교육 정보 확인 및 필터링 기능 제공
2. 사용자들이 정보를 공유하고 질문할 수 있는 게시판 구현
3. 중장년층을 고려하여 쿠키를 사용한 간편한 사용자 정보 수집 방식 도입
4. 수집된 정보를 시각화하여 다양한 통계 기능 제공

## 📌기획서


<details>
    <summary>자세히 (클릭)</summary>

![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/b87116d2-235e-4951-b2bc-7f422e274955)

![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/0b4f9390-9c52-48b6-88bf-c3311607401f)

![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/cc1faab4-e704-409e-80f4-3e7930e9704a)

</details>

## 📌ERD

<details>
    <summary>자세히 (클릭)</summary>
    
![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/68efbf0d-da09-476c-a557-e46adc998d3a)

</details>

## 📌구현 기능 목록

<details>
    <summary>자세히 (클릭)</summary>
    
### 교육 정보 통계
![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/45db426f-d73e-4093-9d99-a9ad6110b689)
### 챗봇
![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/981fe8a4-2dd1-4c8c-a928-501f9e49e8c5)
### 교육 정보 조회 및 필터링 기능
![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/cbe7fa12-a404-4fed-a9f7-954b5824580f)
### 교육 정보 상세 조회 및 댓글
![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/c5ce5c28-8115-4eb5-b124-28c262b417c9)
### 자유 게시판 관련 기능
![image](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/d9636da3-576a-4de3-8843-fc0fac1402aa)

</details>


## 📌주요 구현 과정

### 다른 두 공공 데이터 API를 매핑하여, 하나의 Entity로 만드는 데이터 파이프라인 구축

JSONParser 을 통해 URL에서 데이터를 가져와, 두 공공 데이터를 분석하여 ERD 규격에 맞게 전처리 및 저장을 하였습니다.

실시간으로 유저에게 교육 정보를 제공하기 위해 항상 OpenAPi를 확인하도록 하였는데, 성능상 문제를 생길 가능성이 있어 최적화 작업을 하였습니다. 공공데이터의 교육정보는 사라지지 않기 때문에 총 데이터 개수로 업데이트 여부를 결정하였으며, 업데이트 시, 각 공공 데이터 API에 최적화된 알고리즘을 구현하여 사용하였습니다.

`서울시 어르신 취업지원센터 교육정보` 는 차례대로 새로운 데이터가 들어오므로, 처음부터 데이터 크기 차수만큼 데이터를 Insert 하였습니다.

`서울시 50플러스포털 교육정보` 는 앞에서부터 데이터가 들어오긴 하지만, 랜덤성이기 때문에, 앞에서부터 origin_id를 비교하여 insert를 하였으며, 차수만큼 데이터가 추가되면  바로 종료시키도록 하였습니다.

또한 한번에 많은 데이터가 들어올 것을 방지하고자, 스케줄러를 사용하여 매일 16시에 무조건 한번 업데이트를 하도록 하였습니다.

### Python 기반의 AI를 JAVA 기반 Spring과 연결

- **WebClient**를 통해, Python 프레임워크인 **FastAPI**를 AI 서버로 두어, Spring과 연결하여, AI 모델을 서버에 추가 부하없이, 사용할 수 있게 하였습니다.


## 📌배포

### 배포 된 화면
![KakaoTalk_20231120_182237205](https://github.com/kawkmin/seoul-competition-backend/assets/86940335/52d173b5-9fb9-4ed6-bcbc-db031a6d3dbe)

