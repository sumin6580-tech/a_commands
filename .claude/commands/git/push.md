---
description: main 브랜치를 origin에 push
allowed-tools: Bash(git:*)
---

# Push 작업

`main` 브랜치의 커밋을 `origin`에 push해 줘.

## 1. 사전 확인

- `git remote -v`로 `origin`이 연결되어 있는지 확인해 줘.
  - 연결되어 있지 않으면 push하지 말고 알려 줘.
- `git status`로 커밋되지 않은 변경 사항이 있는지 확인해 줘.
  - 있으면 push 전에 알려 줘. (커밋은 하지 않음)
- 로컬에 `main` 브랜치가 없으면 push하지 말고 알려 줘.

## 2. Push

- 원격에 `main` 브랜치가 아직 없으면 upstream을 설정해서 push해 줘.

```bash
git push -u origin main
```

- 이미 upstream이 설정되어 있으면 그냥 push해 줘.

```bash
git push origin main
```

## 주의 사항

- `--force` 등 강제 push는 사용하지 마.
- push가 거부되면(원격에 새 커밋이 있는 경우 등) 임의로 pull·rebase하지 말고, 원인을 알려 준 뒤 어떻게 할지 물어봐 줘.