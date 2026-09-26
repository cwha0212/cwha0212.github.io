# 프로필 수정 안내

블로그 프로필을 바꿀 때 수정할 파일과 항목입니다.

| 바꿀 내용 | 수정 위치 | 설정 |
| --- | --- | --- |
| 사이트 이름 | `_config.yml` | `title` |
| 사이드바 소개 문구 | `_config.yml` | `tagline` |
| 검색·공유용 사이트 설명 | `_config.yml` | `description` |
| 저자 이름·이메일 | `_config.yml` | `social.name`, `social.email` |
| GitHub 사용자명 | `_config.yml` | `github.username` |
| 사이드바 연락처 아이콘과 링크 | `_data/contact.yml` | 항목의 `type`, `icon`, `url` |
| 정보 페이지 본문 | `_tabs/about.md` | Markdown 본문 |
| 사이트 전체 공유 미리보기 이미지 | `_config.yml` | `social_preview_image` |
| 특정 글의 미리보기 이미지 | 해당 `_posts/*.md` | Front matter의 `image` |
| 브라우저·모바일 앱 아이콘 | `assets/img/favicons/` | 아래 아이콘 파일들 |

## 프로필 사진

프로필 사진은 `assets/img/profile/avatar.png`에 있습니다. `_config.yml`의 `avatar`에는 사이트의 절대 URL을 지정합니다. 현재 `cdn` 설정이 상대 이미지 경로에 접두사를 붙이므로, 절대 URL은 CDN에 잘못 연결되는 것을 방지합니다.

```yml
avatar: "https://cwha0212.github.io/assets/img/profile/avatar.png"
```

이후 사진을 바꿀 때 같은 경로의 `avatar.png`만 교체하면 됩니다.

## 사이트 아이콘

- `assets/img/favicons/favicon.svg`: 최신 브라우저 탭 아이콘
- `assets/img/favicons/favicon-96x96.png`: PNG 파비콘
- `assets/img/favicons/favicon.ico`: 구형 브라우저 및 RSS 아이콘
- `assets/img/favicons/apple-touch-icon.png`: iPhone·iPad 홈 화면 아이콘
- `assets/img/favicons/web-app-manifest-192x192.png`: PWA 설치 아이콘
- `assets/img/favicons/web-app-manifest-512x512.png`: 큰 화면용 PWA 설치 아이콘
- `assets/img/favicons/site.webmanifest`: PWA 이름, 색상, 아이콘 연결 설정

아이콘을 교체할 때는 기존 파일명과 각 이미지 크기를 유지하세요. 프로필 아이콘의 종류와 실제 URL은 `_data/contact.yml`에서 관리합니다. 새 연락처를 추가할 때는 `type`, Font Awesome `icon`, 실제 프로필 `url`을 함께 지정하세요.