# comm-converter.c

USBまたはBluetooth(BLE)をC言語(WebAssembly)で高速に独自のフォーマット(communication.mdを参照)にエンコード・デコード。
ブラウザのUSBデバイスの信号をエンコードする"usbEncoder()"という関数を所持。
デバイスからのUSBデバイスへの信号をデコードする"usbDecoder()"という関数を所持。
ブラウザのBLEデバイスの信号をエンコードする"bleEncoder()"という関数を所持。
デバイスからのBLEデバイスへの信号をデコードする"bleDecoder()"という関数を所持。