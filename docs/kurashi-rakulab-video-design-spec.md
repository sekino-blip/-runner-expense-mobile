# 暮らしラク研究所「ここ、NGが3つあります」動画設計書

> このファイルはClaude / チャッピー(ChatGPT) / コーデックス(Codex)が同じ文脈を共有するための共通ドキュメントです。
> 更新時は必ずユーザーの確認を取った上で反映します。

最終更新日: 2026-09-11
関連文書: `docs/kurashi-rakulab-machigai-sagashi-plan.md`(企画書)
対象: Instagram `kurashi_rakulab` / 間違い探しシリーズ
ステータス: **ドラフト / 未承認**

**記載の区分**: `【事実】` 確認済み / `【推測】` 未検証 / `【提案】` 要承認

---

## 0. 制作分担(4者)

`【事実】` 2026-09-11時点で確認した、各者の実行可能範囲に基づく分担。
**役割は「得意だから」ではなく「実行できるから」で決めている。** 根拠は0-4に記載。

### 0-1. 成果物ごとの担当

| 成果物 | 担当 | 引き渡し先 |
|---|---|---|
| ネタ選定(企画書8章・8-2章の骨子をベースに具体化) | **チャッピー**(**コーデックス経由**、2026-09-11〜) | コーデックス→Claude |
| **テロップ文言の原稿**(見出し・解答3つ・CTA) | **チャッピー**(コーデックス経由) | コーデックス→Claude |
| **キャプション本文・ハッシュタグ** | **チャッピー**(コーデックス経由) | コーデックス→Claude |
| **一次情報の裏取り・出典URLの収集** | **チャッピー**(コーデックス経由) | コーデックス→Claude |
| **チャッピーへの指示出し・受け取り・差し戻し**(0-0-1参照) | **コーデックス**(2026-09-11〜。従来はClaudeが担当) | Claude |
| 企画書・動画設計書の作成と維持 | **Claude** | コーデックス(経由でチャッピーにも共有) |
| 文言の禁止事項チェック、設計書への反映 | **Claude** | コーデックス |
| 一枚絵の要素設計(NG3箇所・ダミー配置) | **Claude** | コーデックス |
| **HyperFrames の compose / render 実行** | **コーデックス** | Claude |
| **出力仕様の検証**(尺・解像度・fps) | **コーデックス** | Claude |
| 納品チェックリストの記入 | **コーデックス** | Claude |
| 動画ファイルの受け渡し(Dropbox等) | **コーデックス** | Claude |
| 生成物の設計適合レビュー | **Claude** | 関野 |
| **Metricool 予約投稿** | **Claude** | — |
| 週次の数値計測・レポート | **Claude** | 関野 |
| **公開可否の最終承認** | **関野洋平** | — |

### 0-2. 各者の役割要約

| 担当 | 役割 |
|---|---|
| **チャッピー(ChatGPT)** | **言葉と事実の担当。** ネタ出し、日本語コピーの作成と推敲、キャプション、そして**外部の一次情報にあたって出典を取る**役割 |
| **コーデックス(Codex)** | **実行と仕様順守の担当、および窓口(2026-09-11〜)。** 動画生成・出力検証に加え、**チャッピーへの指示出しと受け取りを担当**。Claudeから受け取ったルールをそのままチャッピーに伝達し、成果物をClaudeに引き渡す |
| **Claude** | **設計とレビューの担当。** 設計書の作成と維持、禁止事項・整合性のチェック、Metricoolの数値検証と予約投稿 |
| **関野洋平** | **承認。** 事業方針、公開可否、仕様変更の最終判断 |

### 0-2-1. 連携フローの変更(2026-09-11): コーデックスを窓口に

`【事実】` これまではClaudeがチャッピーとコーデックスにそれぞれ個別の指示文を作成していたが、
2026-09-11以降、**コーデックスがチャッピーとの窓口を担当する**ことに変更した。

**新フロー**

1. Claudeが、シーンの骨子(企画書8章・8-2章)とルール一式(5章の許容形式、6章の禁止事項、
   8章の表現ルール)を**まとめてコーデックスに渡す**
2. **コーデックスがその内容をチャッピーに転送し**、テロップ・キャプション・裏取り結果を受け取る
   (0-5のHANDOFFフォーマットはそのまま使用。送信元がClaudeからコーデックスに変わるのみ)
3. コーデックスは、チャッピーの回答を**そのままClaudeに引き渡す**(内容を要約・改変しない)
4. **Claudeによる最終チェック(禁止事項・事実主張の許容形式・設計書への確定反映)は従来どおり
   実施する。** 窓口の変更は伝達経路の効率化であり、Claudeのレビュー工程を省略するものではない
5. Claudeが確定させた内容をもとに、コーデックスが動画を制作・納品する(以降は従来どおり)

**変わらないこと**
- チャッピーの禁止事項(出典の無い主張を書かない等)は不変
- コーデックスの禁止事項(文言を自分で作らない等)も不変。**チャッピーへの指示を伝達する際、
  ルールを省略・改変しないことが新たな禁止事項として加わる(0-3参照)**
- Claudeの最終レビュー・Metricool予約投稿の役割は不変

---

### 0-3. 各者の「やってはいけないこと」

**この事故は、動画生成側が自分でクイズ文言を書いたために起きました**(7章参照)。
同じ経路を塞ぐため、以下を厳守します。

**コーデックス**
- **設計書に書かれていない文言を、自分で作らない。** テロップ・キャプションは
  チャッピーが書き、Claudeが設計書に確定させたものだけを使う
- 尺・解像度・fps・カット割りを勝手に変更しない。変更が必要ならClaudeに差し戻す
- 事実主張(データ・調査・数値)を自分で追加しない
- **(2026-09-11〜)窓口としてチャッピーに指示を伝達する際、Claudeが定めたルール
  (2択・答えを問題文に含めない・形式A/B・禁止語等)を省略・簡略化・改変しない。
  チャッピーの回答もClaudeへそのまま引き渡し、内容を要約・改変しない**

**チャッピー**
- **動画生成を実行しない。** compose / render はコーデックスの担当と重複させない
- **確認できていない出典・URL・調査名を書かない。** 裏が取れないネタは「不採用」として返す
- 設計書の秒数・px仕様を自分で書き換えない。提案はClaudeに投げる

**Claude**
- **動画を生成しない**(構造的にできない。0-4参照)
- 完成動画を目視できないまま予約投稿しない
- 関野さんの承認なしに、投稿・予約・有料枠の消費を行わない

### 0-4. この分担になっている根拠(すべて実測)

| # | 事実 | 帰結 |
|---|---|---|
| 1 | HyperFrames MCPの仕様上、Claude CodeのようなCLIクライアントからは `compose` と `render_video` が**無効化**されている | **動画生成はコーデックスが担当するほかない** |
| 2 | Claudeの実行環境から `files2.heygen.ai` / `static.metricool.com` への直接アクセスが組織プロキシに拒否される(CONNECT 403)。ffprobe等の動画解析ツールも無い | **Claudeは完成動画を目視・解析できない。**納品時の文字起こしと絵コンテが必須 |
| 3 | 同じ制約により、Claudeは外部サイトの一次情報にアクセスできない | **出典の裏取りはチャッピーが担当する** |
| 4 | ClaudeはMetricool MCPで読み書きができ、実測値を取得済み | **数値検証と予約投稿はClaudeが担当する** |
| 5 | 2026-09-11、**コーデックスの実行環境ではHyperFramesの`compose`が利用できないことが判明**(「このCodexでは」という限定付きの報告。恒久的制約か本環境固有かは未確認)。一方でHiggsfield(Higgsedit)・FFmpeg・ffprobeは利用可能と確認された | **制作ツールをHyperFramesからHiggsfield(Higgsedit)+FFmpegへ変更する。0-6参照** |

### 0-5. 引き継ぎ(HANDOFF)フォーマット

**チャッピー → Claude**(文言の納品)

```
シーン番号: #N (部屋名)
見出し: (2行以内)
NG①(易): 名称 / 解答テロップ(2行以内)
NG②(易): 名称 / 解答テロップ(2行以内)
NG③(難): 名称 / 解答テロップ(2行以内) / 難である理由
CTA: (1行)
キャプション: (企画書9章の8ブロック構造で全文)
事実主張の有無: 有 / 無
 → 有の場合、主張ごとに出典URLと発行元を列挙
禁止事項の自己チェック: 衛生・細菌・健康・食品安全の語 → 無 / 金額・削減率 → 無
```

**コーデックス → Claude**(動画の納品)

```
プロジェクトID:
動画URL / ファイル受け渡し先:
総尺: N.NNN秒 (設計値との差分: ±N.NNN秒)
解像度 / fps:
全テロップの文字起こし: (カットごとに全文)
一枚絵の要素リスト: NG3箇所 / ダミー要素を区別して列挙
絵コンテ画像 or サムネイル: (添付)
11章チェックリスト: 全項目の結果
設計書から逸脱した点: (あれば理由とともに。無ければ「無し」)
```

---

### 0-6. 制作ツールの変更(2026-09-11)

`【事実】` コーデックスの実行環境ではHyperFramesが使えないため、**Higgsfield(Higgsedit)+FFmpegで制作する。**
文言・尺・解像度・fps・カット割りなど、**確定済みの内容は一切変わらない。変わるのは実装ツールのみ。**

| 項目 | 変更前(HyperFrames) | 変更後(Higgsedit + FFmpeg) |
|---|---|---|
| 一枚絵・テロップの生成 | `compose`(自然言語プロンプト) | Higgseditでの直接制作 |
| ビジュアルの一貫性 | `claude` built-in style(自動) | **手動での色合わせが必要**(0-6-1) |
| 出力検証 | Claudeが目視できず(CDN 403) | **コーデックス側でffprobeによる検証が可能** |
| 9章・10章のHyperFrames用プロンプト | (このツールでは使用不可) | **参考として保持**。他環境で使う場合に備える |

**この変更に伴い、9章に「Higgsedit/FFmpeg版 制作パラメータ」を新設する(9-0章)。**
内容はツールに依存しないパラメータ(色・座標・フレーム番号・SFXタイミング)のみで記述し、
コーデックスが自身の実装(Higgseditのコード・FFmpegのフィルタグラフ等)に落とし込む。

### 0-6-1. 色の確定(未解決・要対応)

`【事実】` 深緑・テラコッタの正確なカラーコードは、動画設計書2章で当初から
「未確定・カラーピック要」としていた課題。HyperFramesの`claude` built-in styleは
これを自動で吸収していた可能性があるが、**Higgseditでは先送りできない。**

`【事実】` Claudeは既存動画のCDN(`static.metricool.com`)にアクセスできず(CONNECT 403)、
色を抽出できない。**コーデックス側にffmpeg/ffprobeがあるため、この作業はコーデックスが担当する。**

**依頼内容(下記「コーデックスへ返す指示」参照)**: 既存の投稿済み2本
からffmpegでフレームを抽出し、背景色・見出し(深緑)・バッジ(テラコッタ)の
HEX値をピクセルサンプリングして報告する。
**この値が確定するまで、9-0章の色指定は`【推測】`のプレースホルダーとする。**

**既存2本のMP4 URL**(2026-09-11、Metricool MCP `getScheduledPosts` で取得。詳細は企画書9-2章)

| # | 投稿日 | MP4 URL |
|---|---|---|
| 1 | 2026-09-08 20:00 | `https://static.metricool.com/video/5293012/202609/eb62560da29b4299.mp4` |
| 2 | 2026-09-09 20:00 | `https://static.metricool.com/video/5293012/202609/fe13c6ea94e144b5.mp4` |

