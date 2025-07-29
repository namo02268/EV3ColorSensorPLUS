# EV3 ColorSensor PLUS
## 概要 (Overview)
EV3 ColorSensor PLUS は、LEGO MINDSTORMS EV3 向けの拡張プログラミングブロックです。標準のカラーセンサーブロックでは取得できない **RGBデータ** や **生の反射光の強さ** を取得できるのが特徴です。

EV3 ColorSensor PLUS is an extended programming block for LEGO MINDSTORMS EV3.It enables to obtain RGB data and raw reflected light intensity.

本ブロックでは、以下の4つのモードを追加しています。

This block adds the following four modes.

---
### RGB 測定モード (Measure RGB Mode)
センサーから読み取った 赤（Red）・緑（Green）・青（Blue） の各チャンネルの値（範囲：0〜1024）をそのまま出力します。カラー情報をより細かく扱いたい場面で役立ちます。

Outputs the raw sensor values of Red, Green, and Blue channels (range: 0–1024). Useful when you need more detailed color information.

![RGB_Measure](./images/README_RGB_Measure.png)

---
### RGB 比較モード (Compare RGB Mode)
あらかじめ設定したRGBの範囲と現在のセンサー値を比較し、条件に一致すれば true、一致しなければ false を返します。スイッチブロックやループの条件にも使用することができます。

Compares the current sensor RGB values with preset RGB ranges. Returns true if conditions are met, otherwise false. Can be used in switch blocks or loop conditions.

![RGB_Compare](./images/README_RGB_Compare.png)

---
### 生の反射光 測定モード (Measure Raw Reflected Light Intensity Mode)
通常の反射光モードは 0〜100% に正規化された値を返しますが、このモードでは、センサーから取得した未加工のADC値 を直接出力します。より広い値の範囲を扱えるため、より細かな変化の検出や滑らかな制御が可能になります。

The standard reflected light mode returns a normalized value (0–100%), but this mode outputs the raw ADC value directly from the sensor. Handling a wider range enables finer detection and smoother control.

![RGB_Measure](./images/README_RawREF_Measure.png)

---
### 生の反射光 比較モード (Compare Raw Reflected Light Intensity Mode)
設定した閾値と比較演算子を使い、生の反射光の値を判定します。

Evaluates the raw reflected light value using preset thresholds and comparison operators.

![RGB_Measure](./images/README_RawREF_Compare.png)

## インストール方法
- [Releases ページ](https://github.com/namo02268/EV3ColorSensorPLUS/releases)より 「EV3ColorSensorPLUS.ev3b」 をダウンロード
- EV3ソフトウェアを起動し、
　[ツール] > [ブロック インポート] を開く
- ダウンロードした .ev3b ファイルを読み込む
- EV3ソフトウェアを再起動
- 追加されたブロックをプログラムにドラッグ＆ドロップして使用

## Installation
- Download the "EV3ColorSensorPLUS.ev3b" file from the [Releases page]((https://github.com/namo02268/EV3ColorSensorPLUS/releases)).
- Launch the EV3 software and open [Tools] > [Block Import].
- Import the downloaded .ev3b file.
- Restart the EV3 software.
- Drag and drop the added blocks into your program to use them.

## 使用例 (Example)
以下は、ロボットが前進し、「緑色 を検出したら停止する」処理の例です。

This is an example where the robot moves forward and stops when detecting the color green.

![RGB_Example](./images/README_RGB_Example.png)
