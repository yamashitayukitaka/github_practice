✅git pullとはfetch + merge
pull --rebase = fetch + rebase + ファストフォワードmerge

※git pull --rebase は「ローカルの作業ブランチ（たとえば main）」を、リモート追跡ブランチ（origin/main）の最新状態に合わせて rebase（移動する）する。

★1
git pull --rebaseの流れ

A --- B --- C (origin/main)
       \
        D --- E (main)


A --- B --- C (origin/main)
       
        　　　D´ --- E´(main)
<!-- 途中経過 -->


A --- B --- C --- D' --- E' (main)
<!-- pull --rebase完了 -->


★2、
--------------------------------------------
✅pull rebaseが終わったらremoteにpush
pull rebase後の状態
A --- B --- C --- D' --- E' (main)
A --- B --- C (origin/main)
--------------------------------------------
※git pull origin(リモートリポジトリ名) main（リモートリポジトリのブランチ名）を実行
git pull origin main実行後の状態

A --- B --- C --- D' --- E' (main)
A --- B --- C --- D' --- E' (origin/main)（リモートリポジトリの状態が反映される）


----------------------------------------
※単にgit pullとコマンドを打つとrebaseされないので
3-way-mergeになり見ずらくなるので
git pull --rebaseの仕様が推奨される

