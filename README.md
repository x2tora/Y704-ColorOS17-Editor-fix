# Y704 ColorOS 17 Editor Fix

Lenovo Legion Y700 4세대의 ColorOS 17 포팅 롬에서 기본 갤러리의 사진·동영상 편집기가 강제 종료되는 문제를 해결하는 KernelSU 모듈입니다.

## 테스트 환경

- Lenovo Legion Y700 4세대 (Y704)
- [Y704_Color17_Global_v1.24](https://gall.dcinside.com/mgallery/board/view/?id=andtabcus&no=24934)
- 빌드 `OPD2415_17.0.0.103(EX01)`
- KernelSU와 시스템 파일 마운트를 지원하는 메타모듈

KernelSU v3.3.1과 meta-overlayfs v1.3.1 조합에서 테스트했습니다. 다른 ROM과 기기에서는 동작을 확인하지 않았습니다.

## 설치

### 1. 마운트 메타모듈 준비

KernelSU에서 모듈 탭을 열고 마운트 메타모듈이 활성화되어 있는지 확인합니다.

설치되어 있지 않다면 다음 순서로 설치하세요.

1. [meta-overlayfs 릴리스 페이지](https://github.com/KernelSU-Modules-Repo/meta-overlayfs/releases)에서 ZIP을 다운로드합니다.
2. KernelSU의 모듈 탭에서 `+` 버튼을 눌러 다운로드한 ZIP을 선택합니다.
3. 설치가 끝나면 기기를 재부팅합니다.

이미 마운트 메타모듈을 사용하고 있다면 이 단계를 건너뛰세요.

### 2. Y704 Editor Fix 설치

1. [Releases](https://github.com/x2tora/Y704-Editor/releases)에서 모듈 ZIP을 다운로드합니다.
2. KernelSU의 모듈 탭에서 `+` 버튼을 눌러 다운로드한 ZIP을 선택합니다.
3. 설치가 끝나면 기기를 재부팅합니다.
4. 기본 갤러리에서 사진과 동영상 편집기를 열어 확인합니다.

## 알려진 문제

- 동영상 필터 목록의 미리보기가 초록색으로 표시됨

## 제거

KernelSU 모듈 탭에서 **Y704 Meishe Filter Restore**를 끄거나 제거한 뒤 재부팅합니다.

## 출처

이 모듈에는 OnePlus Pad 3 순정 펌웨어에서 추출한 Meishe 필터 라이브러리와 LUT가 포함되어 있습니다. 해당 바이너리의 재배포 허용 여부는 확인되지 않았습니다.
