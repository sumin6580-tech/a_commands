---
description: .gitignore 생성, origin 연결, prefix 규칙에 맞춘 커밋까지 한 번에 처리
argument-hint: [커밋 메시지]
allowed-tools: Bash(git:*), Read, Write
---

# Commit 작업

아래 순서대로 커밋 작업을 진행해 줘.
이미 처리된 단계는 확인 후 건너뛰어 줘.

## 1. `.gitignore` 생성

> 프로젝트 루트에 `.gitignore`가 이미 있으면 이 단계는 생략

다음 항목을 모두 포함한 `.gitignore`를 생성해 줘.

- **에디터/IDE**: VS Code(`.vscode/`), JetBrains(`.idea/`) 등
- **macOS**: `.DS_Store`, `.AppleDouble`, `._*` 등
- **Windows**: `Thumbs.db`, `Desktop.ini`, `$RECYCLE.BIN/` 등
- **환경변수 파일**: `.env`, `.env.*`(단, `.env.example`은 제외하지 않음) 등
- **기타 일반 항목**: 로그 파일, 의존성 폴더(`node_modules/` 등), 빌드 산출물

## 2. 원격 저장소 연결

> `git remote -v`로 확인해서 `origin`이 이미 연결되어 있으면 이 단계는 생략

- 원격 이름: `origin`
- 주소: `[https://github.com/sumin6580-tech/a_commands.git]`

```bash
git remote add origin [https://github.com/sumin6580-tech/a_commands.git]
```

## 3. 커밋

변경 사항을 스테이징한 뒤, 아래 메시지에 적절한 prefix를 붙여 커밋해 줘.

- 커밋 메시지: `$ARGUMENTS`
- 형식: `<prefix>: <메시지>` (예: `feat: 로그인 기능 추가`)
- 메시지 내용과 실제 변경 사항을 보고 가장 알맞은 prefix 하나를 골라 줘.

### 커밋 prefix 규칙

| prefix | 용도 |
| --- | --- |
| `feat` | 새로운 기능 추가 |
| `fix` | 버그 수정 |
| `docs` | 문서 수정 (README 등) |
| `style` | 코드 포맷 변경 (세미콜론, 공백 등) |
| `refactor` | 리팩토링 (기능 변화 없음) |
| `test` | 테스트 코드 추가/수정 |
| `chore` | 빌드, 설정, 패키지, 기타 작업 |
| `perf` | 성능 개선 |
| `ci` | CI 설정 수정 |
| `build` | 빌드 시스템 수정 |
| `revert` | 커밋 되돌리기 |