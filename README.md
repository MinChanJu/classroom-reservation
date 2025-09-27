# 🏫 Classroom Reservation System

아주대학교 강의실 예약 및 관리 시스템

## 📋 프로젝트 소개

이 프로젝트는 아주대학교 해커톤에서 4명이 함께 개발한 아주대학교의 강의실 예약 및 실시간 상태 관리를 위한 웹 애플리케이션입니다.
React와 TypeScript를 기반으로 개발되었으며, 데스크톱, 태블릿, 모바일 등 다양한 디바이스에서 반응형으로 동작합니다.

### ✨ 주요 기능

- **실시간 강의실 상태 모니터링**: 강의실의 사용 가능 여부를 실시간으로 확인
- **3D 건물 뷰어**: Three.js를 활용한 대화형 3D 건물 및 층별 보기 (데스크톱)
- **강의실 예약 시스템**: 직관적인 인터페이스를 통한 강의실 예약
- **반응형 디자인**: 모바일, 태블릿, 데스크톱 환경에 최적화된 UI
- **다중 건물 지원**: 성호관, 팔달관, 다산관 등 여러 건물 관리
- **PassKey 인증**: 생체 인증을 활용한 보안 로그인
- **QR 코드 생성**: 강의실 정보 공유를 위한 QR 코드 기능

### 🏢 지원 건물

- **성호관**: 1층~6층 강의실 관리
- **팔달관**: 1층~3층 강의실 관리  
- **다산관**: 1층~4층 강의실 관리

## 🛠 기술 스택

### Frontend
- **React 19.1.0** - UI 프레임워크
- **TypeScript** - 타입 안전성을 위한 언어
- **Vite** - 빠른 개발 및 빌드 도구
- **Three.js** - 3D 그래픽 렌더링
- **React Three Fiber** - React용 Three.js 바인딩
- **Bootstrap 5.3.6** - UI 컴포넌트 라이브러리

### 개발 도구
- **ESLint** - 코드 품질 관리
- **TypeScript ESLint** - TypeScript 전용 린팅
- **Vite SWC Plugin** - 빠른 React 컴파일

### 추가 라이브러리
- **jQuery & jQuery DateTimePicker** - 날짜/시간 선택
- **QRCode.js** - QR 코드 생성
- **React DatePicker** - 날짜 선택 컴포넌트
- **js-sha256** - 암호화 해싱
- **Emotion** - CSS-in-JS 스타일링

## 🚀 시작하기

### 필수 요구사항

- Node.js 16.0 이상
- npm 또는 yarn

### 설치 및 실행

1. **저장소 클론**
   ```bash
   git clone https://github.com/MinChanJu/classroom-reservation.git
   cd classroom-reservation
   ```

2. **의존성 설치**
   ```bash
   npm install
   ```

3. **개발 서버 실행**
   ```bash
   npm run dev
   ```
   
   서버가 `http://localhost:5173`에서 실행됩니다.

4. **프로덕션 빌드**
   ```bash
   npm run build
   ```

5. **빌드 미리보기**
   ```bash
   npm run preview
   ```

## 📱 화면 구성

### 데스크톱
- **3D 건물 뷰어**: Three.js 기반 대화형 3D 건물 탐색
- **층별 상세 보기**: 각 층의 강의실 배치도 및 상태 확인

### 모바일/태블릿
- **통합 관리 인터페이스**: 강의실 상태, 예약, 설정을 탭으로 구분
- **터치 최적화**: 모바일 환경에 최적화된 UI/UX

## 🗂 프로젝트 구조

```
src/
├── components/          # React 컴포넌트
│   ├── common/         # 공통 컴포넌트
│   ├── desktop/        # 데스크톱 전용 컴포넌트
│   ├── mobile/         # 모바일 전용 컴포넌트
│   ├── tablet/         # 태블릿 전용 컴포넌트
│   └── reservation/    # 예약 관련 컴포넌트
├── data/               # 정적 데이터 및 설정
├── hooks/              # 커스텀 React 훅
├── pages/              # 페이지 컴포넌트
├── styles/             # CSS 모듈 스타일
├── types/              # TypeScript 타입 정의
└── utils/              # 유틸리티 함수
```

## 🔧 주요 기능 설명

### 실시간 강의실 모니터링
- 30초마다 자동 새로고침으로 실시간 데이터 업데이트
- 서버 동기화를 통한 정확한 시간 관리
- 강의실 상태: 사용 가능, 사용 중, 점검 중

### 반응형 디자인
- **useDeviceType** 훅을 통한 디바이스 감지
- 디바이스별 최적화된 컴포넌트 렌더링
- CSS 모듈을 활용한 스타일 분리

### 3D 건물 뷰어
- Three.js 기반 실시간 3D 렌더링
- 층별 네비게이션 및 강의실 선택
- 인터랙티브 카메라 컨트롤

### PassKey 인증
- WebAuthn API 활용
- 생체 인증 (지문, 얼굴 인식)
- 보안성이 강화된 로그인 시스템

## 🧪 개발 및 빌드

### 사용 가능한 스크립트

```bash
npm run dev      # 개발 서버 실행 (포트: 5173)
npm run build    # 프로덕션 빌드
npm run lint     # ESLint 코드 검사
npm run preview  # 빌드된 앱 미리보기
```

### 개발 환경 설정

- **호스트 설정**: `--host` 옵션으로 네트워크 접근 가능
- **포트**: 기본 5173 포트 사용
- **Hot Reload**: Vite의 HMR로 빠른 개발 경험

## 📂 주요 파일 설명

- `src/App.tsx` - 메인 애플리케이션 컴포넌트
- `src/pages/ClassroomManagement.tsx` - 강의실 관리 메인 페이지
- `src/hooks/useDeviceType.ts` - 디바이스 타입 감지 훅
- `src/data/` - 건물 및 강의실 정적 데이터
- `src/utils/passkeyAuth.ts` - PassKey 인증 로직
- `src/utils/qrCode.ts` - QR 코드 생성 유틸리티