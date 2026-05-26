# playwright-practice

Playwright를 학습하고 연습하기 위한 개인 프로젝트입니다.

## 환경

- [Playwright](https://playwright.dev/) v1.x
- TypeScript
- Node.js

## 브라우저

Chromium, Firefox, WebKit (기본 설정)

## 설치

```bash
npm install
npx playwright install
```

## 테스트 실행

```bash
# 전체 테스트 실행 (headless)
npx playwright test

# 특정 파일만 실행
npx playwright test playwright-dev.spec.ts

# 브라우저 화면을 보면서 실행
npx playwright test --headed

# 테스트 결과 리포트 열기
npx playwright show-report
```

## Codegen (테스트 코드 자동 생성)

브라우저 동작을 녹화해서 테스트 코드를 자동으로 생성합니다.

```bash
npx playwright codegen https://example.com
```

## 폴더 구조

```
playwright-practice/
├── tests/                        # 테스트 파일
│   ├── example.spec.ts           # Playwright 기본 샘플 테스트
│   └── playwright-dev.spec.ts    # Codegen으로 생성한 첫 테스트
├── tests-examples/               # Playwright 제공 예제
├── playwright.config.ts          # Playwright 설정
└── .github/
    └── workflows/
        └── playwright.yml        # GitHub Actions CI 설정
```

## CI

GitHub Actions를 통해 push 시 자동으로 전체 테스트가 실행됩니다.
