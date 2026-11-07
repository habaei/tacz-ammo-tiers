# TaCZ Ammo Tiers (Minecraft 1.21.1)

TaCZ の弾薬箱と同じ弾薬出し入れ機能を使う、銅・エメラルド・ネザライト製の弾薬箱を追加します。元の TaCZ JAR は変更しません。

## 対応環境

- Minecraft 1.21.1
- NeoForge 21.1 系（ビルド確認は 21.1.172）
- TaCZ NeoForge 1.21.1。参照・ビルド確認したファイルは `tacz-neoforge-1.21.1-1.1.8-hotfix-r7.jar`
- Java 21

## 追加アイテム

各箱は TaCZ の弾薬箱と同じく、弾薬種ごとの基礎スタック数に容量レベルを掛けて保持します。レベルはアイテムごとに固定です。

| アイテム | TaCZ容量レベル | 鉄の弾薬箱に対する容量 |
| --- | ---: | ---: |
| 銅の弾薬箱 | 1 | 2倍 |
| エメラルドの弾薬箱 | 3 | 4倍 |
| ネザライトの弾薬箱 | 4 | 5倍 |

TaCZ の既存レシピと同じ3×3配置です。上段中央に素材を置きます。

```text
PIP
P P
PPP
```

`I` は銅インゴット、エメラルド、またはネザライトインゴット、`P` は板材です。

## インストール

1. Minecraft 1.21.1 の NeoForge プロファイルを用意します。
2. TaCZ の対応JARと `tacz-ammo-tiers-1.21.1-1.0.0.jar` を `mods` フォルダーへ入れます。
3. ゲームを起動し、TaCZ の「弾薬」クリエイティブタブで追加アイテムを確認します。

## ソースからビルド

Java 21 と Gradle 8.10.2 が必要です。ビルド時に参照する TaCZ JAR の場所を指定します。

```powershell
.\gradlew.bat build -PtaczJar="C:\path\to\tacz-neoforge-1.21.1-1.1.8-hotfix-r7.jar"
```

成果物は `build/libs/` に出力されます。TaCZ 本体はコンパイル時の参照だけに使い、アドオンJARには同梱しません。
