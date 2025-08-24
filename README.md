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
├── docs                         - 資料のフォルダ
│   ├── tree.txt                   - ディレクトリ構造
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
│           ├── media.go               - デバイスから送られた映像や音声をブラウザに出力
│           ├── input.go               - ブラウザの操作をデバイスに送信
│           ├── ports.go               - デバイスとブラウザのUSBやBluetooth、AUXなどのIOポートの入出力を連動
│           └── communication.go       - デバイスとの通信を確立
├── app                          - ビルドされたアプリケーション本体
│   ├── app.exe                    - Windowsのコマンドラインアプリケーション
│   └── app.deb                    - Linux(debian系)のコマンドラインアプリケーション
├── LICENSE                      - このリポジトリのライセンスファイル
└── README.md                    - このリポジトリのREADMEファイル
```

## 使用方法
1. app.exeまたはapp.debを開く
2. コマンドラインでパスワードを設定する
3. ブラウザでコマンドラインに出力されたURLにアクセスする