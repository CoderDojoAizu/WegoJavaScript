## 1. [wego]クラス：基本動作を集めたクラス

1-1. おじぎをする

```javascript
await commands.wego.bow();
```

1-2. バイバイする

```javascript
await commands.wego.bye();
```

1-3. 後ろに戻る

```javascript
await commands.wego.goBackward();
```

1-4. 少し後ろに戻る

```javascript
await commands.wego.goBackwardLittle();
```

1-5. 後ろに（１歩）戻る

```javascript
await commands.wego.goBackwardNStepsSlowly(1);
```

※()内は歩数を 1~4 で指定

1-6. 前に進む

```javascript
await commands.wego.goForward();
```

1-7. 少し前に進む

```javascript
await commands.wego.goForwardLittle();
```

1-8. 前に(1 歩)進む

```javascript
await commands.wego.goForwardNStepsSlowly(1);
```

※()内は歩数を 1~4 で指定

1-9. 左足でキックする

```javascript
await commands.wego.kickWithLeftFoot();
```

1-10. 右足でキックする

```javascript
await commands.wego.kickWithRightFoot();
```

1-11. 左に（1 回）ずれる

```javascript
await commands.wego.moveLeftTimes(1);
```

※()内は回数を 1~3 で指定

1-12. 右に（1 回）ずれる

```javascript
await commands.wego.moveRightTimes(1);
```

※()内は回数を 1~3 で指定

1-13. 左手を上げて下げる

```javascript
await commands.wego.raiseLeftHand();
```

1-14. 右手を上げて下げる

```javascript
await commands.wego.raiseRightHand();
```

1-15. 目の色を消灯する

```javascript
await commands.wego.setLED("OFF");
```

1-16. 目の色を赤にする

```javascript
await commands.wego.setLED("R");
```

1-17. 目の色を青にする

```javascript
await commands.wego.setLED("B");
```

1-18. 目の色を黄にする

```javascript
await commands.wego.setLED("Y");
```

1-19. 少し左を向く

```javascript
await commands.wego.turnBitLeft();
```

1-20. 少し右を向く

```javascript
await commands.wego.turnBitRight();
```

1-21. 左を向く

```javascript
await commands.wego.turnLeft();
```

1-22. わずかに左を向く

```javascript
await commands.wego.turnLittleLeft();
```

1-23. わずかに右を向く

```javascript
await commands.wego.turnLittleRight();
```

1-24. 右を向く

```javascript
await commands.wego.turnRight();
```

## 2. [wegoDance]クラス：体操などのダンス系動作を集めたクラス

2-1. ♪ 桜イルミネーション

```javascript
await commands.wegoDance.SakuraIllumination();
```

2-2. 目の色を変える

```javascript
await commands.wegoDance.changeEyeColor();
```

2-3. 左手でチョップする

```javascript
await commands.wegoDance.chopWithLeftHand();
```

2-4. 右手でチョップする

```javascript
await commands.wegoDance.chopWithRightHand();
```

2-5. カスタマイズダンス

```javascript
await commands.wegoDance.customizeDance(
  "sound1.wav",
  "88",
  "88",
  "88",
  "88",
  "189"
);
```

※ミュージック、ダンス、決めポーズそれぞれ以下の選択肢を有する

2-6. ダンスする ♪

```javascript
await commands.wegoDance.dance();
```

2-7. モゾモゾする

```javascript
await commands.wegoDance.fidget();
```

2-8. ガッツポーズする

```javascript
await commands.wegoDance.holdUpFists();
```

2-9. フレフレ

```javascript
await commands.wegoDance.hooray();
```

2-10. リズムをとる

```javascript
await commands.wegoDance.horizontalRhythm();
```

2-11. ガッカリする

```javascript
await commands.wegoDance.lookDisappointed();
```

2-12. ごっつあんポーズをする

```javascript
await commands.wegoDance.lookGottuan();
```

2-13. オーマイガッポーズをする

```javascript
await commands.wegoDance.lookOmg();
```

2-14. 左足ローキック

```javascript
await commands.wegoDance.lowKickWithLeftFoot();
```

2-15. 右足ローキック

```javascript
await commands.wegoDance.lowKickWithRightFoot();
```

2-16. 左足を高く上げる

```javascript
await commands.wegoDance.raiseLeftLeg();
```

2-17. 右足を高く上げる

```javascript
await commands.wegoDance.raiseRightLeg();
```

## 3. [wegoSensor]クラス：照度・距離・二次元コードスキャナー等センシング機能をもつクラス

3-1. 充電

```javascript
while ((await commands.wegoSensor.batteryCharging()) == 0) {
  await commands.wego.bow();
}
await commands.wego.bye();
```

