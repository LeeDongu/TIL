# 원격 저장소 Push 시 오류

```bash
$ git push origin master
To https://github.com/LeeDongu/Bigdata.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/LeeDongu/Bigdata.git'
# 거절됨 (Rejected)
# 원격 저장소의 작업(커밋)이 로컬에 없음
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
# 원격 저장소의 변경사항을 먼저 통합하고
# 예) git pull ...
hint: to the same ref. You may want to first integrate the remote changes
# 다시 push
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

* 원격 저장소와 로컬 저장소의 커밋 히스토리를 확인하고 아래의 명령어를 입력한다.

  ```bash
  $ git pull origin master
  remote: Enumerating objects: 5, done.
  remote: Counting objects: 100% (5/5), done.
  remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (3/3), 662 bytes | 73.00 KiB/s, done.
  From https://github.com/LeeDongu/Bigdata
   * branch            master     -> FETCH_HEAD
     e0f87a5..a404f8c  master     -> origin/master
  Merge made by the 'recursive' strategy.
   README.md | 1 +
   1 file changed, 1 insertion(+)
  
  ```

  * vim 편집기 창이 Pop-up 될 것.
    * `esc` + `:wq`  엔터
      * w : write (저장)
      * q : quit (나가기)



* log를 확인한다

  ```bash
  $ git log --oneline
  # vim 편집기가 뜬 이유 => 합쳐졌다라는 사실을 커밋으로 남김
  8894bd5 (HEAD -> master) Merge branch 'master' of https://github.com/LeeDongu/Bigdata
  # 로컬 작업한 것
  ed29cf7 Add test
  # 원격 저장소에서 작업 한 것
  a404f8c (origin/master) Update README.md
  e0f87a5 Create README
  ```

* 다시 Push 한다.

