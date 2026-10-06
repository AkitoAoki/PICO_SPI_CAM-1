# PICO_SPI_CAM サンプル
このサンプルでは、Pico プラットフォーム上で SPI カメラミニカメラを C 言語または Python で駆動する方法を示します。
このデモは ArduCAM_Mini_2MP/5MP 用に作成されており、PC ソフトウェアと併用して使用する必要があります。

# ドライバのダウンロード
```bash
git clone https://github.com/ArduCAM/PICO_SPI_CAM.git
```

# C 言語を使用して SPI カメラを駆動する
開発環境を構築するには、公式マニュアルを参照してください。リンクは以下のとおりです。
```bash
https://www.raspberrypi.org/documentation/rp2040/getting-started/#getting-started-with-c
```
- コンパイル
コンパイルするドライバを選択してください。デフォルトは Arducam_MINI_2MP_Plus_Videostreaing です。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/1.png)
```bash
cd PICO_SPI_CAM/C
mkdir build
cd build
cmake ..
make
```
PICO_SPI_CAM/C/build/Examples/Arducam_MINI_2MP_Plus_Videostreaing/Arducam_mini_2mp_plus_videostreaming.uf2 を Pico にコピーしてテストを実行します。
PC ソフトウェアを開き、ポート番号、ボーレート、カメラモデルを設定し、「Capyure」をクリックすると画像が表示されます。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/2.png)

# Python を使用して SPI カメラを駆動する
## 注記: 開発システムは Windows です。
開発環境を構築するには、公式マニュアルを参照してください。リンクは以下のとおりです。
```bash
https://circuitpython.org/
```
開発ソフトウェアのダウンロードリンクです。
```bash
https://thonny.org/
```

## PICO_SPI_CAM/Python/ 配下の boot.py を除くファイルを Pico デバイスにコピーします。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/3.png)
## Thonny ソフトウェアを開き、環境とポート番号を選択します。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/4.png)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/5.png)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/10.png)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/11.png)
## PICO_SPI_CAM/Python/ 配下の boot.py を Pico にコピーし、Pico を再起動してデバイスマネージャーを開き、USB 通信に新しいポート番号を使用します。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/12.png)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/13.png)
## カメラドライバを開きます。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/6.png)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/7.png)
## 「Run」をクリックすると [48] が表示され、CameraType が OV2640、SPI interface OK であることが表示され、カメラが初期化されたことを意味します。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/8.png)
## HostApp フォルダ内の hostapp.exe を開き、USB 通信に使用するポート番号を選択して「Image」をクリックします。
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/pico/Spi%20Camera/9.png)