`【事実】` Claudeはこれらへ直接アクセスできず(CONNECT 403)、署名・有効期限は未検証。

## 1. 出力仕様

| 項目 | 値 |
|---|---|
| 解像度 | 1080 × 1920 |
| アスペクト比 | 9:16(縦型) |
| フレームレート | 30fps |
| **尺** | **15.000秒**(標準版) / 12.000秒(A/B検証用の短尺版。7章参照) |
| 形式 | MP4 / H.264 |
| 音声 | 効果音のみ。**ナレーション・音声合成は使用しない** |
| BGM | **なし(2026-09-11承認)**。効果音のみで統一 |

### 安全領域(テロップ配置禁止エリア)

| 領域 | px | 理由 |
|---|---|---|
| 上部 | 0 〜 220 | Instagramのヘッダー・アカウント表示 |
| 下部 | 1536 〜 1920(下20%) | キャプション・音源表示・親指 |
| 右端 | 918 〜 1080(右15%) | いいね・コメント・シェアボタン |

**主要テロップは y = 300 〜 1450、x = 80 〜 900 の範囲に収める。**

---

## 2. ビジュアル仕様

既存投稿のテイストを維持する。HyperFramesでは **`claude` built-in style** を指定し、
既存動画との一貫性を確保する。

| 要素 | 仕様 |
|---|---|
| 背景 | クリーム `#F0E9DC` `【事実】`既存動画の生成指示に記載された値 |
| 見出し文字 | 深緑(deep forest green) **`【推測】`具体値は未確定。既存動画からのカラーピック要** |
| トピックバッジ | テラコッタオレンジ、角丸 **`【推測】`具体値は未確定。同上** |
| 背景テクスチャ | 紙片(paper-square)を控えめに散らす |
| イラスト | フラットな線画。**線は深緑1色**、面の着色は最小限 |
| 解答マーカー | テラコッタオレンジの円。**線のみ・塗りつぶしなし**(下の絵を隠さないため) |
| トーン | 静かで丁寧な編集トーン |

**色の指定について**: 深緑とテラコッタの正確な値は未確定です。Codex側で既存動画から
カラーピックするか、`claude` built-in style に委ねてください。**推測値を確定値として
設計書に書き込まないでください。**

---

## 3. カット割り(標準版 15.000秒 / 450フレーム)

| カット | 時間 | フレーム | 内容 |
|---|---|---|---|
| **C1** | 0.00-2.00 | 0-59 | 問題提示 |
| **C2** | 2.00-9.00 | 60-269 | 探す時間(7秒) |
| **C3** | 9.00-10.00 | 270-299 | 答え合わせ宣言 |
| **C4** | 10.00-14.00 | 300-419 | 解答3箇所 |
| **C5** | 14.00-15.00 | 420-449 | CTA + ループ |

### C1 問題提示(0.00-2.00)

| 要素 | 配置 | 内容 |
|---|---|---|
| シリーズラベル | y≈300、小 | `暮らしの間違い探し / 01` |
| トピックバッジ | y≈380、テラコッタ角丸 | `玄関` |
| 見出し | y≈520、極太・深緑 | `ここ、` / `NGが3つあります` (2行) **全シーン固定。1文字も変えない** |
| 一枚絵 | y≈900-1450 | **0.30秒から opacity 0.25 でフェードイン → 2.00秒で 1.0** |

- **要件: 1.0秒時点で一枚絵が視認できる状態にする。**冒頭に絵が無いと離脱する
- 効果音: 0.00 に軽いポン音1回

### C2 探す時間(2.00-9.00) ← 本企画の中核

| 要素 | 配置 | 内容 |
|---|---|---|
| 一枚絵 | 画面中央、フル表示 | **完全静止** |
| 小見出し | y≈330 | `NGは3つ` |
| 残り時間バー | y≈1450、高さ8px | テラコッタ。7.0秒かけて右→左に減少 |

**厳守事項**
- **一枚絵を一切動かさない。** ズーム、パン、パララックス、揺れ、要素のアニメーションすべて禁止
- **数字のカウントダウンを使わない**(視線を奪い、絵から目が離れる)
- **ヒント・マーカー・チェックマークを出さない**(答えバレ)
- 効果音: このカット中は無音、または極めて controlled な秒針音のみ

`【推測】` 7秒の静止提示は本企画の中核仮説であり、最大のリスクでもある。7章のA/Bで検証する。

### C3 答え合わせ宣言(9.00-10.00)

- 一枚絵の上にクリーム色のオーバーレイ(opacity 0.85)
- 中央 y≈960 に深緑で `答え合わせ`
- 効果音: 柔らかいチャイム1回
- **1.0秒ちょうど。これ以上伸ばさない**

### C4 解答(10.00-14.00 / 各1.333秒)

オーバーレイを外し一枚絵に戻る。**丸は消さずに累積表示**していく。

| # | 時間 | 内容 | 一言テロップ(y≈1400) |
|---|---|---|---|
| ① 易 | 10.00-11.33 | NG①の位置に円を描画 | (8章のシーン別表を参照) |
| ② 易 | 11.33-12.67 | NG②の位置に円を描画 | 同上 |
| ③ 難 | 12.67-14.00 | NG③の位置に円を描画 | 同上 |

- **順序は必ず 易 → 易 → 難**。最後に驚きを置く
- 円は0.25秒で描き込むアニメーション(線が回って閉じる)
- 効果音: ①②は同じポン音、③のみ音程を上げる/強める
- 一言テロップは各カット開始から0.1秒遅れて表示、次のカットで差し替え

### C5 CTA + ループ(14.00-15.00)

- 一枚絵(円3つ付いた状態)をそのまま維持
- y≈1400 にテロップ `いくつ分かった? コメントで`
- **14.70秒からC1のレイアウトへクロスフェード開始 → 15.00で完全にC1の絵柄に一致させる**
- **締めカード(深緑の角丸カード+保存アイコン)は使用しない** ← 企画書 A-1、**2026-09-11承認済み**

`【事実】` A-1は承認済み。旧・代替案(締めカードを14.0-14.7秒に短縮する案)は不要になった。
**全シーン、締めカードなし・14.70秒からのクロスフェードで統一して制作する。**

---

## 4. 一枚絵(イラスト)の設計ルール

全シーン共通。**これが本企画の成否を決めます。**

### 構図
- 線画、線は深緑1色。面の着色は最小限(クリーム系の薄い面のみ)
- 対象空間を**正面またはやや斜め**から。俯瞰・魚眼は使わない
- 絵の占有範囲は **y = 850 〜 1460**(安全領域の内側)

### NG3箇所の配置ルール
1. **3箇所は画面内で必ず離して配置する**(1箇所に固まると同時に見つかる)
2. **NG③(難)は画面の上部または端に置く** `【推測】`視線は中央→下に流れやすいため
3. NG①②(易)は中央〜下部の視認しやすい位置に置く
4. 3箇所とも、円マーカー(直径約160px)を重ねても他のNGと重ならない間隔を空ける

### ダミー要素
- NG以外の小物を **5〜8個** 配置する(観葉植物、鍵フック、カレンダー、スリッパ等)
- **ダミーはすべて「正常な状態」で描く。**紛らわしくするために半端に乱さない
- ダミーが多すぎると探索が総当たりになり、7秒で終わらない。上限8個を守る

### 難易度設計
- **易2つ + 難1つ**に固定。増減しない
- 「難」の定義は2種類あり、どちらでもよい
  - (a) **見つけにくい**: 小さい、端にある
  - (b) **NGだと認識されにくい**: 見えているが問題だと思われていない
- `【推測】` 想定正答率は 易70%以上 / 難30%以下。**「3つ全部分かった」が少数派になる状態が理想**

---

## 5. テキスト原稿ルール

| ルール | 内容 |
|---|---|
| **決め台詞の固定** | 見出しは **`ここ、` / `NGが3つあります`** で全シーン固定。**1文字も変えない。**「この部屋」「この玄関」等に置き換えない(14本中大半が「部屋」ではないため)。場所はトピックバッジで示す |
| 断定の禁止 | 「〇〇はNG」と書かない。「〇〇だと、こうなりやすい」 |
| **解答テロップの許容形式**(**確定**。#1玄関で実運用検証済み) | 出典が必要な主張は禁止。以下のいずれかのみ使用可。<br>**形式A(観察の言い換え)**: 一枚絵に描かれた状態をそのまま言葉にしたもの。例:「たたきの靴、散らばっていませんか」<br>**形式B(自明な帰結)**: 外部データを介さず、絵の状態から直接論理的に導ける帰結のみ<br>**禁止**: 具体的な数値基準(「1人1足」等)、「〜という調査」「〜と言われている」等の外部権威への言及、統計的傾向の断定 |
| 1テロップ | 最大2行 / 1行あたり全角16文字以内 |
| 敬体 | 既存投稿と同じ、静かで丁寧なトーン。煽り表現・強い断定を使わない |
| 数字 | 具体的な金額・時間・削減率を書かない(一次情報が必要になるため) |

---

## 6. 禁止事項(厳守)

**以下に1つでも該当したら、そのカットは作り直しです。**

1. **健康・衛生・細菌・食品安全に関する記述**(「雑菌」「菌」「除菌」「清潔」等の語を含む)
2. **節約金額・電気代・省エネ効果の数値**
3. **特定メーカー・商品名・ロゴの描画、および商品の否定**
4. 人物の描画(本シリーズは空間のみ)
5. 探す時間中のヒント・マーカー・チェックマークの表示
6. 一枚絵のアニメーション(ズーム・パン・揺れ等)
7. ナレーション・音声合成の使用
8. 問題文の中に答えを書くこと ← **7章の事故事例を参照**
9. 出典が必要な事実主張(出典を画面に出せないなら、そのネタを使わない)

---

## 7. 事故事例(再発防止 / 必読)

`【事実】` 2026-09-11 14:48 に HyperFrames で生成された
プロジェクト `e6c1a534-1241-408e-82de-c11891e1bcae`(「暮らしの豆知識帳 / 01」)には、
以下の欠陥がありました。**公開していません。**

| # | 欠陥 | 重大度 |
|---|---|---|
| 1 | 問題文「**台所のスポンジ**、実は一番汚いのは?」に対し、選択肢が A)トイレの便座 **B)台所のスポンジ** C)玄関マット、正解B。**問題文の中に答えが書かれており、クイズとして成立していない** | High |
| 2 | 「便座より雑菌が多い」「菌を増やさないために」と、衛生・細菌の主張を含む(本設計書6-1に抵触) | High |
| 3 | NSF International の調査に基づくとされるが、**画面にも制作メモにも出典が無い** | Medium |
| 4 | 完全なAI生成だが、既存運用の `isAiGenerated: false` をそのまま踏襲してよいか未検証 | Medium |

**再発防止として、9章の納品チェックリストで #1〜#3 を必ず確認すること。**

---

## 8. A/Bテスト仕様(T-1)

**1回に1変数のみ**を切り替える。T-1が確定するまで他の変数を触らない。

| | A(標準) | B(短尺) |
|---|---|---|
| 総尺 | 15.000秒 | 12.000秒 |
| C1 問題提示 | 0.00-2.00 | 0.00-2.00 |
| **C2 探す時間** | **2.00-9.00(7秒)** | **2.00-6.00(4秒)** |
| C3 答え合わせ | 9.00-10.00 | 6.00-7.00 |
| C4 解答 | 10.00-14.00 | 7.00-11.00 |
| C5 CTA | 14.00-15.00 | 11.00-12.00 |

