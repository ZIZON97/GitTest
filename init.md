# init

## 프로젝트 git으로 관리 시작하기
```Shell
git init
git branch -M main
```

## 원격저장소에 로컬 프로젝트 저장
```Shell
git push 원격저장소주소 main(로컬브랜치명)
```

## 주소 맨날치기 귀찮지 ?
변수로 지정 가능.
```Shell
git remote add var 원격저장소주소
git push origin main
```
혹시 변수 기억 안나면
```Shell
git remote -v
```

## 이것도 귀찮지 ?
-u 옵션이면 주소를 기억. 처음한번 push 할 때 -u 하면 됨.
```Shell
git push -u 원격저장소주소 main
git push
```