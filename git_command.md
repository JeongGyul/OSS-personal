# Git 명령어 정리
## 1. 커밋
### add
* add는 Working Directory에 있는 파일을 Staging Area에 추가해줍니다.
```git
$ git add [파일 이름]
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
## 2. 서버
### clone
* clone은 원격 저장소의 커밋된 코드를 복제하여 내려받습니다.
```git
$ git clone [원격 저장소 링크]
```

***
### push
* push는 로컬 저장소의 커밋된 파일들을 원격 저장소로 업로드하는 명령어입니다.
```git
$ git push [원격 저장소 별칭] [브랜치 이름]
```

***
### pull
* pull은 원격 저장소의 갱신된 내용만을 로컬 저장소로 내려받습니다.
```git
$ git pull
```

***
### fetch/merge
* fetch는 원격 저장소에서 코드를 수동으로 내려받습니다. 내려받은 후 현재 브랜치와 자동 병합하지 않습니다.
```git
$ git fetch [원격 저장소 링크]
```
* merge는 fetch로 내려받은 코드를 수동으로 병합합니다.
```git
$ git merge 원격저장소별칭/브랜치이름
```


## 3. 브랜치
### branch
* branch는 특정 커밋에서 새로운 개발 분기점을 생성합니다. 
```git
$ git branch [브랜치 이름] [커밋 ID]
```

***
### checkout
* checkout은 현재 브랜치를 떠나 새로운 브랜치로 이동합니다.
```git
$ git checkout [브랜치 이름]
```

***
### switch
* switch는 checkout과 동일한 기능을 합니다. 현재 브랜치를 떠나 새로운 브랜치로 이동할 수 있습니다.
```git
$ git switch [브랜치 이름]
```

## 4. 병합
### Fast-Forward merge
* Fast-Forward merge은 두 개의 브랜치가 일렬 상태에 있을 때 브랜치를 병합하는 방법입니다.
```git
$ git merge [브랜치 이름]
```

***
### 3-way merge
* 3-way merge는 두 개의 브랜치가 일렬 상태에 있지 않고 더 복잡할 때 브랜치를 병합하는 방법입니다.
* Fast-Forward merge와 달리 브랜치를 병합하면 새로운 커밋이 추가됩니다.
* 명령어는 Fast-Forward merge와 동일합니다.
```git
$ git merge [브랜치 이름]
```

***
### rebase
* rebase는 기존의 베이스 커밋을 브랜치의 최신 커밋으로 변경하는 명령어입니다.
* 앞에서 언급한 병합 방법과 달리 rebase는 커밋의 진행 모습이 단순하다는 장점이 있습니다.
```git
$ git rebase [브랜치 이름]
```

## 5. 복귀
### reset
* reset은 마지막에 기록한 커밋을 취소하고 이전 커밋의 상태로 되돌아가는 것입니다.
* reset의 옵션에는 Working Directory와 Staging Area를 유지한 채 되돌아가는 soft와  
  Working Directory만 유지하는 mixed, 둘 다 삭제하는 hard 옵션이 있습니다.
```git
$ git reset [옵션] [커밋 ID]
```

***
### revert
* revert는 reset과 달리 기존 커밋을 남겨 두고 취소에 대한 새로운 커밋을 생성합니다.
```git
$ git revert [커밋 ID]
```
