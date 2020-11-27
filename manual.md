# 自分用　Gitの使い方メモ  
## Gitの保存場所について  
1. #### 「ワーキングツリー」
	作業中のファイルの保存場所  
	ローカル環境にある  
	<br>↓add<br>
1. #### 「インデックス」  
	コミットするファイルを登録する場所  
	コミットするファイル数を決めることができる  
	ローカル環境にある  
	<br>↓commit<br>
1. #### 「ローカルリポジトリ」  
	リモートリポジトリに送るためのコミットを記録する場所  
	ローカル環境にある  
	<br>↓push<br>
1. #### 「リモートリポジトリ」
	複数人で共有するための場所  
	リモート環境にある  


## よく使うGitコマンド
- #### ローカルリポジトリを作成する  
	```
	git init  
	#カレントディレクトリにローカルリポジトリ作成  
	#デフォルトでmain(旧:master)ブランチが作成される   
	```
- #### リモートリポジトリ   
	fetch pull pushなどで使うリモートリポジトリのurlを設定する。  
	```  
	git remote #一覧表示  
	git remote get-url <--all:Fetch and Push/--push:Push/None:Fetch> <name> #url取得
	git remote add <name:origin> <url> #リモートリポジトリのurlに名前を付ける
	git remote rename <old> <new>
	```
- #### ブランチ関連  
	並行して作業する際に使用する  
	例.　developブランチを作成　→　developで作業　→　mainにマージ  
	mainブランチでの作業は行わない  別のブランチで開発しマージする
	```  
	git branch -a #ブランチ一覧表示  
	git branch <name> #新規ブランチを作成  
	git checkout <name> #ブランチ切り替え
	git merge <name> #現在のブランチに<name>のブランチをマージする
	```  
- #### ファイルをインデックスに登録する  
	```  
	git add <file name> <file name> ... #インデックスへファイルを追加  
	git add -A          #全てのファイルの変更を追加  
	```  
- #### ブランチの差分を確認する   
	```  
	git diff  #前回addされてからの差分
	```  
- #### コミットを確認する  
	```  
	git show <hash>  
	git show HEAD   #今いるブランチの最新のcommit  
	git show HEAD^  #最新のcommitの１つ前  
	git show HEAD^^ #最新のcommitの２つ前  
	git show HEAD~2 #最新のcommitの２つ前  
	```  

## リポジトリ作成からpushまで
1. 編集中

## ブランチ作成からマージまで
1. 編集中
