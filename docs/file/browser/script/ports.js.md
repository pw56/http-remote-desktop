# ports.js

ブラウザのUSBやBluetoothに接続されている外部のデバイスをデバイス(リモート)に接続する。
Web Workerで別スレッドを立ち上げ、WebUSBでUSBデバイスとバイナリで通信し、C言語(Wasm)の"comm-converter.wasm"の"usbEncoder()"または"usbDecoder()"という関数を用いて高速にエンコード・デコード。
Web Workerで別スレッドを立ち上げ、Web BluetoothでBLEデバイスと通信し、C言語(Wasm)の"comm-converter.wasm"の"bleEncoder()"または"bleDecoder()"という関数を用いて高速にエンコード・デコード。