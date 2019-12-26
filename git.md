# Git ( 큰 제목은 # 1개)

> Git은 분산버전관리시스템(DVCS)이다. (오른쪽 꺽새 사용, >)
>
> (파이썬이 객체지향프로그램이다. 객체라는 개념에 대해서 준비하기)
>
> 소스코드의 버전 및 이력을 관리할 수 있다.

## 준비하기 ( ## )

윈도우에서 git을 활용하기 위해서 [git.bash](https://gitforwindows.org)를 설치한다.

git을 활용하기 위해서 GUI 틀인 `source tree`,` github desktop`,`desktop`등을 활용할 수도 있다.

초기 설치를 완료한 이후에 컴퓨터에 author 정보를 입력한다. 이메일 정보를 `github`에 가입된 이메일로 일치시켜야 커밋 이력들이 관리한다.

```bash
$ git config --global user_name edutak
$ git config --global user.email
20152201@soongsil.ac.kr
```

# 로컬 저장소(repository) 활용하기

### 1. 저장소 초기화 ( ### )

```bash
$ git init
Initialized empty Git repository in C:/Users/student/Desktop/TIL/.git/
(master) $
```

* `.git` 폴더가 생성되며, 여기에 git과 관련된 모든 정보가 저장된다.

* git bash에 `(master)`라고 표현되는데, 이는 master 브랜치에 있다는 뜻이다.

  

### 2. add

`working directory`,  즉 작업 공간에서 변경된 사항을 이력으로 저장하기 위해서는 반드시 `staging area`를 거쳐야한다.

```bash
$ git add markdown.md # 특정 파일
$ git add images/ # 특정 폴더
$ git add . # 현재 디렉토리
```

* add 전 상태

  ```bash
  $ git status
  On branch master
  
  No commits yet
  
  # 트래킹 되고 있지 않는 파일들
  # => commit 이력에 한번도 담기지 않은 파일들
  Untracked files:
  # 커밋될 것들에 포함시키려면 add 명령어를 사용해
    (use "git add <file>..." to include in what will be committed)
          git.md
  
  # 아직 커밋될 것들은 없지만,
  # untracked files은 존재한다.
  nothing added to commit but untracked files present (use "git add" to track)
  ```

* add 후 상태

  ```bash
  $ git add images/
  $ git status
  On branch master
  
  No commits yet
  
  Untracked files:
    (use "git add <file>..." to include in what will be committed)
          git.md
  
  nothing added to commit but untracked files present (use "git add" to track)
  ```

  