3-2. 体力

```javascript
while ((await commands.wegoSensor.batteryMonitor()) >= 30) {
  await commands.wego.bow();
}
await commands.wego.bye();
```

3-3. 二次元コードリーダー

```javascript
await commands.wegoSensor.read2dCode();
```

3-4. 周囲の明るさ

```javascript
while ((await commands.wegoSensor.sensorIlluminance()) >= 30) {
  await commands.wego.bow();
}
await commands.wego.bye();
```

3-5. 障害物までの距離

```javascript
while ((await commands.wegoSensor.sensorTOF()) >= 10) {
  await commands.wego.bow();
}
await commands.wego.bye();
```

3-6. カメラの画像を解析する

```javascript
await commands.wegoSensor.setInput("webcam");
```

3-7. ステージの画像を解析する

```javascript
await commands.wegoSensor.setInput("stage");
```

3-8. シャッター

```javascript
await commands.wegoSensor.shutter();
```

## 4. [wegoSpecial]クラス：前転・後転などスペシャルな動作を集めたクラス

4-1. （注意）ダッシュ 30% 9 歩

```javascript
await commands.wegoSpecial.dash30Percentage();
```

4-2. （注意）ダッシュ 60% 9 歩

```javascript
await commands.wegoSpecial.dash60Percentage();
```

4-3. 元気よく後ろに（１歩）戻る

```javascript
await commands.wegoSpecial.goBackwardNSteps(1);
```

※()内は歩数を 1~4 で指定

4-4. 元気よく前に（１歩）進む

```javascript
await commands.wegoSpecial.goForwardNSteps(1);
```

※()内は歩数を 1~4 で指定

4-5. ロボットにモーション ID101 を送信する（待機なし）

```javascript
await commands.wegoSpecial.motionWithId("101");
```

4-6. モーション ID101 のモーションを動かす（待機あり）

```javascript
await commands.wegoSpecial.motionWithIdWait("101");
```

4-7. ロボットにモーション ID101 を送信する（待機あり）

```javascript
await commands.wegoSpecial.sendCommand("101");
```

4-8. 座り姿勢から立つ

```javascript
await commands.wegoSpecial.sitDownAndStandUp();
```

4-9. Special1

```javascript
await commands.wegoSpecial.special1();
```

4-10. Special2

```javascript
await commands.wegoSpecial.special2();
```

4-11. Special3

```javascript
await commands.wegoSpecial.special3();
```

4-12. 立ち姿勢から座る

```javascript
await commands.wegoSpecial.standUpAndSitDown();
```

## 5. [wegoSpeech]クラス：音声合成・音声認識など会話機能をもつクラス

5-1. 言語

```javascript
await commands.wegoSpeech.setLanguage("ja-JP");
console.warn(await commands.wegoSpeech.getLanguage());
```

5-2. 発音評価の結果

```javascript
await commands.wegoSpeech.setLanguage("en-US");
console.warn(await commands.wegoSpeech.getLanguage());
console.warn(await commands.wegoSpeech.getRecognitionScore());
```

5-3. 音声認識の結果

```javascript
await commands.wegoSpeech.startSpeech2Text();
console.warn(await commands.wegoSpeech.getRecognitionText());
```

5-4. 〇〇としゃべる

```javascript
await commands.wegoSpeech.startText2Speech("こんにちは");
```

5-5. 翻訳

```javascript
await commands.wegoSpeech.translateByDeepL("Hello", "JA");
await commands.wegoSpeech.translateByDeepL("さようなら", "EN");
```

## 6. [wegoMotionCreation]クラス：モーションをゼロから制作できる機能をもつクラス

6-1. 関節角度取得

```javascript
for (let i = 0; i < 8; i++) {
  console.warn(await commands.wegoMotionCreation.getAngle(i));
}
```

6-2. 関節角度設定(右肩)

```javascript
await commands.wegoMotionCreation.angleVid0(160, 100);
```

6-3. 関節角度設定(左肩)

```javascript
await commands.wegoMotionCreation.angleVid1(160, 100);
```

6-4. 関節角度設定(右腿)

```javascript
await commands.wegoMotionCreation.angleVid2(160, 100);
```

6-5. 関節角度設定(右足首)

```javascript
await commands.wegoMotionCreation.angleVid3(160, 100);
```

6-6. 関節角度設定(右足)

```javascript
await commands.wegoMotionCreation.angleVid4(160, 100);
```

6-7. 関節角度設定(左腿)

```javascript
await commands.wegoMotionCreation.angleVid5(160, 100);
```

6-8. 関節角度設定(左足首)

