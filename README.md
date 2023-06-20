# Unity_VR_metabase
Unityによるメタバース発表会場を作ることを目的として作成したリポジトリです。
大学の研究として使用しています。

## 参考サイト
Aska,「Unity初心者がawsサーバーとWebSocketを使ってのリアルタイム同期通信について学ぶ」[[https://www.aska-ltd.jp/jp/blog/105]]　（2023/6/20）

### 使用環境

Unity 20.51.?

aws ec2

node.js v14.15.1

---

### 最低限のawsでの手順
```
sudo yum update

// 必要な開発ツールのインストール
sudo yum -y install gcc-c++
sudo yum -y install git

// nvmのダウンロード
git clone https://github.com/creationix/nvm.git ~/.nvm

// nvm実行コマンドのパス設定
source ~/.nvm/nvm.sh

// 再ログイン時に設定したパスが有効になるように、プロフィールファイルに下記を追加
vi /home/[ログインユーザー名]/.bash_profile\

========================================
# nvm
if [[ -s ~/.nvm/nvm.sh ]] ; then
        source ~/.nvm/nvm.sh ;
fi
========================================
// Node.jsの14.15.1をインストール
nvm install 14.15.1

// 使用するバージョンを指定
nvm use v14.15.1

// 有効なNode.jsのバージョンを確認　使用するバージョンは(v14.15.1)となります。
node -v

//WebSocketのインストール
npm install websocket
//
```
###コピペ用
```
sudo yum update
sudo yum -y install gcc-c++
sudo yum -y install git
git clone https://github.com/creationix/nvm.git ~/.nvm
source ~/.nvm/nvm.sh
nvm install 14.15.1
nvm use v14.15.1
node -v
npm install websocket
```

#### 再ログイン時に設定したパスが有効になるように、プロフィールファイルに下記を追加

```
vi /home/[ログインユーザー名]/.bash_profile\
```

内容(編集モードに入る「i」→下のコードを１番したにコピペ→コマンドモードに入る「ESC」→:wqを入力)

```
# nvm
if [[ -s ~/.nvm/nvm.sh ]] ; then
        source ~/.nvm/nvm.sh ;
fi
```
