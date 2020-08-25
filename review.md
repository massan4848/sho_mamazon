$
# 1  
pipenvの設定
`pipenv install` 仮想環境をつくる。
`pipenv shell`
`pipenv install django`
`pipenv install --dev autopep8 flake8`  



# 2 
startapp ->migrate,settingのInstalled Appに追加`アプリ名.apps.<アプリ名>Config`
setting.pyに`STATICFILES_DIRS = [os.path.join(BASE_DIR,'static')]`を追記  
（のちのち使う）templates/<app名>/<xx.html>、staticの作成、settingにstaticのパスを通す。  
templatesの複数形に注意  

課題：プロジェクト作成から、アプリを一つ立ちあげられるまでの流れ作業を確認する。

# 3 
fixture:データを指定したファイルから入力できる。  
adminから手動で入力するより楽  
データを準備する必要がある。 
json file に作成したら、`python manage.py loaddata xx.json`でデータをデータベースに追加
super user `python manage.py createsuperuser`
settings.py のSTATIC_URL とSTATICFILES_DIRはそれぞれ、
defaultのstaticではなくどのフォルダを参照するか、そのパスがどこかを参照。  
他のdefaultにstatic,templates,media,fixturesがある。
パスの通し方は形式的なもので、urls.pyで調整。  
サイトのurlsそのものではないものを通すので、書き方に注意
