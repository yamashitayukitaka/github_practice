✅git fetch originで
リモートの最新状態のコミットをローカルのリモート追跡ブランチのに取得する。
この段階では、ローカルのmainブランチとリモート追跡ブランチの更新は統合されていない。
※git fetchは後でmergeする必要がある

-------------------------------------------
✅git fetch 後
ローカルのmainブランチ
HEAD → main
main: A

ローカルのリモート追跡ブランチ
origin/main:   A --- B --- C   
origin/HEAD → origin/main
-------------------------------------------

✅git merge origin/main後
ローカルのmainブランチ
HEAD → main
main → A --- B --- C

ローカルのリモート追跡ブランチ
origin/main → A --- B --- C
origin/HEAD → origin/main
