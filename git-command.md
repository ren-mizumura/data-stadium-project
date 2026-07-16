# git command

## 作業ブランチの作成方法

### mainブランチに移動（基本ここでは作業しちゃダメ）
git checkout main

### 最新の状態に更新
git pull origin main

### 新しいブランチを作成して移動（自分の作業するブランチ）
git checkout -b feature/機能名  
git checkout -b fix/修正内容


## ローカルでの開発作業

### 変更されたファイルの確認
git status

### 変更をステージングエリアに追加
git add ファイル名
### またはすべての変更を追加
git add .

### コミットする（変更内容の説明付き）
git commit -m "コメント"



## 変更をGitHubにプッシュする

### ブランチをプッシュ（ブランチを作っていたらこっちで大丈夫）
git push origin ブランチ名

### リモートブランチを作成してプッシュ（初めてプッシュする場合）
git push -u origin ブランチ名


## プルリクエストの作成手順
1, GitHubのリポジトリページにアクセス  
2, 「Pull requests」タブをクリック  
3, 「New pull request」ボタンをクリック  
4, ベースブランチ（通常はmain）と、作成したブランチを選択  
5, 「Create pull request」をクリック  
6, タイトルと説明を入力して「Create pull request」をクリック  
<!-- プルリクエストの書き方 -->
<!-- 
どんな変更をしたのか
なぜその変更が必要だったのか
どうテストしたのか
 -->
