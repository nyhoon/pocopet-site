# PocoPet 공개 정책 사이트

**앱 소스(`MobilePet`)는 Private** — 이 폴더만 **Public** 저장소로 올려 Play·Search Console용 URL을 씁니다.

## 배포 상태

- 원격: https://github.com/nyhoon/pocopet-site
- 로컬 push: `MobilePet` 루트에서 `.\scripts\deploy\push_pocopet_site.ps1`

## Pages 설정 (한 번만)

[Settings → Pages](https://github.com/nyhoon/pocopet-site/settings/pages)

| 항목 | 값 |
|------|-----|
| Source | **Deploy from a branch** |
| Branch | **main** |
| Folder | **`/ (root)`** |

저장 후 1~3분 뒤: https://nyhoon.github.io/pocopet-site/

## 처음 올릴 때 (새 PC)

1. 이 폴더에서 `git clone` 하거나 `MobilePet` 안의 `pocopet-site/` 사용
2. `.\scripts\deploy\push_pocopet_site.ps1` (경로는 `MobilePet` 루트 기준)

## Play Console · Search Console URL

| 용도 | URL |
|------|-----|
| 조직 기본 웹사이트 (Search Console과 동일) | `https://nyhoon.github.io/pocopet-site/` |
| 개인정보처리방침 | `https://nyhoon.github.io/pocopet-site/legal/privacy-policy.html` |
| 계정 삭제 | `https://nyhoon.github.io/pocopet-site/legal/account-deletion.html` |
| AdMob `app-ads.txt` | `https://nyhoon.github.io/pocopet-site/app-ads.txt` |

## 내용 수정

1. `MobilePet`의 `docs/` 또는 `docs/legal/` 수정
2. 프로젝트 루트에서:

```powershell
.\scripts\deploy\sync_pocopet_site_from_docs.ps1
```

3. `pocopet-site` Public 저장소에 push

정본 설명: [`docs/PRIVACY_POLICY_HOSTING.md`](../docs/PRIVACY_POLICY_HOSTING.md)
