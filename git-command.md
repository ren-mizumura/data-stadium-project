# git command

## 作業の流れ
1,git clone プロジェクトのソースコードをクローンする  
2,git switch -c feature/xxx ブランチを分ける  
3,コードを編集する  
4,git add . 編集をコミットするファイルを選ぶ（.だと全部のファイルを指定）  
5,git commit -m "コミットメッセージ" ローカルで変更をコミットする  
6,git push origin feature/xxx ローカルの変更をリモートに反映する  
7,GitHub上でプルリクエスト（自分の変更をメインブランチに反映したいよと要求する）  
8,（チームメンバーに レビュー & マージ してもらう）  
9,git switch main でメインブランチに戻り、git pull で最新のメインブランチの情報を取得する  
ここまでが一連の流れで、この後再び2に戻ります。

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
