# merge

## merge 명령어
merge 받을 main (기준 브랜치) 과 merge 될 COFFEE 브랜치(신규 브랜치)가 있음
```Shell
git switch main
git merge COFFEE
```

## 하지만 같은 파일을 변경하였을 경우에는?
각각의 브랜치에서 같은 파일을 수정하면 coflict 발생했다고 하면서 conflict 발생한 파일을 알려준다.  
conflict 발생한 파일을 확인해보면 conflict 발생한 부분에 대해서 브랜치별로 다른 점을 정리하여 파일이 수정되어 있다. 그래서 다시 add 하고 commit 해야 한다.

## merge 방법들
+ 3-way
   - 기준 브랜치와 신규 브랜치 둘다 commit 이 있는 경우
+ fast-forward
	- 기준 브랜치에는 신규 commit 이 없어서 신규 브랜치를 기준 브랜치로 지정하는 경우
	- 기준 브랜치에 신규 commit 없으면 자동으로 fast-forward
+ rebase
	- 신규 브랜치의 commit 들을 기존 브랜치의 제일 마지막 commit 뒤로 붙여서 fast-forward 로 merge 하는 방식
	- rebase 를 이용하게 되면 신규 브랜치에 있던 commit들 전부 그대로 따라온다.
	- ```Shell
		git switch 신규 브랜치명
		git rebase 기준 브랜치명
		git switch 기준 브랜치명
		git merge 신규 브랜치명
		```
+ squash
	- squash 의 경우 rebase 와 다르게 신규 브랜치에 있던 커밋을 한꺼번에 뭉쳐서 하나의 commit 으로 보이게 된다.
	- squash 를 할 경우 log 를 확인해보면 브랜치가 끊긴 것처럼 보임. 보기 싫으면 지우자.
	- ```Shell
		git merge --squash 신규 브랜치명
		```
