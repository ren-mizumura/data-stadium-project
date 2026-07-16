# git command

## 作業の流れ
1,プロジェクトのソースコードをクローンする  
```bash
git clone
```

2,ブランチを分ける  
```bash
git switch -c feature/xxx
```
3,コードを編集する  
4,編集をコミットするファイルを選ぶ（.だと全部のファイルを指定） 
```bash
git add . 
```
5,ローカルで変更をコミットする  
```bash
git commit -m "コミットメッセージ" 
```
6,ローカルの変更をリモートに反映する  
```bash
git push origin feature/xxx
```
7,GitHub上でプルリクエスト（自分の変更をメインブランチに反映したいよと要求する）  
8,（チームメンバーに レビュー & マージ してもらう）  
9,git switch main でメインブランチに戻り、git pull で最新のメインブランチの情報を取得する  
ここまでが一連の流れで、この後再び2に戻ります。

## 作業ブランチの作成方法

### mainブランチに移動（基本ここでは作業しちゃダメ）
```bash
git checkout main
```

### 最新の状態に更新
```bash
git pull origin main
```

### 新しいブランチを作成して移動（自分の作業するブランチ）
```bash
git checkout -b feature/機能名  
git checkout -b fix/修正内容
```


## ローカルでの開発作業

### 変更されたファイルの確認
```bash
git status
```

### 変更をステージングエリアに追加
```bash
git add ファイル名
```
### またはすべての変更を追加
```bash
git add .
```

### コミットする（変更内容の説明付き）
```bash
git commit -m "コメント"
```



## 変更をGitHubにプッシュする

### ブランチをプッシュ（ブランチを作っていたらこっちで大丈夫）
```bash
git push origin ブランチ名
```

### リモートブランチを作成してプッシュ（初めてプッシュする場合）
```bash
git push -u origin ブランチ名
```


## プルリクエストの作成手順
1, GitHubのリポジトリページにアクセス  
2, 「Pull requests」タブをクリック  
3, 「New pull request」ボタンをクリック  
4, ベースブランチ（通常はmain）と、作成したブランチを選択  
5, 「Create pull request」をクリック  
6, タイトルと説明を入力して「Create pull request」をクリック  

### プルリクエストの書き方
 - どんな変更をしたのか
 - なぜその変更が必要だったのか
 - どうテストしたのか  


## おまけ（たまに使うコマンド集）

### commit などの履歴を確認できるコマンド
```bash
git log
```

### 現在ステージングしているファイルやコミットしているファイルなどの状態を確認できるコマンド
```bash
git status
```

### 現在のブランチや、ローカルに存在するブランチの一覧を表示するコマンド
```bash
git branch
```

### 現在の作業状態を一時的に保存し、1つ前のコミットの状態（厳密ではないかも）に戻すコマンド
```bash
git stash
```

### stash しておいた状態を適用するコマンド
```bash
git stash apply
```
