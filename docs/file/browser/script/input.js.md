# input.js

キーボードの入力があった際にJavaScrptで入力されたキーを検出し、C言語(Wasm)の関数に入力されキーを入れ、Wasmで高速に入力されたキーをキーコード(数値型)に変換。
変換されたキーコードを"communication.js"を通じてデバイスに送信。
マウスの入力があった際にJavaScrptで入力された内容を検出し、"communication.js"を通じてデバイスに送信。



マイクとかも未入力