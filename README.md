# gs2d(<u>G</u>eneric <u>S</u>erial-bus <u>S</u>ervo <u>D</u>river) Library

> 汎用シリアルバス RC サーボドライバ・ライブラリ

## gs2d とは

gs2d は、市販のシリアルバス RC サーボ(通称:シリアルサーボ)を同一のメソッドでプロトコルに依存せずに動かすことを目的に開発したライブラリです。

2020 年 8 月現在、サポートする言語は Python、C#、C++ の 3 種。各言語のリポジトリは下記で管理しています。

> 表 1 サポートする言語、および各リポジトリ

|        | Name        | Repository                                         |
| :----- | ----------- | -------------------------------------------------- |
| C++    | gs2d-cpp    | <https://github.com/karakuri-products/gs2d-cpp>    |
| C#     | gs2d-csharp | <https://github.com/karakuri-products/gs2d-csharp> |
| python | gs2d-python | <https://github.com/karakuri-products/gs2d-python> |

gs2d でサポートするメーカ/規格は表 2 のとおりです。対応/動作確認が完了しているシリアルサーボの機種は<a href="https://docs.google.com/spreadsheets/d/15XlF4kySq219ICrvgJmQ_NEENOpA3_AKKTeR7gI3orM/edit?usp=sharing" target="_blank">こちら</a>で確認できます。

> 表 2 サポートするメーカ/規格

| Manufacturer                          | Series                      | Protocol                             |
| ------------------------------------- | --------------------------- | ------------------------------------ |
| ロボティズ (ROBOTIS Inc.)             | Dynamixel X Series          | Protocol 2.0                         |
| 近藤科学 (KONDOKondo Kagaku Co.,Ltd.) | B3M Serises <br> KRS Series | B3M protocol <br> ICS3.6 <br> ICS3.5 |
| 双葉電子工業 (FUTABA Corp.)           | Command Type Servo          | Command Type Protocol                |

また、gs2d に適合するシリアルサーボ・ドライバ製品、ならびにその要件については下記のリポジトリに情報をまとめています。あわせてご確認ください。

> 表 3 gs2d 適合ハードウェアに関するリポジトリ

| Name        | Repository                                         |
| ----------- | -------------------------------------------------- |
| gs2d-hw    | <https://github.com/karakuri-products/gs2d-hw>    |

## 基本仕様

gs2d の基本仕様は以下のとおりです。いずれの言語の実装もこれらを満たします。

> - 送信コマンドによるループバックは無視。
> - 回転角度の単位は deg 、回転方向は CCW を正、CW を負。
>   分解能は各社仕様にあわせて gs2d 側で吸収。
> - メーカ間で共通化不可能な機能についてはメモリ操作メソッドで対応。

## 今後の開発予定

以下に示すメーカ/規格については対応を検討中です。

> 表 4 対応検討中のメーカ/規格

| Manufacturer                      | Series                       | Protocol             |
| :-------------------------------- | ---------------------------- | -------------------- |
| 小西模型 (Konishi Mokei Co.,Ltd.) | JR PROPO XBUS Series         | XBUS Protocol v1.1.0 |
| ヴイストン (Vstone Co.,Ltd.)      | Vservo series (Discontinued) | Vservo Protocol      |

## ライセンス

gs2d は Apache License 2.0 で利用いただけます。詳細は ./LICENSE を参照のこと。