```javascript
await commands.wegoMotionCreation.angleVid6(160, 100);
```

6-9. 関節角度設定(左足)

```javascript
await commands.wegoMotionCreation.angleVid7(160, 100);
```

6-10. 関節角度設定(全指定)

```javascript
await commands.wegoMotionCreation.allAngles(
  "",
  180,
  180,
  180,
  180,
  180,
  180,
  180,
  180
);
```

6-11. 目の色

```javascript
await commands.wegoMotionCreation.setLed("#00FF00");
```

6-12. 関節モーション時間 200 ミリ秒

```javascript
await commands.wegoMotionCreation.setMotionTime(200);
```

6-13. 回転力 100%

```javascript
await commands.wegoMotionCreation.setTorque(100);
```

6-14. 回転力オフ

```javascript
await commands.wegoMotionCreation.torqueOff();
```

## 7. [ml2scratch]クラス：機械学習の機能をもつクラス

7-1. ラベル 1 を学習する

```javascript
await commands.ml2scratch.addExample1();
```

7-2. ラベル 2 を学習する

```javascript
await commands.ml2scratch.addExample2();
```

7-3. ラベル 3 を学習する

```javascript
await commands.ml2scratch.addExample3();
```

7-4. （引数）のカメラを使用する

```javascript
await commands.ml2scratch.changeCamera("machine");
await commands.ml2scratch.changeCamera("robot");
```

7-5. 学習データをダウンロード

```javascript
await commands.ml2scratch.download();
```

7-6. ラベル 1 の枚数

```javascript
await commands.ml2scratch.getCountByLabel1();
```

7-7. ラベル 2 の枚数

```javascript
await commands.ml2scratch.getCountByLabel2();
```

7-8. ラベル 3 の枚数

```javascript
await commands.ml2scratch.getCountByLabel3();
```

7-9. ラベル 4 の枚数

```javascript
await commands.ml2scratch.getCountByLabel4();
```

7-10. ラベル 5 の枚数

```javascript
await commands.ml2scratch.getCountByLabel5();
```

7-11. ラベル 6 の枚数

```javascript
await commands.ml2scratch.getCountByLabel6();
```

7-12. ラベル 7 の枚数

```javascript
await commands.ml2scratch.getCountByLabel7();
```

7-13. ラベル 8 の枚数

```javascript
await commands.ml2scratch.getCountByLabel8();
```

7-14. ラベル 9 の枚数

```javascript
await commands.ml2scratch.getCountByLabel9();
```

7-15. ラベル 10 の枚数

```javascript
await commands.ml2scratch.getCountByLabel10();
```

7-16. ラベル（引数）の枚数

```javascript
await commands.ml2scratch.getCountByLabel(11);
```

7-17. ラベル

```javascript
const label = await commands.ml2scratch.getLabel();
```

7-18. ラベル（引数）の学習をリセット(引数：all（全て）、1~10)

```javascript
await commands.ml2scratch.reset("all");
await commands.ml2scratch.reset("1");
// ...
await commands.ml2scratch.reset("10");
```

7-19. ラベル（引数）の学習をリセット(引数：自由入力)

```javascript
await commands.ml2scratch.resetAny(11);
```

7-20. ラベル付けを（引数）秒間に 1 回行う

```javascript
await commands.ml2scratch.setClassificationInterval(1);
await commands.ml2scratch.setClassificationInterval(0.5);
await commands.ml2scratch.setClassificationInterval(0.2);
await commands.ml2scratch.setClassificationInterval(0.1);
```

7-21. （引数）の画像を学習/判定する

```javascript
await commands.ml2scratch.setInput("webcam");
await commands.ml2scratch.setInput("stage");
```

7-22. ビデオの透明度を（引数）にする

```javascript
await commands.ml2scratch.setVideoTransparency(50);
```

7-23. ラベル付けを（引数）にする

```javascript
await commands.ml2scratch.toggleClassification("off");
await commands.ml2scratch.toggleClassification("on");
```

7-24. ラベル（引数）を学習する(引数：4~10)

```javascript
await commands.ml2scratch.train(4);
await commands.ml2scratch.train(5);
// ...
await commands.ml2scratch.train(10);
```

7-25. ラベル（引数）を学習する(引数：自由入力)

```javascript
await commands.ml2scratch.trainAny(11);
```

7-26. 学習データをアップロード

```javascript
await commands.ml2scratch.upload();
```

7-27. ビデオを（引数）にする

```javascript
await commands.ml2scratch.videoToggle("off");
await commands.ml2scratch.videoToggle("on");
await commands.ml2scratch.videoToggle("on-flipped");
```
