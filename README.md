# 골프 내기 정산기 (웹앱)

타당 내기와 홀당 내기를 정산하는 휴대폰용 웹앱입니다.
설치 후에는 인터넷이 없어도 동작하고, 스코어와 골프장 정보는 각자의 폰에만 저장됩니다.

## 들어 있는 파일

| 파일 | 역할 |
|---|---|
| index.html | 앱 본체 (화면과 계산 전부) |
| manifest.webmanifest | 홈 화면 설치용 정보 (이름, 아이콘, 색) |
| sw.js | 오프라인 동작용 |
| icon-192.png, icon-512.png, apple-touch-icon.png | 앱 아이콘 |

## 처음 올리기 (GitHub Pages, 무료)

1. github.com 에서 무료 계정을 만듭니다.
2. 오른쪽 위 **+** → **New repository** 를 누릅니다.
   - Repository name: 예) `golf-bet`
   - **Public** 선택 → **Create repository**
3. 새 저장소 화면에서 **uploading an existing file** 링크를 누릅니다.
4. 압축을 푼 파일 7개(이 README 포함)를 끌어다 놓고, 아래 **Commit changes** 를 누릅니다.
5. 저장소 위쪽 **Settings** → 왼쪽 메뉴 **Pages** 로 갑니다.
   - Source: **Deploy from a branch**
   - Branch: **main**, 폴더 **/(root)** → **Save**
6. 1~2분 뒤 같은 화면 위쪽에 주소가 나옵니다.
   예) `https://내아이디.github.io/golf-bet/`

GitHub 화면의 버튼 이름이나 위치는 바뀔 수 있습니다. 비슷한 이름을 찾으면 됩니다.

## 폰에 설치하기

- **iPhone**: Safari로 주소 열기 → 아래 공유 버튼 → **홈 화면에 추가**
- **Android**: Chrome으로 주소 열기 → 오른쪽 위 메뉴 → **앱 설치** 또는 **홈 화면에 추가**

동반자에게는 주소만 보내면 각자 같은 방법으로 설치할 수 있습니다.

## 고친 버전 올리기

1. 저장소에서 바꿀 파일(보통 `index.html`)을 다시 **Add file → Upload files** 로 올리고 Commit 합니다.
2. 1~2분 뒤 반영됩니다. 폰에서는 인터넷이 연결된 상태로 앱을 한 번 열면 새 버전을 받습니다.
3. 아이콘이나 manifest를 바꿨다면 `sw.js` 맨 위의 `VERSION` 값을 `golf-v2`처럼 올려 주세요.

## 알아둘 점

- 데이터(스코어, 저장한 골프장)는 **폰마다 따로** 저장됩니다. 앱을 지우거나 브라우저 데이터를 지우면 함께 사라집니다.
- 저장소가 Public이라 코드는 누구나 볼 수 있지만, 스코어 같은 개인 데이터는 저장소에 올라가지 않습니다.
- Claude 버전에 있던 **스코어카드 사진 읽기는 빠져 있습니다.** 시작 화면의 "새 골프장 직접 입력"으로 입력하고 "골프장 저장"을 눌러 두세요.
