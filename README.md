# http-remote-desktop

## 概要
ブラウザからHTTP通信でリモートデスクトップをするためのリポジトリです。
このリポジトリでは、ブラウザからウェブページとしてアクセスし、ブラウザのAPIを利用して通常のPCのように快適にリモートデスクトップを実現することです。

## 使用技術・言語

### プログラミング言語
- Go言語
- HTML
- CSS
- JavaScript

### 使用技術
- Web Worker
- WebGPU
- Canvas
- Web Audio
- WebRTC
- WebSocket
- Web RTC
- WebUSB
- Web Bluetooth

## ファイル構成
```
http-remote-desktop
├── docs                         - ドキュメントのフォルダ
│   ├── file                       - ファイルの説明のドキュメントのフォルダ
│   │   ├── device                   - デバイス側のソースコードについてのドキュメントのフォルダ
│   │   │   ├── main.go.md             - "main.go"についてのドキュメント
│   │   │   ├── media.go.md            - "media.go"についてのドキュメント
│   │   │   ├── input.go.md            - "input.go"についてのドキュメント
│   │   │   ├── ports.go.md            - "ports.go"についてのドキュメント
│   │   │   └── communication.go.md    - "communication.go"についてのドキュメント
│   │   ├── browser                  - ブラウザ側のソースコードについてのドキュメントのフォルダ
│   │   │   ├── index.html.md          - "index.html"についてのドキュメント
│   │   │   ├── style.css.md           - "style.css"についてのドキュメント
│   │   │   └── script                 - "index.html"のページのJavaScriptのファイルについてのドキュメントのフォルダ
│   │   │       ├── main.js.md           - "main.js"についてのドキュメント
│   │   │       ├── media.js.md          - "media.js"についてのドキュメント
│   │   │       ├── input.js.md          - "input.js"についてのドキュメント
│   │   │       ├── ports.js.md          - "ports.js"についてのドキュメント
│   │   │       └── communication.js.md  - "communication.js"についてのドキュメント
│   │   └── app.md                   - デバイス上で動作するコマンドラインアプリケーション本体についてのドキュメント
│   └── tree.txt                   - ディレクトリ構造
├── src                          - ソースコードのフォルダ
│   ├── windows                    - Windows用プログラム
│   │   ├── main.go                  - コマンドラインアプリケーション本体
│   │   ├── media.go                 - デバイスの画面、音声などを取得し、ブラウザに出力
│   │   ├── input.go                 - ブラウザからの操作をデバイスに反映
│   │   ├── ports.go                 - デバイスとブラウザのUSBやBluetooth、AUXなどのIOポートの入出力を連動
│   │   └── communication.go         - ブラウザとの通信を確立
│   ├── linux_debian               - Linux(debian系)用プログラム
│   │   ├── main.go                  - コマンドラインアプリケーション本体
│   │   ├── media.go                 - デバイスの画面、音声などを取得し、ブラウザに出力
│   │   ├── input.go                 - ブラウザからの操作をデバイスに反映
│   │   ├── ports.go                 - デバイスとブラウザのUSBやBluetooth、AUXなどのIOポートの入出力を連動
│   │   └── communication.go         - ブラウザとの通信を確立
│   └── browser                    - ブラウザ側のページ
│       ├── index.html               - 接続ページ
│       ├── style.css                - スタイルシート
│       └── script                   - プログラム
│           ├── main.js                - メインプログラム
│           ├── media.js               - デバイスから送られた映像や音声をブラウザに出力
│           ├── input.js               - ブラウザの操作をデバイスに送信
│           ├── ports.js               - デバイスとブラウザのUSBやBluetooth、AUXなどのIOポートの入出力を連動
│           └── communication.js       - デバイスとの通信を確立
├── app                          - ビルドされたアプリケーション本体
│   ├── app.exe                    - Windowsのコマンドラインアプリケーション
│   ├── app.app                    - macOSのコマンドラインアプリケーション
│   └── app.deb                    - Linux(debian系)のコマンドラインアプリケーション
├── LICENSE                      - このリポジトリのライセンスファイル
└── README.md                    - このリポジトリのREADMEファイル
```

## 使用方法
1. app.exeまたはapp.debを開く
2. コマンドラインでパスワードを設定する
3. ブラウザでコマンドラインに出力されたURLにアクセスする