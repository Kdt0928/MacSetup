# mac-setup
## homebrewのインストール
1. [homebrew](https://brew.sh/)のサイトにある**Install Homebrew**の下にあるコードをコピー
2. ターミナルを開いてコマンドを実行
    ```sh
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
## homebrew-caskのインストール
1. ターミナルでコマンドを実行
   ```
   brew install cask
   ```
## brewfileでライブラリ管理
### brew bunlde
参考：[brew bunldeの使い方](https://gist.github.com/yoshimana/43b9205ddedad0ad65f2dee00c6f4261)
|コマンド|内容|
|---|---|
|`brew bunlde dump`|インストール済みのライブラリをBrewfileに出力|
|`brew bunlde`|Brewfileからライプラリをインストール|
|`brew bunlde cleanup`|Brewfileに記載のないライブラリを削除|
|`brew bunlde check`|Brewfile記載の内、インストール・アップグレードが必要なものを表示|
|`brew bunlde list`|Brewfile記載のリストを表示|
### Brewfileの構文
* **brew**  
   Homebrewに正式に登録されたライブラリをインストール
   ```
   brew "peco"
   ```
* **tap**  
   Homebrewに正式に登録されていないライブラリをインストール
   ```
   tap "mackerelio/mackerel-agent"
   ```
* **cask**  
   Google Chromeなど，Macアプリをインストール
   ```
   cask "keycastr"
   ```
* **mas**  
   App StoreからMacアプリをインストール
   ```
   mas "CotEditor", id: 1024640650
   ```