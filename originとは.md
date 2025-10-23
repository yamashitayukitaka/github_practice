git clone https://github.com/user/repo.git
このコマンドを実行すると：

クローンされたローカルリポジトリが作成される
クローン元（https://github.com/user/repo.git）が「`origin`」という名前で登録される

※gitHubではデフォルトでmasterブランチと言う名前は使えないので、mainブランチと言う名前が採用される


----------------------------------------------------------------
✅ローカルではクローンした時点で
HEAD → main からコミットが始まる

※origin/main と origin/HEAD はクローン時点のリモートの状態を示す
その後リモートで変更があっても、ローカルの origin/main と origin/HEAD は自動では変化しない
----------------------------------------------------------------

✅git branch -rは現在ローカルにあるorigin/main と origin/HEAD を表示する
※ローカルに最後に fetch や clone したときの状態を表示している。

✅git remote は「現在接続されているリモートリポジトリの存在やURL情報」を確認するコマンド
※git clone URLでは指定された URL のリポジトリをコピーして ローカルリポジトリ を作成します。
同時に、クローン先のローカルリポジトリに リモート接続情報 が自動で設定されます。

✅git remote -v
※詳細情報（URLやフェッチ・プッシュ設定など）を確認
origin  https://github.com/example/repo.git (fetch)
origin  https://github.com/example/repo.git (push)