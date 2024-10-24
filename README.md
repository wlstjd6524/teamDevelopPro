# [ 2024.09 - 12 캡스톤디자인 프로젝트 ]
## 👨‍🏫 프로젝트 소개
Wi-Fi 채널 상태 정보를 활용한 인간 행동 인식 시스템 

## ⏲️ 개발 기간 
- 2024.09.16 ~ 2024.11.26
  - 프로젝트에 대한 이해 및 학습
  - 프로젝트에 필요한 하드웨어 및 소프트웨어 구성
  - 오픈소스 채택
  - 환경구성
  - 데이터 수집
  - 머신러닝 모델 구현 및 학습
  - UI/UX 구현 및 구현한 UI/UX 에 학습된 데이터 적용
  - 프로젝트 제출
  - 발표 및 평가

## 🧑‍🤝‍🧑 팀 소개
- **이진성** : 팀장
- **남궁준** : 팀원
- **홍성환** : 팀원

## 💻 개발환경 및 도구와 하드웨어 플랫폼 정보
- Raspberry Pi 4 Model B 2GB RAM
  - Raspberry Pi OS Kernel Version : 5.10.92
  - Nexmon Tool & Nexmon OpenSource
    - Nexmon OpenSource : <https://github.com/nexmonster/nexcsi>
- Wi-Fi AP
- TensorFlow / Keras
- WireShark

## 📌 프로젝트개요
최근 기술이 발전함에 따라 센서를 활용한 인간 행동을 탐지하는 시스템이 각광받고 있습니다. <br>
기존 센서 및 카메라 기반의 인간 행동 인식(HAR) 시스템은 비용 및 사생활 침해 등의 문제를 안고 있습니다. <br>
Wi-Fi 신호를 활용한 인간 행동 인식(HAR) 기술은 이러한 문제를 해결할 수 있으며, 
추가적인 하드웨어 없이 Los(가시선) 및 NLoS(비가시선) 환경에서 인간 행동 인식하는 시스템을 개발하고자 합니다.

## ✒️ 프로젝트 목표
**LoS(가시선) 환경 : 중간 장애물 없이 인간 행동을 신호가 곧바로 받는 환경** <br>
**NLoS(비가시선) 환경 : 중간에 장애물이 있는 상태에서 인간 행동을 신호가 받는 환경** <br>

해당 LoS/NLoS 환경을 구분하여, 각 환경에 맞는 HAR 모델을 적용함으로써 행동 인식 정확도를 개선하는 시스템을 우선 구현하는 것 입니다. <br>
프로젝트의 개발내용은 다음과 같습니다. 
- Raspberry Pi OS 설치 (2대 운용)
  - Raspberry Pi 의 OS 는 반드시 "Kernel Version : 5.10.92" 버전을 권장함.
    - NEXMON_CSI 가 지원하는 운영체제는 4.19/5.4 , 4.19와 5.4 os로 setup하는 경우 buster 저장소가 호환되지 않아 오류 발생
- Paspberry Pi 에 Nexmon Tool 설치
- Wi-Fi 신호를 쏠 수 있는 AP 구성
- CSI 데이터 수집
  - Raspberry Pi 와 Wi-Fi AP 를 통해 신호를 쏠 수 있는 환경을 구성하고 LoS/NLoS 환경에서 데이터를 수집합니다.
- LoS/NLoS 분류 모델 구현
  - GRU 기반의 신경망을 사용하여 수신 데이터를 LoS 와 NLoS 로 구분합니다.
- HAR 모델 구현
  - LoS 와 NLoS 환경에 각각 적합한 HAR 모델을 학습시켜 인간 행동을 인식합니다.
- 데이터 전처리
  - 수집된 CSI 데이터를 필터링하여 노이즈를 제거하고 진폭정보를 추출합니다.
- 모델 학습 및 평가
  - 수집된 데이터를 바탕으로 모델을 학습시키고 기존 HAR 시스템과 비교하여 성능을 평가합니다.     

## 📍 기대효과 및 활용방안

## ✍ 프로젝트 작업 내용

## 💾 프로젝트 결과
