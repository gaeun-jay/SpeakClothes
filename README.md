# 옷을말하다 (Speak-Clothes)
**시각장애인을 위한 옷 색감 및 종류 음성 안내 앱**

<div align="center">
  <img src="./introduce.gif" width="600"/>
</div>

> ⚠️ **안내**: 주 계정 이전(`jga-eun` → `gaeun-jay`)으로 인해 기존 계정인 [@jga-eun](https://github.com/jga-eun) 에서 fork 해 온 프로젝트입니다. 프로젝트 원본 레포지토리 링크는 다음과 같습니다.
> - 원본: [jga-eun/speak-clothes](https://github.com/jga-eun/speak-clothes)

---

## 🏆 수상

**2023 성신여자대학교 AI융합학부 소프트웨어 경진대회 최우수상** (2023.09)

---

## 프로젝트 배경 및 목적

시각장애인이 혼자 옷을 입을 때 색상과 종류를 구분하기 어렵다는 문제에서 출발한 프로젝트입니다. 카메라로 옷을 촬영하면 AI가 색감과 종류를 분석해 음성으로 안내해주는 앱을 개발했습니다. 색을 단순한 색상명이 아닌 촉각·기억·미각 등 공감각적 표현으로 안내해 시각장애인이 보다 직관적으로 이해할 수 있도록 했습니다.

---

## 팀 구성 및 담당 역할

**개발 기간**: 2023.05 ~ 2023.09 (5개월) | **팀원**: 4명

### 프로젝트에서 제 역할은 아래와 같습니다

| 구분 | 내용 |
|------|------|
| **PM** | 프로젝트 전체 일정 관리 및 기획 |
| **AI 모델** | Google Vertex AI / Vision AI 모델 학습 및 앱 연동 |
| **데이터 구축** | Firebase를 활용한 공감각적 색 안내 라벨 데이터 구축 (별도 서버 없이 운영) |
| **Frontend** | Flutter 기반 카메라 캡처 로직 구현 |

---

## 주요 기능

- **옷 촬영 및 분석**: 카메라로 옷을 촬영하면 AI가 색상과 종류를 자동 분석
- **음성 안내**: Google TTS를 통해 분석 결과를 음성으로 안내
- **공감각적 색 표현**: 색을 단순 색상명이 아닌 촉각·기억·미각 등의 감각적 표현으로 안내
- **Firebase 기반 데이터 관리**: 별도 서버 없이 Firebase로 라벨 데이터 운영

---

## 기술 스택

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)

| 구분 | 사용 기술 |
|------|-----------|
| 앱 개발 | Flutter (Dart) |
| AI 모델 | Google Vertex AI, Vision AI |
| 음성 안내 | Google TTS (flutter_tts) |
| 데이터베이스 | Firebase (Cloud Firestore) |
| 기타 | googleapis, flutter_dotenv |

---

## 프로젝트 구조

```
speak-clothes-master/
├── lib/
│   ├── main.dart         # 앱 진입점 및 주요 로직
│   ├── checkAPI.dart     # API 연동 확인
│   └── color.dart        # 색상 데이터 처리
├── assets/
│   └── speak_clothes_top_icon.png
└── pubspec.yaml
```

---

## 설치 및 실행

### 사전 요구사항
- Flutter SDK 3.0.0 이상
- Dart SDK 3.0.0 이상
- Firebase 프로젝트 설정
- Google Cloud (Vertex AI, Vision AI) API 키

### 실행 방법

```bash
git clone <repository-url>
cd speak-clothes-master
flutter pub get
flutter run
```

> Firebase 및 Google Cloud API 키 설정이 필요합니다. `.env` 파일에 키를 입력해주세요.
