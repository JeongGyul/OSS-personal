# Git 명령어 정리
## 1. 커밋
### add
* add는 Working Directory에 있는 파일을 Staging Area에 추가해줍니다.
```git
$ git add 파일이름
```

***
### commit
* commit은 Staging Area에 있는 파일을 .git directory로 기록합니다. 이때, 스냅샷이라는 방식을 이용합니다.
```git
$ git commit
```

***
### log
* log는 커밋한 후 커밋 기록을 확인할 수 있는 명령어입니다.
```git
$ git log
```

***
### show
* show는 모든 커밋 기록을 나타내는 log와 달리 최신 커밋 기록만을 나타냅니다.
```git
$ git show
```
