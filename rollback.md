# restore , revert , reset

## restore
파일을 되돌릴 때 사용. 기본은 최근 커밋 상태로.  
이전의 커밋 상태로 돌리고 싶을 때는 아래의 명령어로.
```Shell
git restore 파일명
git restore --source 커밋아이디 파일명
```

## revert
커밋을 되돌릴 때 사용. 새로운 커밋을 만들어서 취소.  
커밋 여러개도 가능. HEAD 도 가능.
```Shell
git revert 커밋아이디1 커밋아이디2
```

## reset
시간을 되돌릴 때 사용. 몇가지 옵션들이 있음.
- hard : 다 지워버리고 날리기
- soft : Staging Area 에 변동사항 저장
- mixed : Unstaging Area 에 변동사항 저장
```Shell
git reset --hard 커밋아이디
git reset --soft 커밋아이디
git reset --mixed 커밋아이디
```