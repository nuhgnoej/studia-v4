# Studia 퀴즈 앱

이 프로젝트는 React Native 기반의 학습용 퀴즈 애플리케이션입니다. Expo Router를 사용하여 화면을 구성하고, Firebase 인증 및 로컬 SQLite 데이터베이스를 통해 문제를 관리합니다.

## 주요 기능

- **Firebase 인증**: 이메일과 구글 로그인을 지원합니다.
- **JSON 문제 세트 업로드**: `/upload` 화면에서 JSON 형식의 문제 세트를 업로드하면 SQLite DB에 저장됩니다.
- **문제 풀기**: 세트별 문제 목록을 불러와 `StageQuiz` 컴포넌트로 퀴즈를 진행합니다.
- **틀린 문제만 다시 풀기**: 최근 풀이 결과를 기반으로 오답 문제만 선택하여 풀 수 있습니다.
- **태그 기반 배경 이미지**: 문제 태그에 따라 배경 이미지를 매칭합니다.

## 실행 방법

1. 의존성 설치

   ```bash
   npm install
   ```

2. 앱 실행

   ```bash
   npx expo start
   ```

브라우저 콘솔에서 Android/iOS 시뮬레이터 또는 Expo Go로 실행할 수 있습니다.

## 폴더 구조

- `app/` – 화면별 라우트 파일을 모아두었습니다.
- `components/` – 퀴즈 진행에 필요한 공통 컴포넌트들이 위치합니다.
- `lib/` – Firebase 설정과 SQLite 관련 모듈이 있습니다.
- `assets/` – 문제 세트 JSON과 이미지 등의 정적 자산을 보관합니다.
- `scripts/` – 태그 추출 및 질문 파일 매핑 등 유틸리티 스크립트를 제공합니다.

## 초기화

새로운 빈 프로젝트 상태로 돌리고 싶을 때는 다음 명령을 실행합니다.

```bash
npm run reset-project
```

이 스크립트는 기본 예제 코드를 `app-example` 폴더로 이동시키고 비어 있는 `app` 폴더를 생성합니다.

## 참고

이 앱은 파일 기반 라우팅을 사용하며, 자세한 내용은 Expo Router 문서를 참고하세요. 테스트 데이터는 `assets/questions` 폴더에 JSON 형식으로 포함되어 있습니다.
