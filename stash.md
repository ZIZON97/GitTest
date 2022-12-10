# stash

## stash 
staging 된 것을 저장시키는 다른 곳에 임시저장.  
staging 안된 것도 가능. stash 에 이름도 지정 가능.  
여러개 가능. 아래 명령어로 stash 에 저장된 리스트 확인.
```Shell
git stash
git stash save "메모"
git stash list
```

## stash list 에서 제거
stash{0}에 있는 번호 입력하여 하나씩 제거 가능.  
전체 제거 가능
```Shell
git stash drop 번호
git stash clear
```