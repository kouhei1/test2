# Gitの使い方メモ  
## Gitの保存場所  
1. **「ワーキングツリー」**  
	作業中のファイルの保存場所  
	<br>   ↓add<br><br>
1. **「インデックス」**  
	コミットするファイルを登録する場所  
	コミットするファイル数を決めることができる  
	<br>   ↓commit<br><br>
1. **「ローカルリポジトリ」**  
	リモートリポジトリに送るためのコミットを記録する場所  
	<br>   ↓push<br><br>
1. **「リモートリポジトリ」**  
	複数人で共有するための場所  

 
## Gitのコマンド  
### ローカルリポジトリを作成する  
```  
git init   
#カレントディレクトリにローカルリポジトリ作成 初期ブランチの名前はmain(旧 master)
```

### リモートリポジトリ追加  
	リモートリポジトリのurlに名前を付ける  
	fetch pull pushなどで使うことができる  
```  
git remote #一覧  
git remote get-url <--all:Fetch and Push/--push:Push/None:Fetch> <name> #url取得 
git remote add <name:origin> <url>
git remote rename <old> <new>
```  
### ブランチ関連  
```  
git branch -a #ブランチ一覧  
git branch <name> #ブランチを作成  
git checkout <name> #ブランチ切り替え  
```  

### ファイルをインデックスに登録する  
```  
git add <file name> <file name> ... #インデックスへファイルを追加  
git add -A          #全てのファイルの変更を追加  
```  
  
### ブランチの差分を確認する 前回addされてからの差分  
```  
git diff  
```  
  
### コミットを確認する  
```  
git show <hash>  
git show HEAD   #今いるブランチの最新のcommit  
git show HEAD^  #最新のcommitの１つ前  
git show HEAD^^ #最新のcommitの２つ前  
git show HEAD~2 #最新のcommitの２つ前  
```  