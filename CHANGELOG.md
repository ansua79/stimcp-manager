# 변경 이력 (Changelog)

이 프로젝트의 주요 변경 사항을 한 곳에 누적 기록합니다.
형식은 [Keep a Changelog](https://keepachangelog.com/ko/1.1.0/), 버전은 [유의적 버전](https://semver.org/lang/ko/)을 따릅니다.

## [0.1.1] - 2026-06-23

### 변경
- 포터블·설치형 **모두 설정을 `%APPDATA%\kr.kisti.stimcpmanager\` 에 저장**하도록 통일. (포터블 실행 시 exe 옆에 `data` 폴더가 생기던 동작 제거)

### 추가
- **API 키(비밀값) 입력 검증**: 앞뒤 공백 자동 제거, 값에 공백·탭·개행·비가시(제로폭/제어) 문자가 포함되면 경고 표시 + 동작 테스트·저장 차단. (`-` `_` `.` `+` `/` `=` 등 특수문자는 정상 허용)
- **식별자 형식 검증**: 서버명(영숫자·`_`·`-`), ID(kebab-case), 환경변수 이름(영문/밑줄로 시작).

### 수정
- 클라이언트 등록 시 환경변수 값의 앞뒤 공백을 제거해 기록 (이전에 저장된 항목도 등록 시점에 정리).

## [0.1.0] - 2026-06-23

### 추가
- 최초 릴리스.
- 기본 카탈로그(KISTI · ScienceON · AI Hub · KIPRIS 등)에서 선택해 환경변수 입력 후 추가.
- 사용자 카탈로그: GitHub URL로 MCP 추가(`git clone` 후 폼 자동 채움), 동작 테스트(`initialize` + `tools/list`).
- 클라이언트 적용: 선택한 MCP를 Claude Desktop · VS Code 설정 파일에 백업 후 등록.
- 내 MCP: 클라이언트 설정 파일을 읽어 현재 설치된 MCP 표시 · 복원 · 초기화 · 삭제.

[0.1.1]: https://github.com/ansua79/stimcp-manager/releases/tag/v0.1.1
[0.1.0]: https://github.com/ansua79/stimcp-manager/releases
