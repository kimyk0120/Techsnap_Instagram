# 📰 Techsnap - Instagram IT 뉴스 자동 요약 포스터

**Techsnap**은 최신 IT 뉴스를 자동으로 요약하고, Instagram 비즈니스 계정에 정기적으로 업로드하는 Python 기반 자동화 프로젝트입니다.


## 📌 주요 기능

### ✅ 뉴스 수집 및 요약
- IT 매거진 사이트 RSS에서 기사 링크 수집
- 중복 포스팅 방지를 위한 JSON 기반 링크 저장/비교
- OpenAI ChatGPT API를 사용하여:
  - **요약 제목 생성**
  - **본문 요약**
- 해시태그 파일 자동 생성

### ✅ 이미지 생성 및 업로드
- 템플릿 이미지에 뉴스 요약을 삽입하여 카드뉴스 스타일 이미지 생성
- 생성된 이미지를 Cloudinary에 업로드하여 `image_url` 확보

### ✅ Instagram 포스팅
- Instagram Graph API를 이용해 `image_url` 기반 포스트 게시
- Instagram 서버로 이미지 복사 완료 후, Cloudinary 이미지 삭제 처리

### ✅ 자동화 스케줄링
Crontab을 활용한 자동 실행 설정:

## 📁 프로젝트 구조
```
automation_proj/
├── main.py                  # 전체 자동화 주 로직
├── refresh_token.py         # Instagram Access Token 갱신
├── image_generator.py       # 템플릿 이미지 생성
├── instagram_api.py         # Instagram 업로드 기능
├── cloudinary_api.py        # Cloudinary 업로드 및 삭제 기능
├── summarizer.py            # GPT 기반 뉴스 요약
├── rss_parser.py            # RSS 파싱 및 중복 검사
├── log/                     # 실행 로그 및 JSON 저장
└── ...
```

## 🛠 사용 기술
- Python 3.10
- Instagram Graph API
- Cloudinary API
- OpenAI GPT API
- RSS Feed Parsing
- Linux Crontab

## 📎 링크
- 📸 Instagram 계정: [@Techsnap](https://www.instagram.com/elekodar/) 