**判定指標**: ループ率(表示 ÷ リーチ)とコメント数。各4本ずつ制作。
**変えてよいのはC2の長さと総尺だけ。** テロップ文言・イラスト・音・色は完全に同一にする。

---

## 9. シーン別 制作指示(#1 玄関 / 初回分)

企画書8章の14本のうち、**まず #1 のみ制作する。** 承認後に残りへ展開する。

### 9-0. Higgsedit / FFmpeg 版 制作パラメータ(ツール非依存)

`【事実】` 制作ツールをHyperFramesからHiggsfield(Higgsedit)+FFmpegに変更(0-6参照)。
以下はツールの構文に依存しないパラメータ一覧。コーデックスはこれを自身の実装
(Higgseditのコード・FFmpegのフィルタグラフ等)に落とし込む。**値は3章・4章・5章と同一。**

**出力**

| 項目 | 値 |
|---|---|
| 解像度 | 1080 × 1920 |
| fps | 30 |
| 総フレーム数 | 450(15.000秒ちょうど) |
| コーデック | H.264 / MP4 |
| 音声 | 効果音のみ。ナレーション・音声合成は使用しない |

**色**(`【事実】` **確定。コーデックスが9/9投稿からffmpegで抽出したピクセル値**)

| 要素 | 確定値 | 出典 |
|---|---|---|
| 背景 | クリーム `#F6F1E5` | 9/9投稿(`fe13c6ea94e144b5.mp4`)からのピクセルサンプリング |
| 見出し(深緑) | `#24473E` | 同上 |
| バッジ(テラコッタ) | `#E0785E` | 同上 |
| 解答マーカーの円 | `#E0785E`(バッジと同色)、線のみ・塗りつぶし無し | 同上 |

**注記**: `【事実】` 9/8投稿との照合完了(コーデックスがffmpegで3.000秒時点のフレームから
最頻色を採取)。

| 要素 | 9/8 | 9/9(採用) | 座標(9/8 / 9/9、元画像1080×1920) |
|---|---|---|---|
| 背景クリーム | `#F7F1E5` | `#F6F1E5` | (400,100) / (400,100) |
| 見出し深緑 | `#254740` | `#24473E` | (692,576) / (519,597) |
| テラコッタ | `#DD765E` | `#E0785E` | (416,444) / (458,445) |

RGB各成分の差は最大3。圧縮・生成ごとの揺れの範囲内と考えられ、**9/9の採用値は維持する。**

**解決済み**: 2026-09-11、#1玄関の納品時にコーデックスがPNG内部ピクセルで確認。
バッジは実際に**テラコッタの塗りつぶし角丸形状**で、クリーム色の文字(部屋名)が乗る構成と判明。
`#E0785E`は塗りつぶし本体の値であり、既存動画側の採取値(テキストからの採取)とは対象が異なる点に
注意が必要だが、両者とも同系統のテラコッタであり実務上の問題はない。

**フレーム単位のカット割り**(3章の秒数を450フレーム基準に変換。fps=30)

| カット | フレーム範囲 | 秒 |
|---|---|---|
| C1 問題提示 | 0-59 | 0.00-2.00 |
| 　└ 一枚絵フェードイン開始 | 9フレーム目(0.30秒) | opacity 0.25→1.0まで50フレームかけて |
| C2 探す時間(完全静止) | 60-269 | 2.00-9.00 |
| 　└ 残り時間バー | 60-269の210フレームで右→左に減少 | |
| C3 答え合わせ | 270-299 | 9.00-10.00 |
| 　└ クリームオーバーレイ opacity 0.85 | | |
| C4 解答(円は累積・消さない) | 300-419 | 10.00-14.00 |
| 　└ ①円+テロップ | 300-339(0.25秒で描画) | 10.00-11.33 |
| 　└ ②円+テロップ | 340-379 | 11.33-12.67 |
| 　└ ③円+テロップ | 380-419 | 12.67-14.00 |
| C5 CTA+ループ | 420-449 | 14.00-15.00 |
| 　└ 冒頭フレームへのクロスフェード開始 | 441フレーム目(14.70秒) | 449フレーム目(15.00秒)で完了 |

**厳守事項(ツールが変わっても不変)**
- C2(60-269フレーム)は一枚絵を1ピクセルも動かさない。ズーム・パン・パララックス禁止
- ヒント・マーカー・チェックマークをC2中に表示しない
- 数字のカウントダウンを使わない(バーのみ)
- 解答順は 易→易→難 固定。円は累積表示(前の円を消さない)
- 締めカードは使用しない(A-1確定仕様)。C5は冒頭フレームへのクロスフェードのみ
- テロップは y=300〜1450 / x=80〜900 の内側

**#1玄関の内容(NG配置・テロップ)は下記9-1章、および直後の「#1玄関 確定版プロンプト」を参照。**
プロンプトはHyperFrames構文だが、**記述されている内容(構図・配置・テロップ・タイミング)は
ツールに依存しないため、Higgsedit実装時の仕様としてそのまま読み替えて使用できる。**

---

### 9-1. #1 玄関

| 項目 | 内容 |
|---|---|
| トピックバッジ | `玄関` |
| シリーズラベル | `暮らしの間違い探し / 01` |
| 見出し | `ここ、` / `NGが3つあります` |

**一枚絵に描くもの**

| 要素 | 位置 | 種別 |
|---|---|---|
| たたきに散らばった靴6足 | **下部中央** | **NG①(易)** |
| 傘立て、壊れた傘が混在(骨が折れている) | **左下** | **NG②(易)** |
| 靴箱の上に積まれた郵便物・チラシの束 | **上部やや右**(小さめに) | **NG③(難)** |
| 靴箱本体 | 上部〜中央 | ダミー(正常) |
| 鍵フック(鍵が掛かっている) | 右上 | ダミー(正常) |
| 観葉植物 | 右下 | ダミー(正常) |
| スリッパ2足(揃っている) | 中央やや右 | ダミー(正常) |
| 姿見 | 左中央 | ダミー(正常) |
| ドア | 中央奥 | ダミー(正常) |

**解答テロップ(C4)** ← **確定(チャッピー納品版。形式Aのみで構成、出典不要)**

| # | 時間 | テロップ |
|---|---|---|
| ① | 10.00-11.33 | `たたきの靴、` / `散らばっていませんか` |
| ② | 11.33-12.67 | `傘立てに、壊れた傘が` / `混ざっていませんか` |
| ③ | 12.67-14.00 | `靴箱の上、郵便物やチラシが` / `積み重なっていませんか` |

**③が「難」である理由**: 設計上、上部やや右に小さく配置するため。見つけにくくなるという**推測**であり、
実際の難易度(視聴者による検証)は未実施 `【推測】`。

**CTA(確定)**: `いくつ分かった? コメントで`

**キャプション(確定)**

```
ここ、NGが3つあります👀

今回のテーマは「玄関」。
片付けの視点で探す、暮らしの間違い探しです。

① たたきに散らばった靴
② 傘立てに混ざった壊れた傘
③ 靴箱の上に積み重なった郵便物・チラシ

まずは玄関の靴を、置き場所に戻すところから。

いくつ分かった?コメントで

暮らしラク研究所｜@kurashi_rakulab
毎日の「ちょっと面倒」を、少しラクに。

※イラストは収納のイメージ図です。

#間違い探し #収納アイデア #片付け #暮らしの工夫 #暮らしラク研究所
```

**事実主張**: 無(形式Aのみ。外部の裏付けが必要な主張は含まれない)

---

### #1 玄関 確定版プロンプト(コーデックスにそのまま渡す)

10章の雛形に、上記の確定内容を差し込み済みのものを以下に示す。**このままコピーしてコーデックスに渡せる。**

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.

