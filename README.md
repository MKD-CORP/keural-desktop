<div align="center">

<img src="assets/logo.svg" width="92" alt="Keural" />

# Keural Desktop

### 내 컴퓨터의 파일을, AI와 함께.

큐럴 데스크톱 앱은 당신의 로컬 파일을 **직접 읽고, 검색하고, 수정**합니다.
업로드도, 복사·붙여넣기도 필요 없습니다 — 폴더 하나만 열어주면 됩니다.

<br/>

### [⬇️  지금 다운로드](https://github.com/MKD-CORP/keural-desktop/releases/latest)

<sub>macOS · Windows · Linux</sub>

<br/>

[![Download](https://img.shields.io/badge/⬇_Download-874dff?style=for-the-badge)](https://github.com/MKD-CORP/keural-desktop/releases/latest)
[![Latest Release](https://img.shields.io/github/v/release/MKD-CORP/keural-desktop?style=for-the-badge&color=3382ff&label=latest)](https://github.com/MKD-CORP/keural-desktop/releases/latest)

</div>

---

## 왜 데스크톱인가요?

| | 웹 | **데스크톱** |
|---|:---:|:---:|
| 파일 분석 | 업로드 필요 | **내 폴더 직접 접근** |
| 코드·문서 탐색 | — | **grep으로 즉시 검색** |
| 파일 수정 | — | **승인 후 바로 저장** |
| 프라이버시 | 서버 업로드 | **허용한 경로만, 로컬에서** |

> 큐럴이 클루드 코드처럼 작동합니다 — `local_list`로 둘러보고, `local_grep`으로 찾고, 필요한 부분만 `local_read`로 읽은 뒤, 당신이 승인하면 `local_write`로 고칩니다.

## 다운로드

최신 버전은 **[GitHub Releases](https://github.com/MKD-CORP/keural-desktop/releases/latest)** 에서 받을 수 있습니다. 아래 표에서 플랫폼별 파일을 바로 받아도 됩니다.

| 플랫폼 | 아키텍처 | 직접 다운로드 |
|---|---|---|
| 🍎 **macOS** | Apple Silicon (M1 이상) | [Keural-mac-arm64.dmg](https://github.com/MKD-CORP/keural-desktop/releases/latest/download/Keural-mac-arm64.dmg) |
| 🍎 **macOS** | Intel | [Keural-mac-x64.dmg](https://github.com/MKD-CORP/keural-desktop/releases/latest/download/Keural-mac-x64.dmg) |
| 🪟 **Windows** | 64-bit | _준비 중_ |
| 🐧 **Linux** | x86_64 | _준비 중_ |

## 설치

<details>
<summary><b>🍎 macOS</b></summary>

1. `.dmg`를 열고 **Keural**을 응용 프로그램 폴더로 드래그
2. 최초 실행 시 차단되면 **시스템 설정 → 개인정보 보호 및 보안 → "확인 없이 열기"**
</details>

<details>
<summary><b>🪟 Windows</b></summary>

1. `.exe` 실행
2. SmartScreen 경고 시 **추가 정보 → 실행**
</details>

<details>
<summary><b>🐧 Linux</b></summary>

```bash
chmod +x Keural-linux-x86_64.AppImage
./Keural-linux-x86_64.AppImage
```
</details>

---

<details>
<summary><b>🛠 관리자 — 새 버전 배포</b></summary>

> ⚠️ 설치 파일은 100MB가 넘으므로 **레포에 커밋하지 않습니다.** GitHub **Releases**(에셋 최대 2GB)에 업로드하세요. 다운로드 링크는 `releases/latest/download/<고정파일명>`이라 버전이 올라가도 깨지지 않습니다.

1. `mkd-keural-next-fe-chat`에서 빌드 (산출물은 `release/`, git 추적 안 됨):
   ```bash
   yarn electron:build
   ```
2. 산출물을 **고정 파일명**으로 바꿉니다 (다운로드 페이지·링크가 이 이름을 참조):
   | 빌드 산출물 | → 업로드 이름 |
   |---|---|
   | `Keural-<ver>-arm64.dmg` | `Keural-mac-arm64.dmg` |
   | `Keural-<ver>.dmg` | `Keural-mac-x64.dmg` |
   | `Keural-<ver>-setup.exe` | `Keural-win-x64.exe` |
   | `Keural-<ver>.AppImage` | `Keural-linux-x86_64.AppImage` |
3. [새 Release 생성](https://github.com/MKD-CORP/keural-desktop/releases/new) → 태그(예: `v0.1.0`) → 위 파일들을 에셋으로 첨부 → Publish.
4. **GitHub Pages 활성화** (최초 1회): *Settings → Pages → Source: `main` / `/ (root)`* → `https://mkd-corp.github.io/keural-desktop/`

> 웹 앱(`mkd-keural-next-fe-chat`)의 설치 버튼·안내 모달은 `NEXT_PUBLIC_APP_DOWNLOAD_URL`이 이 다운로드 페이지를 가리킵니다.
> macOS는 현재 미서명입니다 — 정식 배포 시 Apple Developer 인증서로 서명·공증(notarization)을 권장합니다.
</details>

<div align="center"><sub>© MKD · Keural Desktop</sub></div>
