✅git clone URLを実行すると
ローカルに以下二つブランチが出来る

★1,mainブランチ(リモートリポジトリをコピーしたローカルでの作業用ブランチ)
※HEADはmainブランチの最新コミットを指す

★2,origin/mainブランチ(追跡・確認用)
※origin/HEADはorigin/mainブランチの最新コミットを指す。

=====================================
git fetchした場合は、
1.origin/mainブランチにリモートリポジトリの最新コミットが取得される
2.git merge origin/mainでmainブランチと統合する