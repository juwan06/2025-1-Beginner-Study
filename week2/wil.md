# branch
* 분기를 나눠서 파일 관리하는 방법
## 명령어
* git branch -a (존재하는 모든 브런치 확인)
* git checkout [branch name] (해당하는 브랜치로 이동,대괄호는 무시)
* git branch -D [branch name] (해당 브랜치 삭제, 단, 현재위치한 브랜치는 불가)
# pull request
* 브랜치 병합요구
## 병합방식(merge)
* squash merge (브랜치 내 개별 커밋 메세지 삭제. 큰 커밋메세지 하나만 전달 하면서 병합)
    * 명령어: git merge --squash [브랜치 이름]

* Create a merge commit (커밋메세지 저장. 브랜치 출처까지 남김 )
    * 명령어: git merge [브랜치 이름]

* Rebase and merge (중앙 브랜치 내역 가져온 후 그위에 쌓아서 머지)
    * 명령어: git merge [브랜치 이름]
