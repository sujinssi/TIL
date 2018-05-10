##github 실습

github에서 repo 하나를 파주자
초기 세팅을 미리 할 수 있다. 
- 'add .gitignore'로 숨김파일만들 수 있다.
- 'add a license' 라이센스를 추가할 수도 있음
- readme.md 미리 만들 수 있다 / 우리는 만들지 않고 시작하는 방법으로 할 것.

```
$ git init
```
git init을 하는 순간부터 git과 연결되는 것. 프로젝트를 시작할 때 처음부터 git init하고 시작하면 ㅈ호음
git init으로 유저의 최상단 폴더에서 깃을 설치하면 안된다. 그러면 내 컴퓨터를 공유하는 것. 
ls -al로 .git이 있냐 없냐를 통해 깃과 연결되어 있는지 확인할 수 있다.

파일을 추가하거나 수정한 뒤에

```
$ git status // 상태 확인
$ git add filename
# git status
$ git commit //vim으로 들어와 메세지 입력. (i로 들어와서 쓰고 esc로 나가기하고 :wp로 저장해서 vim나가기)
```
받는 사람이 누군지 알기 위해 리모트저장소를 알려주자
받는 사람 주소에 대한 별명 같은 것이 origin. 다른 별명을 해도 상관 없는데 한번 하면 계속 그 별명을 사용해야함.
받는 사람 주소는 프로젝트 할 때 한번만 하면 된다.
``` 
$ git remote origin https://github.com/sujinssi/deleted_soon.git
```
이제 우리 변경사항을 master차원으로 올려보자
```
$git push origin master 
```

빔으로 들어가서 직접 수정해보자
```
$ vi readme.md
```
이번에는 빔에서 말고 터미널에서 바로 메세지를 달아보자
```
$ git commit -m "Practicing git
```
이렇게 하면 개행이 열린다. 여기부터 내용을 적으면 됨.내용 다 적으면 
```
$ "
```
마지막으로 푸시하기
```
$ git push origin master
```
---
github에서 MIT license가 가장 자유로운 라이센스다. 만약 GNU open소스는 별로 오픈되어 있지 않아서
어떤 오픈소스가 저 라이센스라면 그 소스는 안쓰는게 좋다.


이미 깃이 연결되어있는 폴더와는 연결하면 안된다. 꼬이기 때문.

방금만든 깃 레포를 연결해서 와보자
깃헙 원격저장소 -> 로컬로 클론 해보자
```
$ git clone https://github.com/sujinssi/TIL.git
````
ls로 찍어보면 방금 만든 TIL가 받아져내려온 것을 알 수 있다. 
```
$ cd TIL
$ mkdir README.md
$ vi README.md // 내용을 수정한다
$ git add .
$ git status
$ git commit - "modified content"
$ git push origin master
```