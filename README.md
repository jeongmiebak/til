# Today I learned

> 매일매일 배운것을 기록합니다

## 2022-09-13

## RPA 1기, 웹프로그래밍 기획과 기본

#### 리눅스 커맨드라인 기초

- `pwd` : print working directory의 약자로 현재 작업 경로를 출력하는 명령어
- `cd` : change directory의 약자로 작업경로를 변경할 때 쓰는 명령어
  - 절대 경로는 `/`로 시작함
  - 상위경로는 `..`로 나타냄
  - tab을 사용하면 경로 자동완성이 됨
- `ls` : list의 약자로 현재 작업경로에 있는 파일이나 디렉터리를 출력하는 명령어
  - `ls -a`, `ls-l`, `ls-al` 과 같은 옵션을 붙일수 있음
- `history` : 과거에 입력했던 명령어 리스트를 보여줌
  - 123번째 명령어를 복구하고 싶으면 `!123` 입력

#### vim 사용법

- 명령 모드와 입력 모드
  - vim 에디터를 열때는 명령 모드로 진입함
  - 명령 모드에서는 입력이 불가능
  - 입력하려면 입력모드로 변경해야 함
    - 키보드에서 `i` 누름
  - 입력이 꿑나고 저장후 나오려면 명령모드로 변경해야 함
    - 키보드에서 `esc` 누름
  - 입력 가능한 명령어
    - :`w` : 저장
    - :`q` : 나오기
    - :`wq` : 저장하고 나오기
  - 참고자료 [링크] (https://zeddios.tistory.com/122)
- 비정상적으로 종료시 해결방법
  - vim 이 비정상 종료되었을때 `swp`파일이 생성됨
    - attention 문구가 뜨는 경우
      1. 두 프로세스, 두사람이 동시에 한파일을 수정하는 경우
      2. crash가 나서 vim이 비 정상적으로 닫힌 경우
  - 기존에 입력했던 내용을 복구하고 싶을떄는 `vim -r 파일명`을 입력하거나 recovery 모드로 진입
  - 정상 종료 후, `swp` 파일 삭제
    - `rm .4.txt,swp` 로 삭제

#### 마크다운 문법

- 외부 링크 추가

```
사용문법: [Title](link)
적용예: [Google](https://google.com, "google link")
```

Link: [Google](https://google.com, "google link")

#### 버전 관리 시스템과 git

#### 버전 관리 시스템을 사용하는 이유

1. 실행 취소, 재 실행이 가능
2. 버전간 소스코드 비교가 가능
3. 협업이 쉬워짐

#### 다양한 버전관리 방법

이름 변경하기 좋은 방법이 있는데, 개발할때는 git을 주로 사용함

#### 커밋

- 커밋은 논리적 변경이 있을때 만듬
- 가능하면 커밋 크기가 작을수록 좋음

##### 커밋 이력보기

```
git log
```

##### 리포지토리

- 정의 : 여러 파일을 하나로 모은 컬렉션
- 일반 디렉터리와 리포지토리의 차이 : .git 디렉터리의 유무

##### 로컬에서 리포지토리 생성

```
git init
```