VISUAL STYLE — match the brand's existing videos exactly. Use the `claude`
built-in style for consistency.
- Warm cream background (#F0E9DC)
- Deep forest green headline text (pick the exact green from the brand's
  existing videos; do not invent a new green)
- Terracotta orange rounded topic badge (same — pick from existing videos)
- Subtle scattered paper-square background texture
- Calm flat line-art illustration, drawn with deep green strokes only,
  minimal fill
- Quiet editorial tone. NO spoken narration, NO voice synthesis.
  On-screen text + sound effects only.

SAFE AREAS — keep all text within y=300..1450 and x=80..900.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
Setting: a genkan (Japanese entryway), viewed from a front / slightly angled view.
- NG1 (easy): 6 pairs of shoes scattered on the concrete floor (たたき),
  positioned bottom-center.
- NG2 (easy): an umbrella stand at bottom-left, mixing normal umbrellas with
  one visibly broken umbrella (bent rib).
- NG3 (hard): a stack of mail and flyers piled on top of the shoe cabinet,
  positioned upper-right, drawn small.
- Dummy items, all drawn in a NORMAL tidy state (do not make them ambiguous):
  shoe cabinet body (upper-center), a key hook with keys hanging (upper-right),
  a potted plant (bottom-right), 2 pairs of slippers neatly aligned
  (center-right), a standing mirror (center-left), a door (center-back).
Keep NG1/NG2/NG3 spaced apart from each other and from dummy items so their
160px-diameter answer circles won't overlap anything else.

TIMELINE:
[0.00-2.00] Series label "暮らしの間違い探し / 01" small at top.
  Terracotta badge "玄関". Bold deep-green headline
  "ここ、" / "NGが3つあります".
  The illustration fades in from opacity 0.25 at 0.30s to 1.0 at 2.00s —
  it MUST be clearly visible by 1.0s.
  SFX: one soft pop at 0.00.

[2.00-9.00] SEARCH TIME. Show the illustration full, COMPLETELY STATIC.
  No zoom, no pan, no parallax, no element animation whatsoever.
  Small label "NGは3つ" at y=330.
  A thin terracotta progress bar at y=1450 depletes right-to-left over 7.0s.
  Do NOT show numbers counting down. Do NOT show any hint or marker.
  SFX: silence.

[9.00-10.00] Cream overlay at 0.85 opacity over the illustration.
  Centered deep-green text "答え合わせ". SFX: one soft chime. Exactly 1.0s.

[10.00-14.00] Remove the overlay. Reveal the three NGs in this exact order,
  drawing an OUTLINE-ONLY terracotta circle (no fill, ~160px diameter) at
  each location. Circles ACCUMULATE — do not erase previous ones.
  Each circle draws in over 0.25s.
  [10.00-11.33] circle on the scattered shoes (NG1) + caption at y=1400:
    "たたきの靴、" / "散らばっていませんか"
  [11.33-12.67] circle on the broken umbrella (NG2) + caption:
    "傘立てに、壊れた傘が" / "混ざっていませんか"
  [12.67-14.00] circle on the mail stack (NG3) + caption:
    "靴箱の上、郵便物やチラシが" / "積み重なっていませんか"
  SFX: same pop for the first two; a higher/stronger pop for the third.

[14.00-15.00] Keep the illustration with all three circles.
  Caption at y=1400: "いくつ分かった? コメントで".
  From 14.70 to 15.00, cross-fade back into the exact 0.00 frame layout so
  the video loops seamlessly. Do NOT use a closing end-card (confirmed spec —
  no bookmark/save card in this series).

HARD CONSTRAINTS:
- Never mention bacteria, germs, hygiene, disinfection, or food safety.
- Never state money amounts, electricity costs, or savings percentages.
- No brand names, product names, logos, or people.
- Never put the answer inside the question text.
- Use only the exact caption text given above — do not paraphrase or add
  reasoning/statistics of your own.
```

---

### #1 玄関 納品記録(2026-09-11)

`【事実】` コーデックスから納品。プロジェクトID `genkan01-realism`。

| 項目 | 結果 |
|---|---|
| 総尺 | 15.000秒(設計値との差分 0.000秒)。ffprobe実測 |
| 解像度/fps/フレーム数 | 1080×1920 / 30fps / 450フレーム / H.264 / yuv420p |
| ファイルサイズ | 28,087,921バイト(約26.8MB) |
| 音声 | AAC LC 48kHz mono。音声ストリーム尺14.933秒(映像より0.067秒短い。エンコーダ特性によるものと推定) |
| 設計書11章チェックリスト | 16項目中、全項目「合格」または「記載済み」。項目15(ナレーションなし)のみ「全編の聴取確認は未実施」との留保付き |
| バッジ色 | **解決**。PNG内部ピクセルで`#E0785E`を確認。塗りつぶしバッジ本体の色であり、テキストの色ではないと判明(9-0章の留保を解消) |
| 費用 | 実行前後とも119.37クレジットで差分0.00。**Claudeが同日中に`balance`/`transactions`で独立に再確認し、新規取引が無いことも確認済み**(状況証拠として企画書A-4参照) |
| 受け渡し状況 | Higgsfield外部ストレージ(CloudFront)に保存済み。SNS投稿は未実施 |

**コーデックスが自己申告した逸脱・未検証事項**

| # | 内容 | 重大度 | Claudeの評価 |
|---|---|---|---|
| 1 | NG③(郵便物)の解答円の下端が、靴箱上端の一部と重なる | Low | 郵便物は靴箱の上に置かれた設定であり、構図上自然な重なり。修正不要と判断 |
| 2 | 9秒直前にAAC由来の音の前にじみ(最大約-65dBFS) | Low | 非常に小さく、実際の再生で知覚される可能性は低いと考えられる。修正不要と判断 |
| 3 | 静止画領域の圧縮劣化を避けるため、H.264ロスレス設定(profile表示: High 4:4:4 Predictive相当)を採用 | **Medium** | **投稿先(Instagram)・再生端末での互換性が未検証。次工程で必ず確認すること(下記)** |
| 4 | 全編の再生・聴取確認は未実施 | — | Claudeも実ファイルにアクセスできず(CONNECT拒否)、同様に未検証。工程9で解消する |

**次工程への申し送り(工程9: 実機確認。企画書10-1参照)**

`【提案】` 上記#3により、通常のMetricool予約投稿(工程11)に進む前に、**関野さんによる実機(iPhone)での
再生確認を必須のゲートとする。** 音声を含めた通し再生ができるかを最優先で確認する。可能であれば
Metricoolへの下書き登録で、Instagram側が受理するかも合わせて確認する。ここで問題が出た場合は、
標準的な(非ロスレスの)エンコード設定での再出力をコーデックスに依頼する。

---

### 9-2. #2 シンク下

`【事実】` 2026-09-11、コーデックス経由でチャッピーから納品。文言はチャッピーの裏取り済み
(形式Aのみ、外部照合対象なし)。一枚絵の要素配置はClaudeが確定(工程5)。

| 項目 | 内容 |
|---|---|
| トピックバッジ | `シンク下` |
| シリーズラベル | `暮らしの間違い探し / 02` |
| 見出し | `ここ、` / `NGが3つあります`(固定・変更なし) |

**一枚絵に描くもの**(シンク下収納棚の内部を正面から見た構図。扉は開いた状態)

| 要素 | 位置 | 種別 |
|---|---|---|
| 洗剤のストック(同一形状のボトルが3〜4本、列をなして並ぶ) | **下部左** | **NG①(易)** |
| 排水管まわりに直置きされた小物(スポンジ・ブラシ・布巾など、**NG①とは異なる形状**の物が数点、無造作に置かれている) | **中央下部**(排水管の根元) | **NG②(易)** |
| 重ねて収納された鍋2つ(下の鍋の一部が上の鍋に隠れて見えにくい) | **上部やや右**(小さめに) | **NG③(難)** |
| 収納棚の内部フレーム(枠・棚板) | 全体の骨格 | ダミー(正常・空間) |
| ゴミ袋のロール、ケースに収まりきちんと巻かれている | 右上 | ダミー(正常) |
| ゴム手袋、フックに掛けてある | 右下 | ダミー(正常) |
| 排水管本体(構造物) | 中央奥 | ダミー(正常・空間) |
| スポンジのストック、ケースに収まっている | 左上 | ダミー(正常) |
| キッチンペーパーの替え、立てて置かれている | 中央やや左 | ダミー(正常) |

**NG①・NG②の判別ルール(チャッピーの確認事項#3への対応)**: NG①は**同一形状のボトルの列**、
NG②は**形状の異なる複数の小物が排水管の根元に集まっている状態**とし、形状差で視覚的に区別する。
両者は画面内で離して配置し(4章ルール)、混同を避ける。

**解答テロップ(C4)** ← **確定(チャッピー納品版。形式Aのみで構成、出典不要)**

| # | 時間 | テロップ |
|---|---|---|
| ① | 10.00-11.33 | `洗剤のストック、` / `並んでいませんか` |
| ② | 11.33-12.67 | `排水管のまわりに、` / `物を直置きしていませんか` |
| ③ | 12.67-14.00 | `下の鍋に、別の鍋が` / `重なっていませんか` |

**③が「難」である理由**: 設計上、上部やや右に小さく配置するため。加えて、鍋が収納されていること
自体は不自然ではなく、**上下の重なりに気づく必要がある**点が難易度を上げる `【推測】`(チャッピー提出の
理由をClaudeが配置に反映)。

**CTA(確定)**: `いくつ分かった? コメントで`

**キャプション(確定)**

```
ここ、NGが3つあります👀

今回のテーマは「シンク下」。
片付けの視点で探す、暮らしの間違い探しです。

① 並んだ洗剤のストック
② 排水管まわりに直置きされた物
③ 重ねて収納された鍋

まずはシンク下に何があるか、見渡すところから。

いくつ分かった?コメントで

暮らしラク研究所｜@kurashi_rakulab
毎日の「ちょっと面倒」を、少しラクに。

※イラストは収納のイメージ図です。

#間違い探し #収納アイデア #片付け #暮らしの工夫 #暮らしラク研究所
```

**事実主張**: 無(形式Aのみ。外部の裏付けが必要な主張は含まれない)

**チャッピーからの確認事項への回答(Claude)**

| # | チャッピーの確認事項 | Claudeの回答 |
|---|---|---|
| 1 | 原案の本数は描画設定として維持可能か、適正数の基準として使うか | **描画のみに使用。基準として主張しない。**「何本以上がNG」という記述は一切行わない |
| 2 | 「見直す箇所」として扱う企画意図で成立するか | **成立する。** 8章の既存ルール(「NGは悪ではなく使いにくくなる理由として説明」「断定形を避ける」)そのものであり、新しい解釈ではない。**この解釈を標準として以降の全シーンに適用する**(下記「標準解釈」参照) |
| 3 | NG①とNG②を別対象として判別できる必要がある | 上記「NG①・NG②の判別ルール」で一枚絵の設計により対応 |

### #2 シンク下 確定版プロンプト(コーデックスにそのまま渡す)

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.
Follow the same visual style, safe areas, and timeline structure as
#1 玄関(9-1章参照)exactly — only the scene illustration and captions differ.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
Setting: the interior of an under-sink kitchen cabinet, viewed from the front
with the cabinet doors open.
- NG1 (easy): a row of 3-4 identical-shaped detergent refill bottles lined up,
  positioned bottom-left. Draw a specific count for visual purposes only —
  this is NOT asserting any "too many" threshold.
- NG2 (easy): a small cluster of DIFFERENTLY-SHAPED items (a sponge, a scrub
  brush, a folded rag) placed directly on the cabinet floor around the base
  of a drain pipe, positioned center-bottom. Must be visually distinct in
  shape from NG1's uniform bottle row — do not reuse bottle-like shapes here.
- NG3 (hard): two stacked pots, positioned upper-right, drawn small — the
  lower pot is partially hidden under the upper one.
- Dummy items, all drawn in a NORMAL tidy state: the cabinet's internal frame/
  shelving (structural), a roll of trash bags neatly cased (upper-right), a
  pair of rubber gloves hung on a hook (bottom-right), the drain pipe itself
  (structural, center-back), a spare sponge in a case (upper-left), a spare
  roll of paper towels standing upright (center-left).
Keep NG1/NG2/NG3 spaced apart from each other and from dummy items so their
160px-diameter answer circles won't overlap anything else.

TIMELINE: identical structure to #1(9-1章参照). Only these texts differ:
[0.00-2.00] Series label "暮らしの間違い探し / 02". Terracotta badge
  "シンク下". Headline "ここ、" / "NGが3つあります"(固定・変更なし).
[10.00-11.33] circle on NG1 + caption: "洗剤のストック、" / "並んでいませんか"
[11.33-12.67] circle on NG2 + caption: "排水管のまわりに、" / "物を直置きしていませんか"
[12.67-14.00] circle on NG3 + caption: "下の鍋に、別の鍋が" / "重なっていませんか"
[14.00-15.00] Caption: "いくつ分かった? コメントで". Loop per #1's spec
  (cross-fade from 14.70 to 15.00, no closing end-card).

HARD CONSTRAINTS: same as #1(6章参照)。特に:
- Never mention bacteria, germs, hygiene, disinfection, or food safety.
- Never state a specific quantity as a "correct" or "too many" threshold.
- Never assert future behavior (e.g., "the bottom pot will never be used
  again") — use only the exact caption text given above.
- Never put the answer inside the question text.
```

---

### #2 シンク下 納品記録・予約投稿(2026-09-12)

`【事実】` コーデックスから納品。プロジェクトID `sink02`。

| 項目 | 結果 |
|---|---|
| 総尺/解像度/fps/フレーム数 | 15.000秒(差分0.000秒) / 1080×1920 / 30fps / 450フレーム |
| エンコード | **H.264 High / yuv420p(標準プロファイル)**。#1のロスレス設定(High 4:4:4 Predictive相当)から変更 |
| ファイルサイズ | 19,598,748バイト(約18.7MB)。#1(約26.8MB)より軽量化 |
| 音声 | AAC LC 48kHz mono。**音声尺15.000000秒(映像と完全一致)**。#1の0.067秒ズレが解消 |
| 設計書11章チェックリスト | 17項目(バッジ確認を含む)すべて合格 |
| 逸脱事項 | AAC由来の音の前にじみ(9秒直前、約-65dBFS)。#1と同様、Lowと評価 |
| 費用 | 実行前後とも119.37クレジットで差分0.00。**Claudeが独立に`balance`/`transactions`を再確認し、新規取引が無いことも確認済み**(3回連続で同じ結果。企画書A-4の状況証拠がさらに強化) |
| 実機確認 | 2026-09-12、関野さんが実施。**問題なし**(映像・音声・ループとも) |
| Metricool予約投稿 | **実行済み**。投稿ID `374754270`、2026-09-13 20:00(Asia/Tokyo)公開予定、`autoPublish=true`、`isAiGenerated=false` |

---

### 標準解釈: 「NG」表記と「見直す箇所」の関係(全シーン共通・確定)

`【事実】` 2026-09-11、#2シンク下のチャッピーからの確認を機に明文化。**以降、同種の確認は不要。**

シリーズの決め台詞は「NGが3つあります」だが、これは**キャッチーな見出し表現**であり、
個々の解答テロップで「これは悪いことです」と断定するものではない。8章の表現ルール
(「NGは悪ではなく使いにくくなる理由として説明する」「断定形を避ける」)がこの関係を規定している。

- 見出し・バッジ: 「NG」という強い言葉をそのまま使ってよい(フックとして機能させる)
- 解答テロップ: 「〜していませんか」という**問いかけ**の形にとどめ、断定・基準・将来予測を含めない
- この2層構造(キャッチーな見出し + 控えめな解説)が、本シリーズの標準スタイルである

---

### 9-3. #3 冷蔵庫の中

`【事実】` 2026-09-12、コーデックス経由でチャッピーから納品。文言はチャッピーの裏取り済み
(形式Aのみ、外部照合対象なし)。前回(#2)からの改善点: ①の「使用実態」への言及を排除、
②の解答を問いかけ形に統一。一枚絵の要素配置はClaudeが確定(工程5)。

| 項目 | 内容 |
|---|---|
| トピックバッジ | `冷蔵庫の中` |
| シリーズラベル | `暮らしの間違い探し / 03` |
| 見出し | `ここ、` / `NGが3つあります`(固定・変更なし) |

**一枚絵に描くもの**(冷蔵庫内部を正面から見た構図。ドアポケットと本体棚を両方描く)

| 要素 | 位置 | 種別 |
|---|---|---|
| ドアポケットに並んだ調味料瓶3本(同一形状) | **ドア下段** | **NG①(易)** |
| 無地の不透明容器(正面に表示・ラベルが一切無いことが分かる描画) | **中段棚・中央** | **NG②(易)** |
| 最上段棚奥、牛乳パック(手前)の陰から、別の保存容器の角が**一部だけ見える**(完全には隠れていない) | **最上段棚・奥・端寄り** | **NG③(難・前景と背景の組み合わせ)** |
| 冷蔵庫内フレーム(棚板・仕切り) | 全体の骨格 | ダミー(正常・空間) |
| 野菜室の引き出し、閉まっている | 下部 | ダミー(正常) |
| 卵ケース、整然と収まっている | 中段棚・端 | ダミー(正常) |
| ドアポケットの飲み物ボトル1本、まっすぐ立っている | ドア上段 | ダミー(正常) |
| チーズなどの個包装、まとめてケースに収まっている | 中段棚・端 | ダミー(正常) |
| 透明な保存容器、中身が見える状態(NG②の不透明容器との対比) | 中段棚・別位置 | ダミー(正常) |

**チャッピーの6つの描画確認事項への対応**

| # | 確認事項 | Claudeの対応 |
|---|---|---|
| 1 | ①②③を別対象として分ける | ドア(①)・棚中央(②)・棚最上段(③)と、領域そのものを分離 |
| 2 | ②の容器を③の隠れた物と兼用しない | ②(中段・無地容器)と③の前景/背景(最上段・牛乳パック+保存容器)は別物として設計 |
| 3 | ③は奥の物が一部見え、解答で初めて追加しない | 探す時間から**保存容器の角が常に一部見えている**状態で描画する。解答時に初出させない |
| 4 | ②はラベルなしと分かる描画にする | 正面に表示物が一切無い無地容器として明示 |
| 5 | ①にヒントとなる札等を追加しない | 調味料瓶3本のみ。使用頻度等を示す要素は追加しない |
| 6 | NG3箇所を離し、易→易→難、③は上部/端 | 上表の配置で対応(ドア下段/棚中央/最上段奥端) |

**解答テロップ(C4)** ← **確定(チャッピー納品版。形式Aのみで構成、出典不要)**

| # | 時間 | テロップ |
|---|---|---|
| ① | 10.00-11.33 | `ドアポケットに、` / `調味料が並んでいませんか` |
| ② | 11.33-12.67 | `この容器、` / `ラベルなしで置いていませんか` |
| ③ | 12.67-14.00 | `手前の物で、` / `奥が隠れていませんか` |

**③が「難」である理由**: 設計上、最上段棚の奥・端寄りに配置するため。加えて、手前の物だけでなく
その後ろの見えにくい部分へ注意を向ける必要がある点が難易度を上げる `【推測】`(チャッピー提出の理由を
Claudeが配置に反映)。実際の難易度(視聴者による検証)は未実施。

**CTA**: 動画内テロップは `いくつ分かった? コメントで`(「?」の後に半角スペース、C5の指定どおり)。
キャプション内は `いくつ分かった?コメントで`(スペースなし、#1・#2の確定キャプションと同一表記)。

**キャプション(確定)**

```
ここ、NGが3つあります👀

今回のテーマは「冷蔵庫の中」。
片付けの視点で探す、暮らしの間違い探しです。

① ドアポケットに並んだ調味料
② ラベルのない不透明容器
③ 手前の物に隠れた奥の物

まずは調味料を、使う物かどうか確認するところから。

いくつ分かった?コメントで

暮らしラク研究所｜@kurashi_rakulab
毎日の「ちょっと面倒」を、少しラクに。

※イラストは収納のイメージ図です。

#間違い探し #収納アイデア #片付け #暮らしの工夫 #暮らしラク研究所
```

**事実主張**: 無(形式Aのみ。使用実態・購入履歴・効果・本数基準はすべて不採用として除外済み)

### #3 冷蔵庫の中 確定版プロンプト(コーデックスにそのまま渡す)

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.
Follow the same visual style, safe areas, and timeline structure as
#1 玄関(9-1章参照)exactly — only the scene illustration and captions differ.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
Setting: the interior of a refrigerator, viewed from the front with the door
open, showing both the door pocket shelves and the main body shelves.
- NG1 (easy): 3 identical-shaped condiment bottles lined up on the door
  pocket, positioned lower door area.
- NG2 (easy): a plain opaque container with NO visible label or markings on
  its front face, positioned on the middle shelf, center. Must be clearly
  distinct in location from NG1 (door vs. shelf).
- NG3 (hard): on the top shelf, toward the back and one edge, a milk carton
  sits in front of another storage container — the container behind must be
  PARTIALLY VISIBLE (a corner or edge peeking out) throughout the search
  phase. Do NOT introduce this hidden object only at the answer reveal.
- Dummy items, all drawn in a NORMAL tidy state: the fridge's internal frame/
  shelving (structural), a closed vegetable drawer (bottom), a neatly filled
  egg case (middle shelf edge), one beverage bottle standing upright in the
  door's upper pocket, individually wrapped cheese slices grouped in a case
  (middle shelf edge), and one transparent storage container with visible
  contents (middle shelf, elsewhere) as a contrast to NG2's opaque one.
Keep NG1/NG2/NG3 spaced apart from each other and from dummy items so their
160px-diameter answer circles won't overlap anything else.

TIMELINE: identical structure to #1(9-1章参照). Only these texts differ:
[0.00-2.00] Series label "暮らしの間違い探し / 03". Terracotta badge
  "冷蔵庫の中". Headline "ここ、" / "NGが3つあります"(固定・変更なし).
[10.00-11.33] circle on NG1 + caption: "ドアポケットに、" / "調味料が並んでいませんか"
[11.33-12.67] circle on NG2 + caption: "この容器、" / "ラベルなしで置いていませんか"
[12.67-14.00] circle on NG3(背景の保存容器側) + caption: "手前の物で、" / "奥が隠れていませんか"
[14.00-15.00] Caption: "いくつ分かった? コメントで"(半角スペースに注意). Loop per
  #1's spec(cross-fade from 14.70 to 15.00, no closing end-card).

HARD CONSTRAINTS: same as #1(6章参照)。特に:
- Never mention bacteria, germs, hygiene, disinfection, or food safety
  (even though this scene is a refrigerator — no expiration/spoilage/
  freshness claims of any kind).
- Never assert usage patterns (e.g., "these condiments are never used") or
  purchase history (e.g., "duplicate items were bought").
- Never introduce NG3's hidden container only at the reveal — it must be
  partially visible from 2.00s onward.
- Never put the answer inside the question text.
```

---

### #3 冷蔵庫の中 納品記録(2026-09-12)

`【事実】` コーデックスから納品。プロジェクトID `fridge03`。

| 項目 | 結果 |
|---|---|
| 総尺/解像度/fps/フレーム数 | 15.000秒(差分0.000秒) / 1080×1920 / 30fps / 450フレーム |
| エンコード | H.264 High / yuv420p(標準プロファイル)。#2から継続 |
| ファイルサイズ | 15,805,955バイト(約15.1MB)。#1→#2→#3と一貫して軽量化 |
| 音声 | AAC LC 48kHz mono。音声尺15.000000秒(映像と完全一致) |
| 設計書11章チェックリスト | 17項目すべて合格 |
| **NG③の重点検証** | 保存容器の右端・角が探索区間210フレーム全てで同一ピクセルとして視認可能であることを確認済み(拡大比較画像をZIPに同梱)。解答時の追加・移動なし。**#3で確立した「奥の物は探す時間から一部見えている」原則が正しく実装された** |
| 逸脱事項 | AAC由来の音の前にじみ(9秒直前、約-65dBFS)。#1・#2と同様、Lowと評価 |
| 費用 | 実行前後とも119.37クレジットで差分0.00。**Claudeが独立に`balance`/`transactions`を再確認し、新規取引が無いことも確認済み**(4回連続で同じ結果。企画書A-4の状況証拠がさらに強化) |

**Metricool予約投稿**: 実行済み。投稿ID`374776805`、2026-09-14 20:00(Asia/Tokyo)公開予定、`autoPublish=true`、`isAiGenerated=false`。実機確認(2026-09-12、問題なし)を経て実行。

---

### 9-4. #4 クローゼット

`【事実】` 2026-09-15、コーデックス経由でチャッピーから納品。**骨子変更を承認**:
NG③は当初案「『いつか着る服』が一番取りやすい高さを占領している」(着用意図・主観的な
便利さの断定を含み描画で確認不能)から、「手前の服に隠れた奥の服」(服の重なりのみ)に変更。
企画書8章の該当行もこれに合わせて更新済み。

| 項目 | 内容 |
|---|---|
| トピックバッジ | `クローゼット` |
| シリーズラベル | `暮らしの間違い探し / 04` |
| 見出し | `ここ、` / `NGが3つあります`(固定・変更なし) |

**一枚絵に描くもの**(クローゼット内部を正面から見た構図。ハンガーラックと床を両方描く)

| 要素 | 位置 | 種別 |
|---|---|---|
| 紙袋2〜3個が床に並ぶ | **床下部** | **NG①(易)** |
| 針金ハンガーと幅広の成形ハンガーが混在(**形状差**で判別。色に依存しない) | **ラック中央** | **NG②(易)** |
| 手前の服(厚手のコートなど)の脇から、奥の服の袖・裾が一部見える | **ラック上部・端寄り** | **NG③(難・前景と背景の組み合わせ)** |
| クローゼットの枠・ラックバー | 全体の骨格 | ダミー(正常・空間) |
| 揃ったハンガー(同一形状)が並ぶ区画 | ラック反対側 | ダミー(正常。NG②との対比) |
| 畳まれたセーター、棚の上に整然と積まれている | 上部棚 | ダミー(正常) |
| 収納ケース、ラベル付きで床に並んでいる | 床・NG①と離れた位置 | ダミー(正常) |
| 季節物ケース、床の隅にきちんと置かれている | 床・隅 | ダミー(正常) |
| 姿見または扉の一部 | 奥・背景 | ダミー(正常・空間) |

**NG②・NG③の判別ルール(チャッピーの確認事項1・2への対応)**: NG②(ハンガー混在)は
ラック中央に、NG③(服の重なり)はラック端に配置し、**別々の衣服・ハンガー群として重複させない。**
NG②は形状差(細い針金 vs 幅広の成形樹脂)で判別させ、色の違いには依存しない。

**解答テロップ(C4)** ← **確定(チャッピー納品版。形式Aのみで構成、出典不要)**

| # | 時間 | テロップ |
|---|---|---|
| ① | 10.00-11.33 | `クローゼットの床に、` / `紙袋が並んでいませんか` |
| ② | 11.33-12.67 | `ハンガーの種類、` / `混ざっていませんか` |
| ③ | 12.67-14.00 | `手前の服で、` / `奥の服が隠れていませんか` |

**③が「難」である理由**: 設計上、ラック上部・端寄りに配置するため。加えて、手前の服だけでなく
その後ろに一部見える服へ注意を向ける必要がある点が難易度を上げる `【推測】`。実際の難易度
(視聴者による検証)は未実施。**#3で確立した「奥の物は探す時間から一部見えている」原則を
本シーンにも適用**(探す時間中、奥の服の袖・裾が常に一部視認できる状態を維持し、解答時に
初めて追加したり手前の服を動かして見せたりしない)。

**CTA**: 動画内テロップは `いくつ分かった? コメントで`(半角スペースあり)。
キャプション内は `いくつ分かった?コメントで`(スペースなし、#1〜#3と同一表記)。

**キャプション(確定)**

```
ここ、NGが3つあります👀

今回のテーマは「クローゼット」。
片付けの視点で探す、暮らしの間違い探しです。

① 床に並んだ紙袋
② 種類の異なるハンガーの混在
③ 手前の服に隠れた奥の服

まずは床の紙袋を、使う物かどうか見直すところから。

いくつ分かった?コメントで

暮らしラク研究所｜@kurashi_rakulab
毎日の「ちょっと面倒」を、少しラクに。

※イラストは収納のイメージ図です。

#間違い探し #収納アイデア #片付け #暮らしの工夫 #暮らしラク研究所
```

**事実主張**: 無(形式Aのみ。着用意図・使用実態・効果・適正数の主張はすべて不採用として除外済み)

### #4 クローゼット 確定版プロンプト(コーデックスにそのまま渡す)

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.
Follow the same visual style, safe areas, and timeline structure as
#1 玄関(9-1章参照)exactly — only the scene illustration and captions differ.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
Setting: the interior of a closet, viewed from the front, showing a hanging
rod with clothes and floor space below.
- NG1 (easy): 2-3 paper shopping bags lined up on the floor, positioned
  bottom area.
- NG2 (easy): on the rod, center section, a mix of thin wire hangers and
  wide molded-plastic hangers — differentiate by SHAPE only (thin wire vs.
  wide molded), not by color, since the line-art style uses minimal color.
- NG3 (hard): on the rod, toward one end and upper area, a thick coat/jacket
  hangs in front of another garment — the garment behind must be PARTIALLY
  VISIBLE (a sleeve or hem peeking out from the side) throughout the search
  phase. Do NOT introduce this hidden garment only at the answer reveal, and
  do NOT move the front garment aside to reveal it then.
- Dummy items, all drawn in a NORMAL tidy state: the closet frame/rod
  (structural), a section of uniformly-shaped hangers on the opposite side
  of the rod (contrast to NG2), neatly folded sweaters stacked on a shelf
  above, a labeled storage case on the floor (away from NG1), a seasonal
  storage case tucked neatly in a floor corner, and part of a mirror or door
  in the background.
Keep NG1/NG2/NG3 spaced apart from each other and from dummy items so their
160px-diameter answer circles won't overlap anything else. NG2 and NG3 must
be clearly separate clusters of hangers/clothes — do not let them share the
same garments.

TIMELINE: identical structure to #1(9-1章参照). Only these texts differ:
[0.00-2.00] Series label "暮らしの間違い探し / 04". Terracotta badge
  "クローゼット". Headline "ここ、" / "NGが3つあります"(固定・変更なし).
[10.00-11.33] circle on NG1 + caption: "クローゼットの床に、" / "紙袋が並んでいませんか"
[11.33-12.67] circle on NG2 + caption: "ハンガーの種類、" / "混ざっていませんか"
[12.67-14.00] circle on NG3(奥の服側) + caption: "手前の服で、" / "奥の服が隠れていませんか"
[14.00-15.00] Caption: "いくつ分かった? コメントで"(半角スペースに注意). Loop per
  #1's spec(cross-fade from 14.70 to 15.00, no closing end-card).

HARD CONSTRAINTS: same as #1(6章参照)。特に:
- Never assert wearing intent (e.g., "these clothes will be worn someday")
  or subjective convenience (e.g., "this height is easiest to reach").
- Never introduce NG3's hidden garment only at the reveal — it must be
  partially visible from 2.00s onward.
- Do not rely on color alone to show NG2's hanger-type difference — use
  distinct shapes (thin wire vs. wide molded).
- Never put the answer inside the question text.
```

---

### #4 クローゼット 納品記録(2026-09-12)

`【事実】` コーデックスから納品。プロジェクトID `closet04`。

| 項目 | 結果 |
|---|---|
| 総尺/解像度/fps/フレーム数 | 15.000秒(差分0.000秒) / 1080×1920 / 30fps / 450フレーム |
| エンコード | H.264 High / yuv420p(標準プロファイル)。#2・#3から継続 |
| ファイルサイズ | 15,861,988バイト(約15.1MB) |
| 音声 | AAC LC 48kHz mono。音声尺15.000000秒(映像と完全一致) |
| 設計書11章チェックリスト | 17項目すべて合格 |
| **重点検証** | NG②は針金/成形ハンガーを形状差で描き分け(色に依存しない)。NG③は探索区間210フレーム全てで奥の服の袖露出が同一ピクセルと確認、解答時の追加・移動なし |
| 逸脱事項 | AAC由来の音の前にじみ(9秒直前、約-65dBFS)。#1〜#3と同様、Lowと評価 |
| 費用 | 実行前後とも119.37クレジットで差分0.00。**Claudeが独立に`balance`/`transactions`を再確認し、新規取引が無いことも確認済み**(5回連続で同じ結果) |

**Metricool予約投稿**: 実行済み。投稿ID`374776814`、2026-09-15 20:00(Asia/Tokyo)公開予定、`autoPublish=true`、`isAiGenerated=false`。実機確認(2026-09-12、問題なし)を経て実行。

---

### 9-5. #5 洗面所

`【事実】` 2026-09-12、コーデックス経由でチャッピーから納品。企画書8-1章の事前チェック
(「一番下が永久に使われない」を不採用)に加え、初回企画書が想定していた「振動で落ちやすい」
という表現も**チャッピーが自主的に不採用と判断**(静止画から直接確認できる状態ではなく、
形式B(自明な帰結)の基準を厳密に満たさないため)。一枚絵の要素配置はClaudeが確定(工程5)。

| 項目 | 内容 |
|---|---|
| トピックバッジ | `洗面所` |
| シリーズラベル | `暮らしの間違い探し / 05` |
| 見出し | `ここ、` / `NGが3つあります`(固定・変更なし) |

**一枚絵に描くもの**(洗面台と洗濯機を並べて正面から見た構図)

| 要素 | 位置 | 種別 |
|---|---|---|
| 洗面台下段に、トレーやケースを介さず直接置かれたストック(詰め替えパック等) | **洗面台下段** | **NG①(易)** |
| 洗濯機の天板に直接置かれた洗剤ボトル(独立した棚ではなく洗濯機本体の上と明示) | **洗濯機側・別区画** | **NG②(易)** |
| タオルが何層にも積み重なり、層の境目が視認できる状態 | **洗面台上部の棚** | **NG③(難)** |
| 洗面台本体・鏡 | 全体の骨格 | ダミー(正常・空間) |
| 洗濯機本体 | 全体の骨格(NG②の背景) | ダミー(正常・空間) |
| タオル掛けに掛かった使用中のタオル1〜2枚 | 洗面台脇 | ダミー(正常。NG③との対比) |
| 石鹸・歯ブラシスタンド、洗面台上に整然と置かれている | 洗面台上 | ダミー(正常) |
| 蓋付きゴミ箱 | 床・端 | ダミー(正常) |
| 空の洗濯かご | 床・端 | ダミー(正常) |

**チャッピーの3つの描画確認事項への対応**

| # | 確認事項 | Claudeの対応 |
|---|---|---|
| 1 | 「直置き」はケース・トレーが無い状態と確認できること | NG①はストックと設置面の間に何も無い状態として描画。ケース越しの収納と誤認されないようにする |
| 2 | NG②は洗濯機本体の上、独立棚と混同しない | 洗濯機の天板であることが明確に分かる構図とし、別の棚とは区別する |
| 3 | NG③は探す時間からタオルの層が見える描画、使用頻度札は不要 | タオルの積み重なりは常に視認可能な状態で描画。ヒントとなる札は追加しない |

**解答テロップ(C4)** ← **確定(チャッピー納品版。形式Aのみで構成、出典不要)**

| # | 時間 | テロップ |
|---|---|---|
| ① | 10.00-11.33 | `洗面台の下に、` / `ストックを直置きしていませんか` |
| ② | 11.33-12.67 | `洗濯機の上に、` / `洗剤を置いていませんか` |
| ③ | 12.67-14.00 | `タオルが、` / `積み重なっていませんか` |

**③が「難」である理由**: 設計上、洗面台上部の棚に配置するため。タオルの重なり自体へ注意を
向ける必要がある点が難易度を上げる `【推測】`。実際の難易度(視聴者による検証)は未実施。
下のタオルの使用実態には触れない。

**CTA**: 動画内テロップは `いくつ分かった? コメントで`(半角スペースあり)。
キャプション内は `いくつ分かった?コメントで`(スペースなし)。

**キャプション(確定)**

```
ここ、NGが3つあります👀

今回のテーマは「洗面所」。
片付けの視点で探す、暮らしの間違い探しです。

① 洗面台下に直置きされたストック
② 洗濯機の上に置かれた洗剤
③ 積み重なったタオル

まずは洗面台の下のストックを、確認するところから。

いくつ分かった?コメントで

暮らしラク研究所｜@kurashi_rakulab
毎日の「ちょっと面倒」を、少しラクに。

※イラストは収納のイメージ図です。

#間違い探し #収納アイデア #片付け #暮らしの工夫 #暮らしラク研究所
```

**事実主張**: 無(形式Aのみ。落下傾向・将来の使用・適正ストック数はすべて不採用として除外済み)

### #5 洗面所 確定版プロンプト(コーデックスにそのまま渡す)

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.
Follow the same visual style, safe areas, and timeline structure as
#1 玄関(9-1章参照)exactly — only the scene illustration and captions differ.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
Setting: a bathroom sink/vanity area with a washing machine beside it,
viewed from the front.
- NG1 (easy): under the sink cabinet, lower section, stock items (refill
  packs, spare bottles) placed DIRECTLY on the surface — no tray or case
  between the items and the surface.
- NG2 (easy): on top of the washing machine itself (not a separate shelf),
  a detergent bottle placed directly on the machine's top panel. Must be
  clearly on the washing machine, not on any nearby shelf.
- NG3 (hard): on an upper shelf near the sink, towels stacked in multiple
  visible layers — the layering must be visible throughout the search
  phase (not just at the reveal).
- Dummy items, all drawn in a NORMAL tidy state: the sink/vanity body and
  mirror (structural), the washing machine body itself (structural,
  background for NG2), 1-2 towels neatly hanging on a towel rack (contrast
  to NG3), a soap/toothbrush stand neatly placed on the vanity, a lidded
  trash bin, an empty laundry basket.
Keep NG1/NG2/NG3 spaced apart from each other and from dummy items so their
160px-diameter answer circles won't overlap anything else.

TIMELINE: identical structure to #1(9-1章参照). Only these texts differ:
[0.00-2.00] Series label "暮らしの間違い探し / 05". Terracotta badge
  "洗面所". Headline "ここ、" / "NGが3つあります"(固定・変更なし).
[10.00-11.33] circle on NG1 + caption: "洗面台の下に、" / "ストックを直置きしていませんか"
[11.33-12.67] circle on NG2 + caption: "洗濯機の上に、" / "洗剤を置いていませんか"
[12.67-14.00] circle on NG3 + caption: "タオルが、" / "積み重なっていませんか"
[14.00-15.00] Caption: "いくつ分かった? コメントで"(半角スペースに注意). Loop per
  #1's spec(cross-fade from 14.70 to 15.00, no closing end-card).

HARD CONSTRAINTS: same as #1(6章参照)。特に:
- Never mention bacteria, germs, hygiene, disinfection, or food safety.
- Never assert future events (e.g., "this will fall due to vibration") or
  usage patterns (e.g., "the bottom towel is never used") — use only the
  exact caption text given above.
- NG1's stock must be clearly directly on the surface, not inside a tray
  or case.
- NG2 must be clearly on the washing machine's top panel, not a shelf.
- Never put the answer inside the question text.
```

---

### #5 洗面所 納品記録(2026-09-12)

`【事実】` コーデックスから納品。プロジェクトID `washroom05`。

| 項目 | 結果 |
|---|---|
| 総尺/解像度/fps/フレーム数 | 15.000秒(差分0.000秒) / 1080×1920 / 30fps / 450フレーム |
| エンコード | H.264 High / yuv420p(標準プロファイル)。#2〜#4から継続 |
| ファイルサイズ | 14,531,975バイト(約13.9MB) |
| 音声 | AAC LC 48kHz mono。音声尺15.000000秒(映像と完全一致) |
| 設計書11章チェックリスト | 17項目すべて合格 |
| NG③の視認性 | 探索区間210フレーム全てでタオルの層が同一ピクセル。解答時の追加なし |
| **逸脱事項(要評価)** | 解答円の一部が支持面(洗面台の底線・洗濯機天板・タオル棚板)に重なる。**Low評価**: #1(郵便物の円が靴箱上端に重なった事例)と同種。「直置き」「天板の上」を示す構図上、対象物と支持面の接触点を含むのは自然かつ必然。他のNGや独立した小物とは重なっていない |
| その他の逸脱 | AAC由来の音の前にじみ(9秒直前、約-65dBFS)。#1〜#4と同様、Lowと評価 |
| 費用 | 実行前後とも119.37クレジットで差分0.00。**Claudeが独立に`balance`/`transactions`を再確認し、新規取引が無いことも確認済み**(6回連続で同じ結果) |

**次工程**: 関野さんによる実機(iPhone)再生確認待ち。

---

### 9-10. #10 食品ストック

`【事実】` 2026-09-12、コーデックス経由でチャッピーから納品。企画書8章のA案確定文言
(2026-09-12承認)を正確に反映。賞味期限・使用実態・購入履歴・将来行動への言及なし。
一枚絵の要素配置はClaudeが確定(工程5)。

| 項目 | 内容 |
|---|---|
| トピックバッジ | `食品ストック` |
| シリーズラベル | `暮らしの間違い探し / 10` |
| 見出し | `ここ、` / `NGが3つあります`(固定・変更なし) |

**設計上の例外(承認・2026-09-12)**: NG②「同じ食品が2箇所に分かれている」は、通常の
1NG=1解答円(160px円)では表現できない。**同一の戸棚内で近接する2段(中段・下段)に配置し、
円ではなく縦長の楕円形ハイライトで両方を1つの範囲として囲む例外を承認する。**
これは9-0章の標準仕様(円・160px直径)からの明示的な例外であり、他のNGには適用しない。

**一枚絵に描くもの**(食品ストック棚を正面から見た構図。戸棚と床置きスペースを両方描く)

| 要素 | 位置 | 種別 |
|---|---|---|
| 袋のまま床に置かれた食品(米・パスタ袋等。ブランド・ロゴなし) | **床下部** | **NG①(易)** |
| 同一形状・柄の食品パッケージ(缶詰等)が、同じ戸棚の中段・下段に分かれて置かれている | **中央棚・中段+下段(近接)** | **NG②(易・楕円ハイライト)** |
| 手前の食品(箱型)の陰から、奥の食品(別容器)の角が一部見える | **上部棚・奥・端寄り** | **NG③(難・前景と背景の組み合わせ)** |
| 食品棚のフレーム・棚板 | 全体の骨格 | ダミー(正常・空間) |
| 種類の異なる食品が整然と並んだ区画(NG②との対比) | 別の棚 | ダミー(正常) |
| ラベル付き保存容器、整然と並んでいる | 棚・端 | ダミー(正常) |
| 畳んでまとめられた買い物袋 | 棚・端 | ダミー(正常) |
| 調味料の予備1本、きちんと立てて置かれている | 棚・端 | ダミー(正常) |
| 重ねて置かれた空のかご | 床・端 | ダミー(正常) |

**チャッピーの4つの描画確認事項への対応**

| # | 確認事項 | Claudeの対応 |
|---|---|---|
| 1 | NG①は床との接触が見え、棚板・ケースの上と区別できること | 床に直接置かれた状態として描画。棚上の食品と混同しない位置に配置 |
| 2 | NG②は同じ食品と識別できる形状・図柄をそろえ、実在の商品名・ロゴを使わない | 同一形状の抽象的な缶型パッケージで統一。ブランド要素は一切描画しない |
| 3 | NG③は奥の食品の角が探す時間から常に一部見えること。解答で初出させない | #3・#4・#5と同じ「隠れた奥の物」原則を適用 |
| 4 | NG①②③を別対象とし兼用しない | 床(①)・中央棚(②)・上部棚(③)と、領域そのものを分離 |
| — | NG②の解答円が標準仕様で成立しない場合の扱い | 上記「設計上の例外」で楕円ハイライトを承認 |

**解答テロップ(C4)** ← **確定(チャッピー納品版。形式Aのみで構成、出典不要)**

| # | 時間 | テロップ |
|---|---|---|
| ① | 10.00-11.33 | `食品を袋のまま、` / `床に置いていませんか` |
| ② | 11.33-12.67 | `同じ食品が、` / `別々の場所にありませんか` |
| ③ | 12.67-14.00 | `手前の食品で、` / `奥の食品が隠れていませんか` |

**③が「難」である理由**: 設計上、上部棚の奥・端寄りに配置するため。手前の食品の後ろに
一部見える食品へ注意を向ける必要がある点が難易度を上げる `【推測】`。実際の難易度
(視聴者による検証)は未実施。

**CTA**: 動画内テロップは `いくつ分かった? コメントで`(半角スペースあり)。
キャプション内は `いくつ分かった?コメントで`(スペースなし)。

**キャプション(確定)**

```
ここ、NGが3つあります👀

今回のテーマは「食品ストック」。
片付けの視点で探す、暮らしの間違い探しです。

① 袋のまま床に置かれた食品
② 別々の場所に置かれた同じ食品
③ 手前の食品に隠れた奥の食品

まずは食品の置き場所を、見渡すところから。

いくつ分かった?コメントで

暮らしラク研究所｜@kurashi_rakulab
毎日の「ちょっと面倒」を、少しラクに。

※イラストは収納のイメージ図です。

#間違い探し #収納アイデア #片付け #暮らしの工夫 #暮らしラク研究所
```

**事実主張**: 無(形式Aのみ。賞味期限・使用実態・購入履歴・将来行動・適正数の主張は
すべて不採用として除外済み)

### #10 食品ストック 確定版プロンプト(コーデックスにそのまま渡す)

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.
Follow the same visual style, safe areas, and timeline structure as
#1 玄関(9-1章参照)exactly — only the scene illustration, captions, and
NG2's highlight shape (see below) differ.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
Setting: a food-stock pantry area, viewed from the front, showing both a
cabinet with shelves and floor storage space.
- NG1 (easy): a bag of food (e.g., rice or pasta bag, NO brand/logo) placed
  directly on the floor, positioned lower area.
- NG2 (easy): identical-shaped food packages (e.g., generic cans, NO brand/
  logo) split between two adjacent shelves (middle and lower) of the SAME
  cabinet unit, positioned close together vertically so both fit within
  one highlight area.
- NG3 (hard): on an upper shelf, toward the back and one edge, a box-shaped
  food item sits in front of another container — the container behind must
  be PARTIALLY VISIBLE (a corner or edge peeking out) throughout the search
  phase. Do NOT introduce this hidden item only at the answer reveal.
- Dummy items, all drawn in a NORMAL tidy state: the pantry frame/shelving
  (structural), a section with clearly DIFFERENT food items neatly arranged
  (contrast to NG2), labeled storage containers neatly lined up, folded
  shopping bags grouped together, one spare condiment bottle standing
  upright, and empty baskets stacked neatly on the floor.
Keep NG1/NG2/NG3 spaced apart from each other and from dummy items.

**IMPORTANT EXCEPTION for NG2's answer highlight**: unlike every other NG in
this series (which use a single 160px-diameter outline circle), NG2 requires
an ELONGATED VERTICAL OVAL outline (terracotta, no fill) that encompasses
BOTH the middle-shelf and lower-shelf items together, since NG2 depicts one
concept split across two nearby locations. This is an approved, one-time
exception — do not apply this oval shape to NG1 or NG3, which use the
standard circle.

TIMELINE: identical structure to #1(9-1章参照). Only these texts differ:
[0.00-2.00] Series label "暮らしの間違い探し / 10". Terracotta badge
  "食品ストック". Headline "ここ、" / "NGが3つあります"(固定・変更なし).
[10.00-11.33] circle on NG1 + caption: "食品を袋のまま、" / "床に置いていませんか"
[11.33-12.67] OVAL(see exception above) on NG2 + caption: "同じ食品が、" / "別々の場所にありませんか"
[12.67-14.00] circle on NG3 + caption: "手前の食品で、" / "奥の食品が隠れていませんか"
[14.00-15.00] Caption: "いくつ分かった? コメントで"(半角スペースに注意). Loop per
  #1's spec(cross-fade from 14.70 to 15.00, no closing end-card).

HARD CONSTRAINTS: same as #1(6章参照)。特に:
- Never mention bacteria, germs, hygiene, disinfection, or food safety
  (this is a food-storage scene — no expiration/freshness/spoilage claims
  of any kind).
- Never assert purchase history (e.g., "duplicate items were bought") or
  usage patterns.
- No brand names, product names, or logos anywhere in the illustration.
- Never introduce NG3's hidden item only at the reveal — it must be
  partially visible from 2.00s onward.
- Never put the answer inside the question text.
```

---

## 10. HyperFrames 生成プロンプト雛形(参考・現在は未使用)

`【事実】` 2026-09-11時点、コーデックスの実行環境ではHyperFramesが使えないため、
**本章は使用しない。** Higgsedit/FFmpegでの制作は9-0章のパラメータと、9章末尾の
「#1玄関 確定版プロンプト」(内容はツール非依存)を参照する。
本章は、将来HyperFramesが使える環境に戻った場合の参考として保持する。

以下をベースに、9章のシーン別内容を差し込んで `compose` を実行してください。(HyperFrames利用時)

```
Create a vertical 9:16 video, exactly 15.0 seconds, 1080x1920, 30fps.

VISUAL STYLE — match the brand's existing videos exactly. Use the `claude`
built-in style for consistency.
- Warm cream background (#F0E9DC)
- Deep forest green headline text (pick the exact green from the brand's
  existing videos; do not invent a new green)
- Terracotta orange rounded topic badge (same — pick from existing videos)
- Subtle scattered paper-square background texture
- Calm flat line-art illustration, drawn with deep green strokes only,
  minimal fill
- Quiet editorial tone. NO spoken narration, NO voice synthesis.
  On-screen text + sound effects only.

SAFE AREAS — keep all text within y=300..1450 and x=80..900.

SCENE ILLUSTRATION (one single static drawing, used across the whole video):
<9章の「一枚絵に描くもの」の表をここに転記>
Draw all dummy items in a NORMAL, tidy state. Do not make them ambiguous.

TIMELINE:
[0.00-2.00] Series label "暮らしの間違い探し / 01" small at top.
  Terracotta badge "玄関". Bold deep-green headline
  "ここ、" / "NGが3つあります".
  The illustration fades in from opacity 0.25 at 0.30s to 1.0 at 2.00s —
  it MUST be clearly visible by 1.0s.
  SFX: one soft pop at 0.00.

[2.00-9.00] SEARCH TIME. Show the illustration full, COMPLETELY STATIC.
  No zoom, no pan, no parallax, no element animation whatsoever.
  Small label "NGは3つ" at y=330.
  A thin terracotta progress bar at y=1450 depletes right-to-left over 7.0s.
  Do NOT show numbers counting down. Do NOT show any hint or marker.
  SFX: silence.

[9.00-10.00] Cream overlay at 0.85 opacity over the illustration.
  Centered deep-green text "答え合わせ". SFX: one soft chime. Exactly 1.0s.

[10.00-14.00] Remove the overlay. Reveal the three NGs in this exact order,
  drawing an OUTLINE-ONLY terracotta circle (no fill, ~160px diameter) at
  each location. Circles ACCUMULATE — do not erase previous ones.
  Each circle draws in over 0.25s.
  [10.00-11.33] circle on NG1 + caption at y=1400: <①のテロップ>
  [11.33-12.67] circle on NG2 + caption: <②のテロップ>
  [12.67-14.00] circle on NG3 + caption: <③のテロップ>
  SFX: same pop for the first two; a higher/stronger pop for the third.

[14.00-15.00] Keep the illustration with all three circles.
  Caption at y=1400: "いくつ分かった? コメントで".
  From 14.70 to 15.00, cross-fade back into the exact 0.00 frame layout so
  the video loops seamlessly. Do NOT use a closing end-card.

HARD CONSTRAINTS:
- Never mention bacteria, germs, hygiene, disinfection, or food safety.
- Never state money amounts, electricity costs, or savings percentages.
- No brand names, product names, logos, or people.
- Never put the answer inside the question text.
- Use "〜だと、こうなりやすい" phrasing, never "〇〇はNG" as an assertion.
```

---

## 11. 納品チェックリスト(Codex → Claude)

動画納品時に、以下を**テキストで添えて**ください。Claudeは完成動画を目視できないため、
これが無いと予約投稿の可否を判断できません。

- [ ] 総尺は 15.000秒(または短尺版12.000秒)ちょうどか
- [ ] 解像度 1080×1920 / 30fps / MP4 か
- [ ] **全テロップの文字起こし**(カットごと)
- [ ] **一枚絵に描かれた全要素のリスト**(NG3箇所とダミーを区別して)
- [ ] **問題文の中に答えが含まれていないか** ← 事故事例#1
- [ ] **衛生・細菌・健康・食品安全の語が1つも無いか** ← 事故事例#2
- [ ] **金額・電気代・削減率の数値が無いか**
- [ ] 出典が必要な事実主張が含まれていないか ← 事故事例#3
- [ ] NG3箇所が画面内で離れているか
- [ ] 解答の順が 易 → 易 → 難 になっているか
- [ ] 探す時間(C2)中に一枚絵が完全に静止しているか
- [ ] 探す時間中にヒント・マーカーが映っていないか
- [ ] 最終フレームが冒頭フレームと一致し、ループするか
- [ ] 安全領域(上220 / 下1536以降 / 右918以降)にテロップが掛かっていないか
- [ ] ナレーション・音声合成が入っていないか
- [ ] **絵コンテ画像またはサムネイル**(Claudeが内容を確認できる形で)
- [x] トピックバッジの見た目が意図通りか(塗りつぶしかテキストのみか) → **#1玄関で解決済み。塗りつぶし角丸+クリーム文字と確認**

---

## 12. 未確定事項

| # | 項目 | 影響 |
|---|---|---|
| 1 | 深緑・テラコッタの正確なカラーコード | 既存動画との一貫性。Codex側でのカラーピックが必要 |
| ~~2~~ | ~~エンディング仕様(企画書 A-1)~~ | **2026-09-11承認済み。締めカードなしで確定** |
| ~~3~~ | ~~BGM・音源の可否~~ | **2026-09-11承認済み**。BGMなし、効果音のみで確定 |
| 4 | `isAiGenerated` の申告値 | 既存2本は `false`。本シリーズは完全AI生成のため要確認 |
| ~~5~~ | ~~既存リール2本の尺~~ | **解決済み**。20.000秒/600フレーム(ffprobe実測)。企画書1章に完了率を反映 |
| 6 | Higgsfieldでのレンダリング費用 | **状況証拠が強化**。#1玄関の納品(静止フレーム9枚+動画本体+ZIP)後もClaudeが独立に確認し、残高119.37クレジット・新規取引0件を再確認(2026-09-11)。ただし公式な確約ではなく企画書A-4は未承認のまま |

---

## 13. 更新履歴

| 日付 | 内容 |
|---|---|
| 2026-09-11 | 初版作成(ドラフト)。Codexが動画生成を担当する前提で、カット割り・一枚絵設計・生成プロンプト雛形・納品チェックリストを定義 |
| 2026-09-11 | **#1玄関 納品を記録**。コーデックス納品(プロジェクトID genkan01-realism)を9章末尾に記録。バッジ色の留保を解決。費用の状況証拠をClaudeが独立に再確認(残高・取引履歴とも変化なし)。エンコードプロファイルの互換性未検証をMedium課題として記録し、実機確認を次工程の必須ゲートに設定 |
| 2026-09-11 | **A-2/A-3承認、A-8方針確定**。BGMなしで確定。毎日投稿(週7本、間違い探し6本+クイズ1本)。企画書8-2章に「クイズ枠」の新ルールを新設(旧「暮らしの豆知識帳/01」は不採用のまま) |
| 2026-09-11 | **連携フローを変更**。コーデックスがチャッピーとの窓口を担当することに変更(0-2-1新設)。0-1/0-2/0-3を更新し、コーデックスの新たな禁止事項(ルールの省略・改変禁止)を追加。Claudeの最終レビュー工程は不変 |
| 2026-09-12 | **#2シンク下を確定**。コーデックス経由でチャッピーから納品を受け、禁止事項チェック合格。一枚絵の要素配置をClaudeが確定(9-2章)。チャッピーの3つの確認事項に回答し、「NGと見直す箇所」の標準解釈を明文化(以降の全シーン共通ルール) |
| 2026-09-12 | **#3冷蔵庫の中を確定**。コーデックス経由でチャッピーから納品を受け、禁止事項チェック合格(前回からの改善: ①の使用実態への言及を排除、②の解答を問いかけ形に統一)。チャッピーの6つの描画確認事項に対応し、9-3章に一枚絵の配置を確定。NG③(奥の物)は探す時間から一部視認できる設計とし、解答で初出させない原則を明記 |
| 2026-09-15 | **#4クローゼットを確定**。チャッピー提案の骨子変更(NG③『いつか着る服』→『手前の服に隠れた奥の服』)を承認。9-4章に一枚絵の配置を確定。企画書8章の全14シーンを事前チェックし、#5以降に残る同種の問題(使用実態・将来行動・頻度の断定)を洗い出した(企画書8-1章) |
| 2026-09-12 | **#2シンク下を納品・予約投稿**。標準H.264 Highプロファイルへ改善(ロスレス設定から変更)、音声尺のズレも解消。実機確認(問題なし)を経て投稿ID374754270で予約。費用の状況証拠をClaudeが再確認(3回連続で変化なし) |
| 2026-09-11 | 9/8との色照合結果(RGB差3以内)を反映。テラコッタが文字採取値である留保を追記し、11章チェックリストにバッジ目視確認を追加。既存動画の尺(20.000秒/600フレーム)を12章で解決済みに更新。費用の状況証拠(残高・取引履歴)を12章に追記 |
| 2026-09-11 | **色を確定**。コーデックスが9/9投稿から抽出した値(背景#F6F1E5・深緑#24473E・テラコッタ#E0785E)を9-0章に反映。9/8との照合は未実施と明記 |
| 2026-09-11 | 0-6-1に既存2本のMP4 URLを追記(コーデックスからの依頼に対応) |
| 2026-09-11 | **制作ツールを変更**。コーデックスの実行環境でHyperFramesが使えないため、Higgsfield(Higgsedit)+FFmpegに変更(0-6章)。0-4に事実追記、9-0章にツール非依存の制作パラメータを新設、10章はHyperFrames利用時の参考として保持。既存動画からの色抽出をコーデックスに依頼(0-6-1・未解決) |
| 2026-09-11 | **#1玄関 確定**。チャッピー納品の解答テロップ・キャプションを反映(2回の差し戻しを経て形式Aのみで確定)。5章に解答テロップの許容形式ルール(形式A/B)を追加。コーデックスにそのまま渡せる確定版プロンプトを9章に追加 |
| 2026-09-11 | **A-1承認**。C5の締めカード廃止を確定仕様に変更。代替案(14.0-14.7秒に短縮)を削除 |
| 2026-09-11 | 決め台詞を「この部屋、NGが3つあります」→**「ここ、NGが3つあります」に変更**し全シーン固定と規定(3章C1 / 5章 / 9章 / 10章プロンプト雛形に反映) |
| 2026-09-11 | 0章を全面改稿。チャッピー(ChatGPT)とコーデックス(Codex)を分離し、成果物別の担当表・各者の禁止事項・分担根拠・HANDOFFフォーマットを追加 |
| 2026-09-12 | **#3冷蔵庫の中を納品**。設計書11章チェックリスト17項目合格。NG③(隠れた保存容器)の視認性を拡大比較画像で重点検証。エンコードは#2と同じ標準H.264 High/yuv420p、音声尺も映像と完全一致。費用の状況証拠をClaudeが4回目の独立確認(変化なし) |
| 2026-09-12 | **#4クローゼットを納品**。設計書11章チェックリスト17項目合格。NG②の形状差描写、NG③の視認性(210フレーム同一ピクセル)を重点検証済み。エンコードは#2・#3と同じ標準H.264 High/yuv420p。費用の状況証拠をClaudeが5回目の独立確認(変化なし) |
| 2026-09-12 | **#5洗面所を確定**。コーデックス経由でチャッピーから納品を受け、禁止事項チェック合格。当初想定していた「振動で落ちやすい」という表現もチャッピーが自主的に不採用と判断(形式Bの基準を厳密に満たさないため)。一枚絵の配置を9-5章に確定 |
| 2026-09-12 | **#10食品ストックを確定**。A案確定文言を正確に反映した納品を受け、禁止事項チェック合格。NG②(同じ食品が2箇所に分かれている)は標準の1NG=1円では表現できないため、縦長楕円ハイライトへの例外を承認(9-10章に明記、他NGには適用しない)。一枚絵の配置を確定 |
| 2026-09-12 | **#5洗面所を納品**。設計書11章チェックリスト17項目合格。解答円と支持面の重なりを#1の前例と同様Lowと評価。エンコードは標準H.264 High/yuv420p、音声尺も映像と完全一致。費用の状況証拠をClaudeが6回目の独立確認(変化なし) |
