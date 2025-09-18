# 25-9-18-XIAO-ESP32S3-USBdriver
ESP32-S3のUSB機能を使用するには専用のドライバのインストールが必要です

JTAG通信は、サポートされているすべてのプラットフォームで動作するはずです。Windowsをお使いの場合は、LIBUSB_ERROR_NOT_FOUNDエラーが発生する可能性があります。この問題を解決するには、 ESP-IDFツールインストーラーのバージョン2.8以降を使用し、「Espressif - WinUSB support for JTAG (ESP32-C3/S3)」ドライバーを選択してください。インストーラーを再実行したくない場合は、PowerShellから以下のコマンドを実行することで、idf-envで同じことを実現できます。

Invoke-WebRequest 'https://dl.espressif.com/dl/idf-env/idf-env.exe' -OutFile .\idf-env.exe; .\idf-env.exe driver install --espressif

https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/api-guides/jtag-debugging/configure-builtin-jtag.html

<img width="1005" height="465" alt="image" src="https://github.com/user-attachments/assets/0811a41f-662d-4c9d-82a9-3c0809a66f78" />
