# PocoPet 공개 정책 사이트

**앱 소스(`MobilePet`)는 Private** — 이 폴더만 **Public** 저장소로 올려 Play·Search Console용 URL을 씁니다.

## 배포 (5분)

1. GitHub에서 **새 Public 저장소** 생성 (이름 예: `pocopet-site`)
2. 이 폴더 **안의 파일만** 저장소 루트에 push (`index.html`, `legal/`, `.nojekyll`)
3. **Settings → Pages** → Source: **Deploy from a branch** → Branch `main` → Folder **`/ (root)`**
4. 몇 분 후 접속: `https://nyhoon.github.io/pocopet-site/`

## Play Console · Search Console URL

| 용도 | URL |
|------|-----|
| 조직 기본 웹사이트 (Search Console과 동일) | `https://nyhoon.github.io/pocopet-site/` |
| 개인정보처리방침 | `https://nyhoon.github.io/pocopet-site/legal/privacy-policy.html` |
| 계정 삭제 | `https://nyhoon.github.io/pocopet-site/legal/account-deletion.html` |

## 내용 수정

1. `MobilePet`의 `docs/` 또는 `docs/legal/` 수정
2. 프로젝트 루트에서:

```powershell
.\scripts\deploy\sync_pocopet_site_from_docs.ps1
```

3. `pocopet-site` Public 저장소에 push

정본 설명: [`docs/PRIVACY_POLICY_HOSTING.md`](../docs/PRIVACY_POLICY_HOSTING.md)
