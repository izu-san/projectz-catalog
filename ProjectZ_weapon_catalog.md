# Project Z 武器カタログ

対象: ローカル導入済みの **Project Z 3.1.2**（`Project Z 3.1.2/Config/items.xml`）。

- Project Z 独自の T4/T5 武器は **25 件**、バニラ武器を元にしたレア派生は **123 件**。さらに特殊武器・ロボット兵器を **4 件**追加する。
- レア派生は元武器の Tier を引き継ぎ、接尾辞ごとの固有効果を持つ別アイテム。下の「レア武器」表は、`元武器 + 接尾辞` の各組み合わせが 1 件ずつの実在アイテムを表す。
- 数値は XML の基本値。Project Z の T4/T5 武器はすべて Magnitude（ランダムロール）対象のため、実際の表示値は品質・ロール・Perk・MOD・弾薬で変わる。
- 射撃武器の「威力補正」は弾薬本体に加算される `EntityDamage`。ロケットは弾薬側の爆発ダメージに依存する。

## T4/T5 専用武器

### 遠隔武器

列: **Tier / 弾薬 / 射程 / RPM / 装弾数 / 威力補正 / 再装填 / 耐久(Q1→Q6)**

| 武器 | Tier | 弾薬 | 射程 | RPM | 装弾 | 威力補正 | 再装填 | 耐久 |
| --- | ---: | --- | ---: | ---: | ---: | ---: | ---: | --- |
| M60 マシンガン《改良版》 | T4 | 7.62 Ball / HP / AP / DU | 70 | 550 | 70 | +35 | 1.30 | 700→1250 |
| マシンガン ブルドッグ | T5 | .44 Ball / HP / AP / DU | 45 | 480 | 100 | +68 | 1.60 | 900→1500 |
| オートショットガン《改良版》 | T4 | Shell / Slug / Breaching / DU Slug | — | 110 | 24 | +14 | 1.40 | 800→1300 |
| オートショットガン イレーザー | T5 | Shell / Slug / Breaching / DU Slug | — | 150 | 40 | +17 | 1.80 | 900→1600 |
| スナイパーライフル《改良版》 | T4 | 7.62 Ball / HP / AP / DU | 100 | 210 | 18 | +70 | 1.00 | 800→1250 |
| スナイパーライフル ガウス | T5 | 7.62 HP / AP / DU | 120 | 120 | 12 | +170 | 1.20 | 800→1250 |
| ピストル ヘルガン | T5 | .44 Ball / HP / AP / DU | 45 | 150 | 12 | +28 | 1.50 | 850→1400 |
| SMG-5《改良版》 | T4 | 9mm Ball / HP / AP / DU | 40 | 500 | 56 | +18 | 1.40 | 700→1250 |
| SMG-5 ジンガー | T5 | 9mm HP / AP / DU | 40 | 600 | 88 | +28 | 1.80 | 900→1500 |
| ロケットランチャー《改良版》 | T4 | FS Rocket | 80 | 250 | 1 | 弾薬依存 | 2.00 | 100→200 |
| コンパウンドボウ《改良版》 | T4 | Stone / Iron / Steel AP / Flaming / Exploding Arrow | 60 | 90 | 1 | +80 | 2.50 | 500→1000 |
| コンパウンドクロスボウ《改良版》 | T4 | Stone / Iron / Steel AP / Flaming / Exploding Bolt | 70 | 120 | 2 | +35 | 1.20 | 500→1000 |
| クロスボウ カマキリ | T5 | Stone / Iron / Steel AP / Flaming / Exploding Bolt | 80 | 180 | 3 | +60 | 1.80 | 600→1200 |

補足: ガウスは Ball 弾を使用できない。ヘルガンには通常対象 +300／ボス +600 の追加 `EntityDamage` 条件効果がある。

### 近接武器

列: **Tier / 対エンティティ基礎値 / 対ブロック基礎値 / 耐久(Q1→Q6)**

| 武器 | Tier | 対エンティティ | 対ブロック | 耐久 | 備考 |
| --- | ---: | ---: | ---: | --- | --- |
| 鋼鉄の槍《改良版》 | T4 | 42 | 15 | 700→1250 | 槍系 |
| スピア コンビスティック | T5 | 62 | 80 | 900→1500 | 槍系 |
| スチールクラブ《改良版》 | T4 | 42 | 30 | 700→1250 | クラブ系 |
| アックス バーバリアン | T5 | 78 | 40 | 900→1500 | クラブ系 |
| スチールスレッジハンマー《改良版》 | T4 | 70 | 100 | 700→1250 | スレッジ系 |
| スレッジハンマー デストラクター | T5 | 104 | 96 | 900→1500 | スレッジ系、射程 2.8 |
| スチールナックル《改良版》 | T4 | 34 | 6 | 950→1750 | ナックル系 |
| ナックルズ マウスクロー | T5 | 65 | 16 | 600→1200 | ナックル系 |
| マチェーテ《改良版》 | T4 | 32 | 25 | 1200→2400 | 刃物系 |
| マチェーテ インディアナ | T5 | 44 | 20 | 1600→3200 | 刃物系 |
| スタンバトン《改良版》（Plasma Baton） | T4 | 28 | 12 | 600→1200 | バトン系 |
| スタンバトン《フルゲン》 | T5 | 54 | 12 | 900→1500 | バトン系。通常対象 +2500／ボス +5000 の追加ダメージ条件効果 |

## レア武器（123件）

