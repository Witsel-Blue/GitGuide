# Git Guide

## I. Git 정의

### Git?
분산 버전 관리 시스템(DVCS)

소프트웨어 개발 과정에서 소스 코드의 변경 사항을 추적하고 관리하는 데 사용

### GitHub?
git 을 기반으로 한 웹 호스팅 서비스


로컬 디렉토리 - 로컬 저장소 - 원격 저장소(gitHub)

		add&commit	push


## II. Git 설치
1. 터미널 git 설치
2. GitHub에 새 저장소 생성
3. 생성된 저장소 주소 복사
4. 초기 설정
	Git config —global user.name “name”

	Git config -g user.email “email”
5. 파일 준비
	git init

	git add .

	git status

	git commit -m “message”
6. 업로드
	git remote add origin {3}

	git push -u origin master


## III. Git 명령어
### Clone
* 저장소 복제

	: Git clone <저장소 url>

* 원격 저장소 추가

	: Git remote add <원격 저장소> <저장소 url>

* 원격 저장소명 확인

	: Git remote


### Pull
* 원격 저장소에서 현재 브랜치 합치기

	: Git pull <원격 저장소>

* Origin 에서 현재 브랜치 합치기

	: Git pull


### Add Commit
* 파일 변경사항 로컬에 저장

	: Git add <파일명>

	: Git add . (전체 저장)

	: Git commit -m “<메세지>” 

* Add 취소

	: Git rm —cached <파일명>

* Commit 로그 확인

	: Git log


### Push
* 로컬 브랜치에서 원격 저장소

	: Git push <원격 저장소> <로컬 브랜치>


## IV. Branch
### Branch
코드를 통째로 복사한 후, 원래 코드에 영향을 주지않고 독립적으로 개발

### Workflow
* Fork

	: 타인 소유 원격 저장소 구조 복사 > 내 소유 원격 저장소 생성

* Clone

	: 원격 저장소 > 로컬 저장소

	: Git clone <원격 저장소 url>

* 로컬 저장소에 원본 등록

	: git remote add <생성 폴더명 or upstream> <원본 원격 저장소 url>

	: git fetch -a (upstream 저장소의 commit 내역 불러오기)

* Branch

	: 수정 단위 생성

	: git branch <branch name>

* Commit

	: 로컬 디렉토리 > 로컬 저장소

* Push

	: 로컬 저장소 > 원격 저장소

	: git push <로컬 저장소> <브랜치 이름>

* Fetch

	: 협업자의 원격 저장소 commit 내역 반영

	: git fetch upstream

* Pull request

	: commit 내역을 원격 저장소에 반영해줄 것 요청


### Branch 명령어
* 지역 브랜치 목록 보기

	: Git branch

* 원격 브랜치 목록 보기

	: Git branch -r

* 브랜치 생성

	: Git branch <branch name>

* 브랜치 이동

	: Git checkout <branch name>

* 브랜치 병합

	: Git merge <branch name>

* 병합 취소

	: Git merge —abort

* 브랜치 삭제

	: Git branch -d <삭제할 branch>


### Commit Message
* FEAT: 기능 추가
* FIX: 버그 수정
* DOCS: 문서 수정
* STYLE: 스타일 관련
* REFACTOR: 리펙토링
* TEST: 테스트
* CHORE: 빌드, 패키지 매니저 수정