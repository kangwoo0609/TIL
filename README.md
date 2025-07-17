# Github 입문

* 설정

1. Gitbash 다운받고 설치, 약간 기억 안 남
2. 중간에 뭐 계정 설정도 있었던 듯?
3. git init을 통해서 github에서 관리할 수 있도록 함
4. github에서 파일들을 받아줄 수 있는 repository 만들기

* add, commit, push

1. add<br>
git add로 설정 가능<br>
git hub에 올리고 싶은 파일을 staging area에 달아두는 것<br>

2. commit<br>
git commit으로 가능<br>
현재 staging area에 올라가 있는 파일들이 어떤 version(어떤 변화가 있었는지)인지 명시<br>
commit = 변경된 행동

4. push<br>
git push로 가능<br>
보내기 전에 어떤 repository로 보낼지 경로 설정이 필요<br>
staging area에 있는 파일을 github repository에 넘기기

* pull, clone

1. pull<br>
git repository에 있는 파일 중 변경 사항만 가져오기<br>
github에서 파일을 수정한 후, local repository(working directory)로 수정(변경) 사항 가져오기

2. clone<br>
아묻따 복사


* .gitignore<br>
add, commit, push 하기 싫은/하면 안되는 파일들을 여기에 등록하면 됨<br>
다만, git에 의해 관리가 되고 있으면 소용 없음. 캐시 지우고 다시 등록해야 됨

**잘 안 씀**
* revert<br>
단일 commit의 실행을 취소하는 것<br>
대신 commit 자체가 사라지는 건 아니고, commit으로 실행한 것이 취소되는 거임(commit의 기록은 남음)<br>
취소할 때는 파일이름이 아니라! commit 번호(ID)를 입력해야 됨

* reset<br>
특정 commit으로 되돌아가는 것(save & load의 개념)<br>
단, 그 commit 이후의 모든 commit은 삭제됨<br>
그래도 옵션을 통해서 그 기록을 남길지, 남길지 선택 가능<br>
soft는 commit을 push는 안 하고 add한 상태로 남기기<br>
mixed는 local에 파일은 남기고 add 전 상태로 두는 것(기본값)<br>
hard는 얘는 아예 진짜로 회귀하는 것. 이전 commit으로 바뀐 것들이 다 사라짐

* restore<br>
아직 add되지 않은 파일에 대해서 완전 복구해버리는 것<br>
staging 된 최종 commit의 version으로 복구하기 >> 취소 불가!<br>

* rm --cached<br>
commit 되기 이전에 add만 취소하는 것

* restore --staged<br>
얘도 수정 commit 달기 전에 add된 거 취소하는 것
