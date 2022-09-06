# 【Django】個人用Todoリスト
デモサイトは<a href="http://4ndk5.pythonanywhere.com/" target="_blank">こちら</a>です。

## ローカルでTODOリストを動かす
作成時のバージョン
|ソフトウェア|バージョン|
---- | ----
| python | 3.10.5 |
| Git | 2.37.2 |
| SQLite | 3.37.2 | 

実行時の環境  
Windows10  
PowerShell  

1. プロジェクトをコピーするためのフォルダをひとつ作成してください。コマンドプロンプト（あるいはシェル）のカレントディレクトリをそのフォルダ内にするように設定します。  
```
: cd フォルダまでのアドレス
```
  
2. GitHubのURLからローカルにプロジェクトをコピーするために、以下のコマンドをコマンドプロンプトから実行してください。以下、コマンドの実行(:)はWindowsであればPowerShell、Macであればシェルから実行するコマンドを意味します。  
```
: git clone https://github.com/kametee/djangotodo.git
```

3. 作成されたdjango-todoディレクトリ内に移動してください。  
```
: cd django_todo
```

4. 仮想環境を作ります。  
（ここではvenvという名前で環境を作ります）  
```
: python -m venv venv
```  
  
5. 作成した仮想環境を有効にします。  
仮想環境の必要性や、各OS毎の仮想環境を有効にする方法について説明している、<a href="https://camp.trainocate.co.jp/magazine/venv-python/" target="_blank">こちら</a>のサイトをご参照ください。  

6. Djangoを動作させるのに、必要なモジュールをインストールします。  
```
: pip install -r requirements.txt
```
  
7. データベースにTodoモデルを作成します。  
```
: python manage.py makemigrations todo
```
  
8. データベースのマイグレーションを行います。  
```
: python manage.py migrate
```

9. データベースにアクセスできるユーザーを設定します。
```
: python manage.py createsuperuser  
```
ユーザー名、メールアドレス、パスワードを設定してください。  
ここで作成したユーザーでログインすることができます。    
10. サーバーを開始します。  
```
: python manage.py runserver
```  
11. 早速、以下のＵＲＬからコンテンツにアクセスしてみましょう。  
  **http://127.0.0.1:8000/**
