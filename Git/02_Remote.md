# 원격저장소 활용

> 원격 저장소(remote repository)를 제공하는 서비스는 github, gitlab, bitbucket등이 있다.



## 1. 원격 저장소 설정하기

```bash
$ git remote add origin ____
```

* 깃아, 원격저장소를 추가해줘 (add) origin이라는 이름으로 URL을!!

* 원격저장소 설정을 삭제하는 명령어는 다음과 같다.

  ```bash
  $ git remote rm origin
  ```



## 2. 원격 저장소 확인하기

```bash
$ git remote -v
origin  https://github.com/LeeDongu/project-test.git (fetch)
origin  https://github.com/LeeDongu/project-test.git (push)
```



## 3. `push`

```bash
$ git push origin master
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (7/7), 577 bytes | 288.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/LeeDongu/project-test.git
 * [new branch]      master -> master

```

* `origin` 저장소의 `master `브랜치로 `push`

  

## 4. Pull

* 원격 저장소의 변경 사항을 받아옴

  ```bash
  $ git pull origin master
  ```



## 5. Clone

* 원격 저장소를 복제함

  ```bash
  $ git clone ___ (URL)
  ```

  