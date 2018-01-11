# 3rdDevCampInfo
第3回開発合宿共有情報

## Lambda(MicroService)の追加
1. リポジトリの作成  
githubにログインし、画面上部からリポジトリの作成(New Repository)を選択する  
<img src="https://user-images.githubusercontent.com/34710839/34205880-82d3e820-e5c7-11e7-8bcc-d6e17efbd26e.png" width=800px />  
1. Lambdaの作成
	1. AWS Cloud9の右ペインから「AWS Resources」を選択し、「λ+」アイコンよりLambdaを追加する  <img src="https://user-images.githubusercontent.com/34710839/34237897-69f5ef12-e642-11e7-95ad-a2a702166e9e.png" width=250px />  
	1. FunctionNameとAppNameを入力する(というよりも、FunctionNameをいれるとAppNameに同じものが入る) 
	1. 使う言語に応じて好きなRuntimeを選択する(だいたいnodeかpythonになるはず)  <img src="https://user-images.githubusercontent.com/34710839/34238209-e0cf4f38-e643-11e7-89d1-2021fce9789a.png" width=400px />  
	1. FunctionTrigger(Lambdaを実行するトリガー)を選択する(noneでよい)  
	1. メモリは128(MB)(足りなければ後で変更します)、Roleを「choose an existing role」にし、「ilab-bot-functions」を選択
	1. Finish
1. 作成されたディレクトリをgit管理下に置く
	1. 「＋」アイコンから「New Terminal」を選択し、Newセッションを開く(一番左のコンソールは共有されているため)  <img src="https://user-images.githubusercontent.com/34710839/34239377-539a7c94-e64a-11e7-9904-86d69a5b0932.png" width=250px />
	1. 開いたターミナルコンソール上で`cd [LambdaFunction名]`でカレントディレクトリを作成したlambdaのディレクトリにうつる
	1. `git init`コマンドをうち、リポジトリ化する
	1. `git remote add origin git@github.com:githubのユーザ名/リポジトリ名.git`　コマンドをうち、リポジトリ情報の追加
	1. `git fetch`コマンドの後、`git pull origin master`コマンドでgithubリポジトリのファイルをひきとる
	1. 開発が終わったタイミング・きりのいいタイミングで、`git add .`コマンド、`git commit -m "コミットメッセージ"`コマンド、`git push origin master`で自動作成されたファイルをgithubのリポジトリに送る
