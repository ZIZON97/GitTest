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
```Shell
git revert 커밋아이디
```

## reset
시간을 되돌릴 때 사용.
```Shell
```