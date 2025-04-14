## <p style="text-align:center;">개발 입문 스터디 Quiz 1</p>

#### Example
개발 입문 스터디는 무슨 요일인지 적으시오.

- 답: 금요일

### Q1
Git에서 파일의 상태는 크게 untracked와 tracked로 나눌 수 있다.  
그렇다면 tracked에는 어떤 상태가 있는지 모두 적으시오.

- 답: unmodified Modified Staged


### Q2
Git에는 세 가지 영역이 있다.  
세 가지 영역을 모두 나열하시오.

- 답: working directory, staging area, repository

### Q3
현재 우리는 ```main```브랜치에 있다.  
```develop```이라는 브랜치를 새로 만들고 이동까지 한번에 할 수 있는 명령어를 적으시오.

- 답:  git checkout -b develop

### Q4
Working Directory에 있는 파일들을 모두 Staging Area에 추가할 수 있는 명령어를 적으시오.

- 답: git add .

### Q5
```
1. Create a merge commit
2. Squash and merge
3. Rebase and merge
```
위의 세 가지가 어떤 차이가 있는지 간단히 적으시오.

- 답: 
- create: 기존 커밋 유지하고 브랜치 출처까지 기록하면서 머지함. 변경내역 추적이 용이하다. 
- squash: 수정사항의 커밋을 하나로 통일 후 수정사항을 머지함. 깔끔하다.
- Rebase: 중앙 브랜치의 내용으로 먼저 업데이트 한 후 머지함. 

### Q6
```git log --oneline```으로 commit의 기록을 확인해보니  
첫 줄에 ```a1s2d3f (HEAD -> develop) docs: readme 추가```라는 log가 찍혔다.
알 수 있는 사실을 모두 적으시오.

- 답: 파일이 develop 브랜치로 'docs: readme 추가'라는 메세지와 함께 커밋되었다.

### Q7
```git log --oneline```으로 commit의 기록을 확인해보니 아래와 같은 log를 확인 할 수 있었다.  
```
a1s2d3f (HEAD -> develop) fifth commit
s2d3f4g fourth commit
345hj26 third commit
7g8dg7f second commit
5g568vk first commit
```
이때, fourth commit까지 제거하고 fourth commit과 fifth commit의 변경 사항은
Staging Area에 남아 있길 바란다면 reset을 어떤 옵션과 함께 사용하면 되는지 적으시오.

- 답: --soft

### Q8
```git log --oneline```으로 commit의 기록을 확인해보니 아래와 같은 log를 확인 할 수 있었다.
```
a1s2d3f (HEAD -> develop) fifth commit
s2d3f4g fourth commit
345hj26 third commit
7g8dg7f second commit
5g568vk first commit
```
reset은 너무 위험하니 revert를 사용하려고 하여 ```fifth commit```을 되돌리고 싶다면 
어떤 명령어를 사용하면 되는지 적으시오. 

- 답: git revert s2d3f4g

### Q9
여러 사람이 협업하는 프로젝트에서 커밋을 되돌려야 한다.  
reset과 revert 중에 어떤 것을 선택할 것인지를 그 이유와 함께 적으시오.

- 답: revert.
    reset을 이용하면 기존 커밋이 삭제된다. 만약 협업자가 삭제전 커밋을 알고있었다면 커밋삭제인지 버그인지 의문을 품고 나를 귀찮게 할 것이다. 
    또, 프로젝트가 커졌을 때 같이쓰는 파일을 스리슬쩍 reset해버리면 그 파일을 기반으로 작업하던 협업자는 영문도 모른채 프로그램이 굴러가지 않는 참사를 겪을 것이다.

    commit은 변경사항을 알리기 위해 만들어졌다.
    파일을, commit을 삭제하는 변경조치를 취할 때도 알려주는 것이 인지상정.
    따라서 협업자에게 변경내역을 알릴 수 있는 revert를 이용한다.

