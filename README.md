# 포트폴리오 템플릿 (GitHub Pages)

작업물 폴더를 올리기만 하면 메인 화면에 카드가 자동으로 추가되는 포트폴리오예요.
`index.html`은 처음 한 번 올린 뒤로 고칠 필요가 없어요.

## 처음 한 번만

1. GitHub에서 `계정이름.github.io` 이름으로 **공개(Public)** 레포를 만들어요.
2. 이 폴더의 `index.html`, `profile.json`을 올려요.
3. `profile.json`에 내 이름, 소개, 링크를 적어요.
4. Settings → Pages → Branch를 `main` / `(root)`로 저장해요.
5. 1~2분 뒤 `https://계정이름.github.io`로 접속해요.

## 작업물 추가하기

작업물 하나 = 폴더 하나예요. **Add file → Upload files**에 폴더를 통째로 끌어다 놓으면 돼요.

```
계정이름.github.io/
├─ index.html          ← 손대지 않아요
├─ profile.json        ← 내 소개
├─ 01-color-palette/   ← 작업물 1
│   ├─ index.html      (웹/게임이면 실제 페이지)
│   ├─ info.json       (카드에 보일 내용)
│   └─ thumb.webp      (카드 그림)
└─ 02-line-graph/      ← 작업물 2
```

- 폴더 이름은 `번호-영어이름` 형식으로 지어요. 번호가 큰 작업물이 맨 앞에 나와요.
- `thumb.png` (또는 .jpg .webp .gif .svg)가 카드 그림이 돼요. 작업물 화면을 캡처해서 넣으면 가장 좋아요. 가로로 긴 그림(16:10)이 좋아요.
- `info.json`이 없으면 `index.html`의 `<title>`이 카드 제목이 돼요.
- `_`나 `.`으로 시작하는 폴더는 카드로 만들지 않아요.

## info.json 쓰는 법

```json
{
  "title": "일차함수 놀이터",
  "summary": "기울기와 y절편을 맞춰 직선 하나로 모든 별을 통과시키는 게임",
  "type": "game",
  "subject": "수학",
  "unit": "일차함수와 그래프",
  "stack": ["HTML", "JavaScript", "SVG"],
  "date": "2026-06",
  "role": "기획, 디자인, 개발 (개인 작업)",
  "color": "#2f6fdf",
  "images": ["thumb.png", "shot-2.png"],
  "link": "",
  "story": ["무엇을 만들었는지 한 문단", "어떻게 쓰는지 한 문단"],
  "learned": ["만들면서 배운 점"]
}
```

| 항목 | 뜻 | 꼭 써야 하나요? |
|---|---|---|
| `title` | 작업물 이름 | 네 |
| `summary` | 한 줄 소개 (카드에 보여요) | 네 |
| `type` | `web` 웹 앱 / `sim` 시뮬레이션 / `game` 게임 / `art` 그림, 디자인 | 네 |
| `subject` | 과목 (카드에 보이고 과목 필터가 생겨요) | 권장 |
| `unit` | 배운 내용, 단원 | 선택 |
| `stack` | 사용한 기술 목록 | 권장 |
| `date` | 만든 달 (`2026-09`) | 권장 |
| `role` | 맡은 일 | 선택 |
| `color` | 카드 포인트 색 | 선택 |
| `images` | 상세 화면에 보여줄 그림들 (폴더 안 파일 이름) | 선택 |
| `link` | 외부 링크 (스크래치, itch.io 등). 비워 두면 폴더의 index.html로 연결 | 선택 |
| `story` | 상세 화면 소개 글 (문단마다 따옴표로 나눠요) | 선택 |
| `learned` | 만들면서 배운 점 | 선택 |

## 참고

- React(Vite)로 만든 작업물은 `vite.config.js`에 `base: './'`를 넣고 빌드한 결과물(dist 안의 파일)을 폴더에 올려요.
- 작업물 목록은 GitHub API로 불러와요. 같은 와이파이에서 1시간에 60번 넘게 열면 잠시 목록이 안 보일 수 있어요.
- 다른 곳에서 미리 보려면 `index.html?repo=계정이름/계정이름.github.io`로 열어요.

