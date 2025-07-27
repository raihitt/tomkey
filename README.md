## description
- このキーボードは無線分割式 40% 19mm トラックボール内蔵のキーボードになります。
  ![tomkey keyboard](img/tomkeyimg.png)

## ビルドガイド
- https://github.com/pukuhei/tomkey/blob/main/build_guide/build_guide.md
## スペック

- ファームウェア
  - ZMK を使用しています
  - ZMKStudio に対応しております
- ハードウェア
  - 43 キー
  - choc v1/v2、lofree 系列のスイッチが使用可能
  - 左手側が master,右手側が slave になります
  - 左手側に OLED 内蔵
  - トラックボールはケースごとマグネットで張り付いているので、脱着可能です
  - バッテリー対応 2 つ必要です
    - 横 25mm,縦 35mm,厚さ 5mm 以内のものを使用してください
    - 製作者はこちらを使用しています(https://amzn.asia/d/ebvtzoP)。250mAh で大体 1 週間は持ちます(1 日 5 時間使用くらい)
    - リチウムイオンバッテリーは十分注意して取り扱ってください(https://www.baj.or.jp/battery/safety/safety16.html)
    - 市販のバッテリーの極性が個体によって異なる例が確認されておりますので、極性には気をつけてご利用ください。tomkey では赤色を+極として作成しております

## 電源および充電について
※購入したバッテリーによっては極性が逆になっている可能性がありますので、十分にご確認の上で接続をお願いいたします！(表記と端子が逆の事例もありました)
- スイッチを ON にしている状態で USB に接続することで充電されます。充電しながらの使用も可能です
- スイッチが OFF の状態で USB を接続すると USB からの給電で使用できますが、OFF の状態ではバッテリーに充電はされません
  - 安全上意図的にバッテリー ON 状態でないと充電されない仕様になっております
- バッテリー残量に関しては oled 上に表示されるようになっております
  - 上側が左手のバッテリー残量
  - 下側が右手のバッテリー残量

## oled の切り替えについて

- デフォルトでは us 配列の mac に適した配置になっております
- また oled も mac に併せてありますので、windows の方は以下の設定を n に指定することで表示が切り替わります
- config/boards/shields/tomkey/tomkey_L.conf
- `CONFIG_ZMK_DONGLE_DISPLAY_MAC_MODIFIERS=n`にする

## キーマップについて

- ZMKstudio にて確認・編集を行なってください

  - https://zmk.studio/

- ZMK keymap-editor も使用できます
  - マクロ設定などを使いたい場合はこちらを使うとべんりです
  - https://nickcoutsos.github.io/keymap-editor
  - ご使用の時は本リポジトリをフォークしてお使いください
    - ※フォークしてマクロ等にパスワードなどを設定する際はリポジトリが public になってしまい情報漏洩につながりますのでご注意ください

### レイヤーマップ

- レイヤー 0 がデフォルトです
- レイヤー 1 がオートマウスレイヤーです
  - トラックボール操作中に切り替わるレイヤーです(400ms でレイヤー０に切り替わります)
- レイヤー 2 がスクロールレイヤーです
  ![tomkey layer0](img/layer0.png)
  ![tomkey layer1](img/layer1.png)
  ![tomkey layer2](img/layer2.png)
  ![tomkey layer3](img/layer3.png)
  ![tomkey layer4](img/layer4.png)
  ![tomkey layer5](img/layer5.png)
  ![tomkey layer6](img/layer6.png)

## その他

不明な点がある場合は下記アカウントにご連絡ください
https://x.com/tomcat09131
# Actions test