同じ行の接尾辞をすべて付けたものが追加アイテム。例: `パイプライフル — Crusher / Knockdown / Fasthands` は 3 件である。英字接尾辞はコンソール・XML 検索用、括弧内はゲーム内の日本語表示。

### ライフル・ショットガン・マシンガン

| 系統 | 元武器 (Tier) | 接尾辞 |
| --- | --- | --- |
| ライフル | パイプライフル (T0) | Crusher（クラッシャー） / Knockdown（ノックダウン） / Fasthands（速い手） |
| ライフル | ハンティングライフル (T1) | Experienced（経験豊富） / Apple（アップル） / Fasthands（速い手） |
| ライフル | レバーアクションライフル (T2) | Universal（ユニバーサル） / Vampire（ヴァンパイア） / Unkillable（殺せない） |
| ライフル | スナイパーライフル (T3) | Crusher / Unkillable / Knockdown / Stable（安定） |
| ショットガン | パイプショットガン (T0) | Crusher / Experienced / Fasthands |
| ショットガン | ダブルバレルショットガン (T1) | Sweeper（スイーパー） / Unkillable / Fasthands |
| ショットガン | ポンプショットガン (T2) | Crusher / Experienced / Universal |
| ショットガン | オートショットガン (T3) | Crusher / Unkillable / Snowstorm（吹雪） / Universal |
| マシンガン | パイプマシンガン (T0) | Crusher / Universal / Unkillable |
| マシンガン | AK-47 (T1) | Crusher / Experienced / Unkillable |
| マシンガン | タクティカルアサルトライフル (T2) | Rapidfire（ラピッドファイア） / Apple / Experienced |
| マシンガン | M60 (T3) | Snowstorm / Universal / Unkillable / Stable |

### 弓・クロスボウ・ハンドガン

| 系統 | 元武器 (Tier) | 接尾辞 |
| --- | --- | --- |
| 弓 | プリミティブボウ (T0) | Robinhood（ロビン・フッド） / Ninja（忍者） / Vampire |
| 弓 | 木の弓 (T1) | Robinhood / Ninja / Vampire |
| クロスボウ | アイアンクロスボウ (T1) | Robinhood / Ninja / Vampire |
| 弓 | コンパウンドボウ (T3) | Robinhood / Ninja / Vampire |
| クロスボウ | コンパウンドクロスボウ (T3) | Robinhood / Ninja / Vampire |
| ハンドガン | パイプピストル (T0) | Experienced / Apple / Fasthands |
| ハンドガン | ピストル (T1) | Crusher / Unkillable / Universal |
| ハンドガン | .44 マグナム (T2) | Fasthands / Sweeper / Respect（リスペクト） |
| ハンドガン | SMG-5 (T3) | Snowstorm / Unkillable / Stable / Universal |
| ハンドガン | デザートバルチャー (T3) | Experienced / Universal / Knockdown / Vampire |

### 近接武器

| 系統 | 元武器 (Tier) | 接尾辞 |
| --- | --- | --- |
| 槍 | 石の槍 (T0) | Convenient（便利） / Experienced / Vampire |
| 槍 | 鉄の槍 (T1) | Experienced / Unkillable / Crusher |
| 槍 | 鋼鉄の槍 (T3) | Awl（錐） / Convenient / Universal |
| クラブ | 木製クラブ (T0) | Convenient / Crusher / Knockdown |
| クラブ | 野球バット (T1) | Experienced / Champion（チャンピオン） / Vampire |
| クラブ | スチールクラブ (T3) | Experienced / Universal / Unkillable |
| スレッジ | ストーンスレッジハンマー (T0) | Convenient / Crusher / Knockdown |
| スレッジ | 鉄のスレッジハンマー (T1) | Experienced / Unkillable / Universal |
| スレッジ | スチールスレッジハンマー (T3) | Champion / Convenient / Vampire |
| ナックル | レザーナックル (T0) | Stunner（スタナー） / Experienced / Universal |
| ナックル | アイアンナックル (T1) | Convenient / Unkillable / Crusher |
| ナックル | スチールナックル (T3) | Awl / Convenient / Experienced / Butcher（ブッチャー） |
| 刃物 | ボーンナイフ (T0) | Awl / Vampire / Universal |
| 刃物 | ハンティングナイフ (T1) | Butcher / Experienced / Crusher |
| 刃物 | マチェーテ (T3) | Convenient / Unkillable / Universal |
| バトン | パイプバトン (T0) | Convenient / Vampire / Stunner |
| バトン | スタンバトン (T2) | Convenient / Unkillable / Experienced |

## その他の追加・再編武器

| 武器 | 区分 | 内容 |
| --- | --- | --- |
| ガーデンナイフ | 近接・収穫 | 作物の収穫向け。戦闘用としては低威力。 |
| コンタクトグレネード《改良版》 | 投擲 | 接触式グレネードの改良版。 |
| リアクターハンマー | ロボット兵器 | 改良修理キットで修理するロボットハンマー。 |
| 自動タレット《改良版》 | ロボット兵器 | DU 弾対応。命中した敵を 30% 減速。 |
| スタンバトン (T2) | 再編 | Project Z がいったんバニラ定義を除去して独自定義で再追加する武器。新しい Tier ではないため、上の件数には含めない。 |

## 確認元

- 武器定義: `Project Z 3.1.2/Config/items.xml`
- 表示名: `Project Z 3.1.2/MultiLanguage/Localization.Eng.Japanese.csv`
