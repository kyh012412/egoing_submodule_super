super내의 lib과 module은 각각의 원본 git의 어떤 commit과 연결될지를 나타내준다.

sub1 (원본저장소) 를 수정 후 push
super로 돌아와서 cd lib / git pull
다시 cd .. (super와서)
git diff

여러개의 submodule들을 하나하나 pull하기 어려우므로
super쪽에서
`git submodule update --remote`  
각각의 서브모듈을 원본의 최신으로 가져와라 라는 뜻

만약에 --remote가 없다면 `git submodule update`  
super의 .git 기준
마지막으로 커밋한 버전으로 바뀌게됨

`git submodule summary` 라는 옵션이 있음

`git submodule` 라는 명령어도있음
