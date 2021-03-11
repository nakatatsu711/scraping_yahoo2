## 概要
検索キーワードが入力されたテキストファイルを読み込みます。  
[Yahoo!JAPAN](https://www.yahoo.co.jp)のトップページから読み込んだ検索キーワードで検索します。  
1番目にヒットしたページに遷移し、URLを取得します。  
検索キーワードとURLをセットにしてテキストファイルに書き出します。



## システム環境
以下で動作確認済みです。  
OS：macOS 10.15.6  
Python：3.6.9



## 実行方法
### ライブラリインストール
以下の2通りの方法がありますので、どちらかでインストールしてください。
```
$ pip install selenium
```
```
$ pip install -r requirements.txt
```


### ChromeDriverについて
ブラウザはGoogleChromeを使用します。  
ブラウザを自動操作するためにはChromeDriverが必要です。  
以下から自分のGoogleChromeと同じバージョンのドライバーをダウンロードします。  
[ChromeDriverのダウンロードはこちら](https://sites.google.com/a/chromium.org/chromedriver/downloads)

ChromeDriverをダウンロードしたら解凍して、任意の場所に配置します。  
そして、`chromedriver_path`のところに自分がダウンロードした場所を指定します。


### 読み込み用のテキストファイル
以下は読み込み用のテキストファイルの一例です。実際のクラウドソーシング案件から引用してます。  
`yahoo2_data.txt`のファイル名でPythonの実行ファイルと同じ場所に配置します。
```
立川 焼肉 鉄板粋
新宿 食べログ エビス 新宿西口店
新宿 パーティー エビス西口店
立川 食べログ 千寿
立川 イタリアン rapport
新宿 日本酒 エビス西口店
立川 個室 rapport
新宿 個室 エビス西口店
接待 立川 rapport
立川 飲み屋 しゃぶ粋
新宿 和食 エビス西口店
ステーキ 立川 せんじゅ
立川 居酒屋 しゃぶ粋
新宿 グルメ エビス西口店
立川 洋食 せんじゅ新宿 居酒屋 エビス西口店
立川 グルメ しゃぶ粋
新宿駅 居酒屋 エビス西口店
立川 飲み放題 鉄板粋
新宿西口 居酒屋 エビス西口店
立川 食べログ しゃぶ粋
```


### 実行
コマンドラインで実行します。
```
$ python scraping_yahoo2.py
```
