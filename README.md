# INKWAVE 한글판 (inkwave-ko)

[DevFrancois/inkwave](https://github.com/DevFrancois/inkwave)의 한국어 로컬라이즈 버전입니다. 브라우저에서 바로 플레이할 수 있는 4 대 4 터프 워 잉크 슈터입니다.

**플레이:** https://sigco3111.github.io/inkwave-ko/

## 소개

광장을 우리 팀 잉크로 칠하고, 오징어로 변신해 잉크 속을 헤엄치고, 상대 팀을 스플랫하세요. 시간이 끝났을 때 더 넓은 터프를 칠한 팀이 승리합니다. 봇과 함께하는 4 대 4 터프 워를 세 가지 스테이지(타이드워터 광장, 켈프라인 터미널, 홀리야드 마리나)와 낮/황혼 두 시간대로 즐길 수 있습니다.

## 특징

- 무기 7종: 스프리처, 스웰 롤러, 글린트 차저, 팝퍼 블래스터, 트윈핀 듀얼리, 타이드버킷 슬로셔, 자이어 스플랫링
- 서브 무기(스플랫 밤)와 스페셜(타이달 슬램, 잉크 템페스트)
- 오징어키즈 커스터마이즈: 촉수 스타일, 모자, 눈, 눈썹, 피부톤, 옷
- 슈퍼 점프, 미니맵, 팀 라인업, 결과 메달과 XP/레벨 성장
- 키보드+마우스 / 컨트롤러 지원, 난이도 3단계
- 메뉴, HUD, 월드 간판·포스터·표지판까지 전면 한글화

## 스크린샷

(배포 후 추가)

## 설치 및 실행

정적 사이트라 빌드 도구 없이 실행됩니다.

```bash
# 로컬에서 실행 (ES 모듈이라 http 서버 필요)
python3 -m http.server 8000
# http://localhost:8000 접속
```

배포용 산출물 생성:

```bash
python3 tools/build-dist.py   # dist/ 폴더 생성
```

## 기술 노트

- three.js 기반 절차적 생성: 캐릭터, 무기, 스테이지, 잉크, 음악, 효과음 모두 코드로 생성
- 한글화 범위: UI 전체(menus/hud/menu-art/diorama), 설정·무기·스테이지·캐릭터 데이터(config/character-style), 게임 피드·프롬프트(main), 캔버스 벽화(murals), 소품 텍스처 아틀라스의 표지판·포스터(props)
- 한글 폰트: Noto Sans KR(Google Fonts) — CSS와 캔버스 렌더링 모두 폰트 스택에 추가
- 예외: 홀리야드 마리나의 선체·부두 3D 입체 글자는 커스텀 글리프 빌더가 한글을 지원하지 않아 라틴 유지

## 라이선스 및 크레딧

- 원작: [DevFrancois/inkwave](https://github.com/DevFrancois/inkwave) — Copyright 2026 Jayden Davis, MIT License
- 한글화: sigco3111
- 폰트: Titan One (Font Diner), Rubik (Hubert & Fischer), Noto Sans KR (Google) — SIL Open Font License
