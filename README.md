# TIL

> 오늘 배운 것을 기록합니다.

1. git 특강 (220517~220518)

# 1. GIT 설치

[깃설치 ](https://git-scm.com/downloads)https://git-scm.com/downloads

설치 후

1. C:/사용자(Users)/현재 사용자 계정으로 이동합니다.
2. 폴더 내 빈 공간에 마우스 우 클릭 Git Bash Here 클릭

> 깃의 목표 : 백업 , 복구 , 협업

# 2. GUI vs CLI 차이

![](https://velog.velcdn.com/images/programmerpark94/post/831218c3-aa0f-4b69-bc5e-db0b51c336dd/image.png)

- GUI : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식
- CLI(Command Line Interface) : 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식

인터페이스는 ?

> 사용자와 컴퓨터가 서로 소통하는 접점 이다.

---

CLI를 사용하는 이유는?

> GUI에서 폴더를 만들려면 4단계를 거치는데
> CLI는 mkdir test2 라고 치면 한번에 폴더가 생성된다.

윈도우의 cmd는 왜 안쓰나?

> 맥이랑 윈도우랑 명령어를 통일하기 위해서 git bash 를 쓴다.
> UNIX 계열 운영체제의 터미널 명령어를 연습

# 3.경로

1. 루트 홈 디렉토리(루트디렉토리)

- 모든 파일과 폴더를 담고 있는 최상위 폴더 이다.
- windows 경우 c 드라이브를 의미

2. 홈 디렉토리(~)

- Tilde(틸드) 라고도 부르며 현재 로그인된 사용자의 홈 폴더 의미
- windows 경우 c:\사용자(Users)/현재사용자 계정 의미

폴더 vs 디렉토리

> 폴더와 디렉토리는 거의 같은 의미로 사용된다. 따라서 구분은 무의미 하다.

3.  절대 경로와 상대 경로

    - 절대 경로 : 루트 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것

      > C:Users/kyle/Desktop

    - 상대 경로 : 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것

    > ./ 는 현재 작업하고 있는 폴더를 의미한다
    > ../ 는 현재 작업하고 있는 폴더의 부모 폴더를 의미한다.

# 4. 터미널 명령어

1. touch

- 파일을 생성하는 명령어
- 띄어쓰기로 구분하여 여러 파일을 한꺼번에 생성할 수 있다.
- 숨김 파일을 만들기 위해서 . 을 파일 명 앞에 붙인다.

> $ touch text.txt

2. mkdir

- 새 폴더를 생성하는 명령어
- 띄어쓰기로 구분하여 여러 파일을 한꺼번에 생성 가능
- 폴더 이름 사이 공백을 넣고 싶다면 따옴표

> $ mkdir foler
> $ mkdir 'happy hacking'

3. ls

- list segments
- 현재 작업 중인 디렉토리의 폴더/파일 목록을 보여주는 명령어
- ls -a : all 옵션 , 숨김 파일까지 모두 보여줌
- ls -l : long 옵션 , 용량 , 수정 날짜 등 파일 정보를 자세히 보여준다.

4. mv

- 폴더/ 파일을 다른 폴더 내로 이동 하거나 이름 변경하는 명령어
- 이동할때 반드시 폴더가 반드시 있어야 한다. 없으면 이름이 바뀐다

> $ mv text.txt foler
> $ mv text1.txt text2.txt 파일의 이름을 바꾼다

5. cd

- change directory
- 현재 작업중인 디렉토리를 변경하는 명령어
- cd ~ 입력 홈 디렉토리로 이동한다. 단순히 cd라고만 쳐도 된다.
- cd .. 부모 디렉토리로 이동한다.(위로가기)
- cd - 입력 바로 전 디렉토리로 이동한다.(뒤로가기)

> $ cd folder 현재 작업중인 디렉토리에 있는 folder 폴더로 이동
> $ cd C:/Users/kyle/Desktop 절대 경로를 통한 디렉토리 변경
> $ cd ../parent/child 상대 경로를 통한 디렉토리 변경

6. rm

- remove
- 폴더 / 파일을 지우는 명령어
- GUI 와 달리 휴지통으로 이동하지 않고 바로 삭제 된다.
- - 를 사용하여 rm \*.txt 라고 입력하면 txt파일 전체 삭제
- -r : recursive 옵션 . 폴더를 지울 때 사용한다.

> $ rm test.txt
> $ rm -r folder

7. start , oepn

- 폴더 파일을 여는 명령어
- window 에서 start , mac 에서 open

# Vscode 터미널 사용

지금까지 Git Bash 를 사용했지만 작업 폴더를 직접 옆에 띄워 놓고 수업을 진행했다

이제부터 vscode에서 해보려고 한다.

(1) 단축키 ctrl + `(빽키)

![](https://velog.velcdn.com/images/programmerpark94/post/45e6cbda-8792-4eba-8276-83a911d7f87c/image.png)

![](https://velog.velcdn.com/images/programmerpark94/post/70e5b73b-ae76-4aa6-b736-974ec7327d47/image.png)

(2) vscode 에서 터미널 명령어 사용해보기

- CLI 수업에서 학습했던 터미널 명령어를 vscode에서 실습한다.
- 터미널에서 명령어를 입력했을때 왼쪽 파일 트리의 변화를 관찰한다.

```

fight@DESKTOP-QV1UB26 MINGW64 ~
$ git --version
git version 2.33.0.windows.2

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mkdir test2

fight@DESKTOP-QV1UB26 MINGW64 ~
$ pwd
/c/Users/fight

fight@DESKTOP-QV1UB26 MINGW64 ~
$ ^C

fight@DESKTOP-QV1UB26 MINGW64 ~
$ .
bash: .: filename argument required
.: usage: . filename [arguments]

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd .

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd ..

fight@DESKTOP-QV1UB26 MINGW64 /c/Users
$ pwd
/c/Users

fight@DESKTOP-QV1UB26 MINGW64 /c/Users
$ cd ~

fight@DESKTOP-QV1UB26 MINGW64 ~
$ touch a.txt

fight@DESKTOP-QV1UB26 MINGW64 ~
$ touch b.txt c.txt d.txt

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mkdir test

fight@DESKTOP-QV1UB26 MINGW64 ~
$ ls
'3D Objects'/
 AppData/
 AppMods/
'Application Data'@
 BITUSER.sql
 BITUSER1.sql
 Contacts/
 Cookies@
 Desktop/
 Documents/
 Downloads/
 Example.sql
 Favorites/
 HR~2.sql
 IdeaProjects/
 IntelGraphicsProfiles/
 Links/
'Local Settings'@
 Music/
'My Documents'@
 NTUSER.DAT
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TM.blf
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000001.regtrans-ms
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000002.regtrans-ms
 NetHood@
 Nox_share/
 OneDrive/
 Oracle/
 Pictures/
 PrintHood@
 Recent@
'Recorded Calls'/
 SEARCHID.sql
 SQLPLUS
'Saved Games'/
 Searches/
 SendTo@
 StudentDB.sql
 Templates@
 Videos/
 a.txt
 afiedt.buf
 b.txt
 c.txt
 d.txt
 d4ac4633ebd6440fa397b84f1bc94a3c.7z
 energy-report.html
 git/
 hsperfdata_fight/
 inittk.ini
 inst.ini
 logs/
 mercurial.ini
 ntuser.dat.LOG1
 ntuser.dat.LOG2
 ntuser.ini
 nuuid.ini
 script.sql
 source/
 studentDTO.sql
 test/
 useruid.ini
 vmlogs/
 workspace/
'시작 메뉴'@
'오라클 학습용 PDB서버.sql'
'오라클 학습용 PDB서버1.sql'

fight@DESKTOP-QV1UB26 MINGW64 ~
$

fight@DESKTOP-QV1UB26 MINGW64 ~
$ ls
'3D Objects'/
 AppData/
 AppMods/
'Application Data'@
 BITUSER.sql
 BITUSER1.sql
 Contacts/
 Cookies@
 Desktop/
 Documents/
 Downloads/
 Example.sql
 Favorites/
 HR~2.sql
 IdeaProjects/
 IntelGraphicsProfiles/
 Links/
'Local Settings'@
 Music/
'My Documents'@
 NTUSER.DAT
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TM.blf
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000001.regtrans-ms
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000002.regtrans-ms
 NetHood@
 Nox_share/
 OneDrive/
 Oracle/
 Pictures/
 PrintHood@
 Recent@
'Recorded Calls'/
 SEARCHID.sql
 SQLPLUS
'Saved Games'/
 Searches/
 SendTo@
 StudentDB.sql
 Templates@
 Videos/
 a.txt
 afiedt.buf
 b.txt
 c.txt
 d.txt
 d4ac4633ebd6440fa397b84f1bc94a3c.7z
 energy-report.html
 git/
 hsperfdata_fight/
 inittk.ini
 inst.ini
 logs/
 mercurial.ini
 ntuser.dat.LOG1
 ntuser.dat.LOG2
 ntuser.ini
 nuuid.ini
 script.sql
 source/
 studentDTO.sql
 test/
 useruid.ini
 vmlogs/
 workspace/
'시작 메뉴'@
'오라클 학습용 PDB서버.sql'
'오라클 학습용 PDB서버1.sql'

fight@DESKTOP-QV1UB26 MINGW64 ~
$ ls -a
 ./
 ../
 .3T/
 .BigNox/
 .Ld2VirtualBox/
 .VirtualBox/
 .android/
 .bash_history
 .cache/
 .codetogether/
 .config/
 .ctsystem
 .dbshell
 .eclipse/
 .gitconfig
 .idlerc/
 .lemminx/
 .lesshst
 .m2/
 .mongorc.js
 .node_repl_history
 .oracle/
 .oracle_jre_usage/
 .p2/
 .sts4/
 .swt/
 .tooling/
 .viminfo
 .vscode/
 .webclipse/
 .yarnrc
'3D Objects'/
 AppData/
 AppMods/
'Application Data'@
 BITUSER.sql
 BITUSER1.sql
 Contacts/
 Cookies@
 Desktop/
 Documents/
 Downloads/
 Example.sql
 Favorites/
 HR~2.sql
 IdeaProjects/
 IntelGraphicsProfiles/
 Links/
'Local Settings'@
 Music/
'My Documents'@
 NTUSER.DAT
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TM.blf
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000001.regtrans-ms
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000002.regtrans-ms
 NetHood@
 Nox_share/
 OneDrive/
 Oracle/
 Pictures/
 PrintHood@
 Recent@
'Recorded Calls'/
 SEARCHID.sql
 SQLPLUS
'Saved Games'/
 Searches/
 SendTo@
 StudentDB.sql
 Templates@
 Videos/
 a.txt
 afiedt.buf
 b.txt
 c.txt
 d.txt
 d4ac4633ebd6440fa397b84f1bc94a3c.7z
 energy-report.html
 git/
 hsperfdata_fight/
 inittk.ini
 inst.ini
 logs/
 mercurial.ini
 ntuser.dat.LOG1
 ntuser.dat.LOG2
 ntuser.ini
 nuuid.ini
 script.sql
 source/
 studentDTO.sql
 test/
 useruid.ini
 vmlogs/
 workspace/
'시작 메뉴'@
'오라클 학습용 PDB서버.sql'
'오라클 학습용 PDB서버1.sql'

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mv a.txt
mv: missing destination file operand after 'a.txt'
Try 'mv --help' for more information.

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mv --a.txt
mv: unknown option -- a.txt
Try 'mv --help' for more information.

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mv a.txt /test

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd test

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ ls

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ ls

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ mv a.txt b.txt
mv: cannot stat 'a.txt': No such file or directory

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ cd

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mv b.txt /test

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd .

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd ..

fight@DESKTOP-QV1UB26 MINGW64 /c/Users
$ cd .

fight@DESKTOP-QV1UB26 MINGW64 /c/Users
$ cd

fight@DESKTOP-QV1UB26 MINGW64 ~
$ start .

fight@DESKTOP-QV1UB26 MINGW64 ~
$ ls
'3D Objects'/
 AppData/
 AppMods/
'Application Data'@
 BITUSER.sql
 BITUSER1.sql
 Contacts/
 Cookies@
 Desktop/
 Documents/
 Downloads/
 Example.sql
 Favorites/
 HR~2.sql
 IdeaProjects/
 IntelGraphicsProfiles/
 Links/
'Local Settings'@
 Music/
'My Documents'@
 NTUSER.DAT
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TM.blf
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000001.regtrans-ms
 NTUSER.DAT{9935fe85-1ce5-11ec-a43b-dd8d3020db3b}.TMContainer00000000000000000002.regtrans-ms
 NetHood@
 Nox_share/
 OneDrive/
 Oracle/
 Pictures/
 PrintHood@
 Recent@
'Recorded Calls'/
 SEARCHID.sql
 SQLPLUS
'Saved Games'/
 Searches/
 SendTo@
 StudentDB.sql
 Templates@
 Videos/
 afiedt.buf
 c.txt
 d.txt
 d4ac4633ebd6440fa397b84f1bc94a3c.7z
 energy-report.html
 git/
 hsperfdata_fight/
 inittk.ini
 inst.ini
 logs/
 mercurial.ini
 ntuser.dat.LOG1
 ntuser.dat.LOG2
 ntuser.ini
 nuuid.ini
 script.sql
 source/
 studentDTO.sql
 test/
 useruid.ini
 vmlogs/
 workspace/
'시작 메뉴'@
'오라클 학습용 PDB서버.sql'
'오라클 학습용 PDB서버1.sql'

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mv b.txt test/
mv: cannot stat 'b.txt': No such file or directory

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mv c.txt test/

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd test

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ ls
c.txt

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ mv c.txt d.txt

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ cd

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mkdir test
mkdir: cannot create directory ‘test’: File exists

fight@DESKTOP-QV1UB26 MINGW64 ~
$ rm test
rm: cannot remove 'test': Is a directory

fight@DESKTOP-QV1UB26 MINGW64 ~
$ rm -r test

fight@DESKTOP-QV1UB26 MINGW64 ~
$ mkdir test

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd test

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ touch a.txt

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ mv a.txt b.txt

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ ls
b.txt

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ cd .

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ cd ..

fight@DESKTOP-QV1UB26 MINGW64 ~
$ pwd
/c/Users/fight

fight@DESKTOP-QV1UB26 MINGW64 ~
$ cd test

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$ cd .

fight@DESKTOP-QV1UB26 MINGW64 ~/test
$


[1] Typora 시작하기

  왜 쓰는가?

 - Typora는 마크다운 문법을 읽고 쓰기 위한 일종의 메모장
 - 마크다운 형태로 즉시 변환이 되기 때문에 직관적으로 글 작서잉 가능
 - 이미지 삽입과 관련해서 상당히 편리하다

[2] MarkDown

- 일반 텍스트 기반의 경량 마크업(Markup) 언어이다.
- 마크업과 반대 개념이 아니라 마크업을 더 쉽고 간단하게 사용하고자 만들어졌다
- .md 확장자를 가지며 개발과 관련된 많은 문서 역시 마크 다운 형식으로 만들어 졌다.

> 마크업 이란 ?
마크로 둘러싸인 언어이다.
HTML에서 M의 의미 하는 것은 MarkUp 이다.
즉 HTML 도 마크업 언어 이다.
<h1>제목</h1> 와 같이 작성 한다.
태그라고 할하며 마크 역할을 한다.
각각의 글이 제목 , 내용 , 목록 ,인용 등등  역할을 가지고 표시하는 것이다.

왜 배우나 ? 깃허브에서 사용하기 때문이다.

README.md -> .md 마크다운을 의미한다.

주의
- 글씨의 크기를 키우고 싶다는 이유로 내용에게 제목의 역할을 부여하면 안된다.


# 마크다운 문법

1. 제목

```

# 제목 1

## 제목 2

### 제목 3

#### 제목 4

##### 제목 5

###### 제목 6

```

# 제목1
## 제목2
### 제목3
#### 제목4
##### 제목5
###### 제목6

2. 목록
- 순서가 없는 목록과 순서가 있는 목록을 표현한다.
- 순서가 없는 목록은 _ * + 를 사용한다.
- 순서가 있는 목록은 1. 2. 3. 과 같은 숫자를 사용
- tab 키를 이용해서 들여쓰기를 할 수 있다.


```

- 순서가 없는 목록
  - 서브 목록
  - 서브 목록

* 순서가 없는 목록
  - 서브 목록
  - 서브 목록

- 순서가 없는 목록
  - 서브 목록
  - 서브 목록

1. 순서가 있는 목록

   1. 서브 목록
   2. 서브 목록

1. 혼합 해보기 1
   - 순서 없음
   * 순서 없음
   - 순서 없음
1. 혼합 해보기 2
   1. 순서 있음
   - 순서 없음
   2. 순서 있음

````
- 순서가 없는 목록

    - 서브목록

+ 순서가 없는 목록

    + 서브목록

* 순서가 없는 목록

    * 서브 목록
1. 순서가 있는 목록

    1.서브 목록
    2.서브 목록
2. 혼합 해보기 2
	1. 순서 있음
    - 순서 없음
    2. 순서 있음


3. 강조
- 글자의 스타일링을 표현한다.
1. 기울임 : *글자* 혹은 _글자_
2. 굵게 : **글자** 혹은 __글자__
3. 취소 : ~~글자~~

- 작성
> *이탤릭체1*
_이탤릭체2_
**볼드체1**
__볼드체2__
~~취소선~~

4. 코드
- 한줄 코드인 인라인 코드 와 여러 줄 코드 인 블록 코드로 나뉨
1. 인라인 코드 : `inline` 처럼 백틱을 통해 코드를 감싸줌
2. 블록 코드 : ```python 백틱 3번 입력하여 코드를 작성

- 작성
````

파이썬의 print는 `print("Hello World!")` 과 같이 사용합니다.

```python
for i in range(10):
	print(i)
```

```bash
$ touch test.txt
```

```
Just plain text
```

5. 링크

- 클릭하면 주소로 이동할 수 있는 링크를 의미
- `[표시할이름](이동할주소)` 로 작성한다.
- 작성
  > [GOOGLE](https://google.com) 을 눌러 구글로 이동 하시오

6. 이미지

- 마크 다운 문서에 이미지를 삽입 할 수 있다.
- ![대체텍스트](이미지 주소) 형태로 작성
- 대체 텍스트란 이미지를 정상적으로 불러오지 못했을때 표시되는 문구 이다.

- Typora 에서 이미지 파일을 끌어와서 놓아도 자동 업로드 한다.

- 작성
  > Git 로고 입니다.

```
![Git로고](https://git-scm.com/images/logo@2x.png)
```

![Git로고](https://git-scm.com/images/logo@2x.png)

7. 인용

- 주석이나 인용 문구 표현
- > 를 사용 갯수에 따라 중첩이 가능
- 작성
  > > 인용문을 작성
  > > 중첩된 인용문1
  > >
  > > > 중첩된 인용문2
  > > >
  > > > > 중첩된 인용문3
  > > > >
  > > > > > 중첩된 인용문4

8. 표

| 동물   | 종류   | 다리 개수 |
| ------ | ------ | --------- |
| 사자   | 포유류 | 4개       |
| 닭     | 조류   | 2개       |
| 도마뱀 | 파충류 | 4개       |

9. 수평선

- 구분선을 생성한다.
- -\*\_을 3번 연속으로 작성한다.
- 작성
  > ***

---

---

(2) TIL (Today I Learned)

- TIL 은 오늘 내가 배운 것을 기록하는 것
- 현재까지 배운 것을 마크 다운 문법을 활용하여 정리
- 홈 디렉토리에 TIL 이라는 폴더를 만들고 그 안에 파일 생성

# 깃 이란 ?

> git 을 이용한 분산 버전 관리 프로그램

- 버전 : 컴퓨터 소프트웨어 특정 상태
- 관리 : 어떤 일의 사무 , 시설이나 물건의 유지 개량
- 프로그램 : 컴퓨터에서 실행될 때 특정 작업을 수행하는 일련의 프로그램

- 버전 관리 : 컴퓨터 소프트웨어의 특정 상태들을 관리 하는 것

# 깃허브란 ?

- 깃허브는 개발자들이 인스타그램을 제출하는 것처럼 이렇게 작업을 하고 코딩을 하고 이런 이력들을 가지고 있음을 나타낼수있는 하나의 공간

# 중앙집중식 vs 분산 버전 관리

- 중앙집중식 버전은 : 중앙서버에 버전에대한 데이터가 있고 중앙서버에서 파일을 받음

- 분산버전 관리 : 모든 버전들이 버전에 대한 데이터들이 모든 컴퓨터에 있다.
  사용자는 모든버전에 데이터를 가지고 있고 서버도 마찬가지이다.

# Git 초기 설정

> 최초 한번만 설정한다. 매번 Git을 사용할 때마다 설정 할 필요가 없다.

1. 누가 커밋 기록을 했는지 확인 할 수 있도록 이름과 이메일 작성

```
$ git config --global user.name "이름"
$ git config --global user.email "메일주소"

2. git 기본 명령어

- Working Directory : 사용자의 일반적인 작업이 일어남
- Staging Area : 커밋을 위한 파일 및 폴더가 추가되는 곳
- Repository : Staging Area 에 있던 파일 및 폴더의 변경사항(커밋)을 저장하는 곳

(1) git init
> $ git init

- 현재 작업중인 디렉토리를 Git으로 관리한다는 명령어
- .git 이라는 숨김 폴더를 생성하고 터미널에서 (master)라고 표기
- 절대로 홈 디렉토리에서 git init 하지않는다

(2) git status

> $ git status

- Working Directory 와 Staging Area 에 있는 파일의 현재 상태를 알려주는 명령어
- 어떤 작업을 시행하기 전에 수시로 status 를 확인하면 좋다
- 상태

1.Untracked : Git이 관리하지 않는 파일
2.Tracked : Git이 관리하는 파일
3.Unmodified : 최신 상태
4.modified : 수정되었지만 아직 Staging Area 에는 반영되지 않은 상태
5.Staged : Staging Area 에 올라간 상태


(3) git add

>$ git add a.txt 특정 파일
$ git add my_folder/ 특정 폴더
$ git add . 현재 디렉토리에 속한 파일/폴더 전부

- working Directory 를 Staging Area 에 올리는 명령어
- Git이 해당 파일을 추적(관리)할 수 있도록 만든다.
- Untracked , Modified -> Staged 로 상태를 변경한다.

- 예시
```

$ touch a.txt b.txt
$ git status

No commits yet
Untrached files: # 트래킹 되고 있지 않는 파일 목록

a.txt
b.txt

```

```

> a.txt 만 staging Area 에 올립니다.
> $ git add a.txt

-> a.txt 는 Changed to be committed 로 올라간다.

4.  git commit
    > git commit -m "first commit"

- Staging Area 에 올라온 파일의 변경 사항을 하나의 버전(커밋)으로 저장하는 명령어
- 커밋 메세지는 현재 변경 사항들을 잘 나타낼 수 있도록 의미 있게 작성하는 것을 권장
- 각각의 커밋은 SHA-1 알고리즘에 의해 반환 된 고유의 해시 값을 ID로 가진다.
- (root-commit) 은 해당 커밋이 최초의 커밋 일 때만 표시됨
  이후 커밋부터는 사라진다.

5.  git log

    > git log
    > $ git log
    > commit 1870222981b4731d14ef91d401c68c0bbb2f6e7d (HEAD -> master)
    > Author: kyle <kyle123@hphk.kr>
    > Date: Thu Dec 9 15:26:46 2021 +0900

        first commit

- 커밋의 내역(ID,작성자,시간,메세지 등)을 조회 할 수 있는 명령어
- 옵션

  - --oneline : 한 줄로 축약 해서 보여준다.
  - --graph : 브렌치와 머지 내력을 그래프로 보여준다.
  - --all : 현재 브렌치를 포함한 모든 브렌치의 내역을 보여준다
  - --reverse : 커밋 내역의 순서를 반대로 보여준다.
  - -p : 파일의 변경 내용도 같이 보여준다
  - -2 : 원하는 갯수만큼 내역을 보여준다.

  옵션 과 인자

  > 옵션은 생략 가능 부가적인 기능을 원할때
  > 예로 git log --oneline 로 커밋한 내역을 한줄로 보고싶을때

  > 인자는 명령어의 동작 대상을 지정한다. 생략이 불가능
  > git add 라고 작성하면 어떤 파일을 Staging Area 에 올릴지 모른다
  > 그래서 git ad a.txt 와 같이 동작할 대상을 지정해야하는데 이때 a.txt를 인자라고 한다.

6. 한눈에 보는 git 명령어

![](https://velog.velcdn.com/images/programmerpark94/post/cd0174f4-1e1f-45f6-9ae3-04b4e8b6c70a/image.png)

[1] 원격 저장소(Remote Repository)

> 여기 까지는 내 컴퓨터 한정된 공간 로컬 저장소 에서만 버전 관리를 했었다 이제 Github 라는 원격 저장소를 이용해서 내 로컬 저장소를 다른 사람들과 공유 해본다
> git의 주요 목적 중 하나 협업을 통해 로컬 저장소와 원격 저장소의 연동 방법을 익힌다

(2) 로컬 저장소 와 원격 저장소 연결

1. 원격 저장소가 잘 생성되었는지 확인 후, 저장소의 주소를 복사

2. 기존에 실습 때 만들었던 홈 디렉토리의 TIL폴더로 가서 vscode를 연다

3. git init 를 통해 TIL 폴더를 로컬 저장소로 만들어 준다

> $ git init
> Initialized empty Git repository in C:/Users/kyle/TIL/.git/

4. git remote

로컬 저장소에 원격 저장소를 등록, 조회 , 삭제 할 수 있는 명령어

1. 등록
   git remote add <이름> <주소> 형식으로 작성

   > $ git remote add origin https://github ~ TIL.git

   [해설]
   git 명령어를 작성할 건데 , remote(원격저장소)에 add(추가)
   origin 이름으로 https~.TIL.git 라는 주소의 원격 저장소연결

2. 조회
   git remote -v 로 작성

   > $ git remote -v
   > origin https://github.com/edukyle/TIL.git (fetch)
   > origin https://github.com/edukyle/TIL.git (push)
   > add를 이용해 추가했던 원격 저장소의 이름과 주소가 출력

3. 삭제

git remote rm <이름> 혹은 git remote remove<이름>으로 작성

> 로컬과 원격 저장소의 연결을 끊는 것이지 원격저장소 자체를 삭제하는게 아니다.

> $ git remote rm origin
> $ git remote remove origin

(3) 원격 저장소에 업로드

- 실습 때 작성했던 TIL 파일을 Github 원격저장소에 업로드
- 정확히 말하면 파일을 업로드 하는게 아니라 커밋을 업로드 하는것
- 로컬 저장소에서 커밋을 생성해야 원격 저장소에 업로드할수있다

1. 로컬 저장소에서 커밋 생성

```
# 현재 상태 확인

$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        day1.md

nothing added to commit but untracked files present (use "git add" to track)

$ git add day1.md

$ git commit -m "Upload TIL Day1"
[master (root-commit) f3d6d42] Upload TIL Day1
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 day1.md


 # 커밋 확인

$ git log --oneline
f3d6d42 (HEAD -> master) Upload TIL Day1


```

2. git push

- 로컬 저장소의 커밋을 원격 저장소에 업로드하는 명령어
- git push <저장소 이름><브랜치 이름> 형식으로 작성
- -u 옵션을 사용하면 두 번째 커밋부터 저장소이름,브랜치 이름으로 생략 가능

```
$ git push origin master

[풀이]
git 명령어를 사용할건데, origin이라는 이름의 원격 저장소의 master 브랜치에 push 한다.

------------------------------------------------

$ git push -u origin master
이후에는 $ git push 라고만 작성해도 push가 됩니다.
```

3. vscode 자격증명

![](https://velog.velcdn.com/images/programmerpark94/post/d145586f-2dac-47ab-b8b4-308edfec961b/image.png)

![](https://velog.velcdn.com/images/programmerpark94/post/332d232b-bfdf-4bed-85be-ab4ae85edbb8/image.png)

![](https://velog.velcdn.com/images/programmerpark94/post/80299b34-e62b-4b6a-a57e-a4ea7e5e7bce/image.png)

- 자격 증명 완료

이후 git push 완료

```
$ git push -u origin master
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/edukyle/TIL.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

4. 원격 저장소에서 정상적으로 업로드 되었는지 확인한다.

5. git push 를 그림으로 이해

![](https://velog.velcdn.com/images/programmerpark94/post/1cd4964f-a7ee-4537-8c7b-4c1401e9f9bd/image.png)

- 로컬 저장소의 commit 이력이 원격 저장소에 그대로 반영됩니다.
