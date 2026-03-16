# ECHO

**Embedded Cross-media Homage Offering**

Let every creative work carry its own echoes. A metadata spec for cross-media influence and homage.

---

## What is ECHO

ECHO is a minimal metadata specification that lets any creative work carry its own lineage and resonance.

A novel, a painting, a piece of music, a 3D model — any file can have a companion `echo.yaml` that describes where it came from, what it was shaped by, and what it speaks to.

No platform owns this information. The work carries it.

---

## Why not Dublin Core

Dublin Core has a `relation` element. But its relation types — `HasPart`, `IsVersionOf`, `HasFormat` — are library concepts, not creative ones.

Dublin Core cannot describe:

- "This work was shaped by that painting"
- "These two works were born from the same feeling"
- "This is an answer to that poem"

ECHO is not a discovery protocol. It is a homage protocol.

---

## Schema (v1.0)

```yaml
echo_version: 1.0
authored_by: creator   # creator / curator / researcher / community

meta:
  title:
  creator:
  medium:        # novel / painting / music / poem / model / film / ...

origin:
  derived_from:  # URL or identifier of the direct source (if any)

resonance:
  - url:         # URL or identifier
    type:        # influence / derived / parallel / response / homage / contrast / sample
    note:        # optional, in any language

audience:
  - note:        # optional, written by those who received the work
```

Any field except `echo_version` is optional. A valid `echo.yaml` can be as small as:

```yaml
echo_version: 1.0
authored_by: creator

resonance:
  - url: https://en.wikipedia.org/wiki/Vermeer
    type: influence
    note: the way light enters from the left
```

---

## resonance types

| type | meaning |
|---|---|
| `influence` | this work was shaped by that work |
| `derived` | direct derivation or fan work |
| `parallel` | made in the same period, same feeling, same question |
| `response` | an answer, a continuation, a reply |
| `homage` | explicit tribute |
| `contrast` | made in opposition — disagreement is also homage |
| `sample` | direct quotation or sampling |

---

## Any file. Any medium.

```
novel.md          painting.png       sculpture.glb
novel.echo.yaml   painting.echo.yaml sculpture.echo.yaml
```

The `url` field in `resonance` accepts anything with an identifier:

```yaml
resonance:
  - url: https://github.com/someone/novel
  - url: https://www.pixiv.net/artworks/xxxxx
  - url: https://archive.org/details/xxxxx
  - url: isbn:978-4-10-109205-5
```

ECHO does not depend on any platform. GitHub is one possible host, not a requirement.

---

## Three layers

`echo.yaml` is written by three different kinds of contributors, and they remain distinct. The `authored_by` field declares which layer is speaking:

| `authored_by` | written by | examples |
|---|---|---|
| *(omitted)* | tools, automation | `_generated` block only |
| `creator` | the creator | intent, influence, lineage |
| `curator` / `researcher` | third party on behalf of past works | scholarly interpretation |
| `community` | collective maintenance | open contribution |

A creator's own declaration and a curator's interpretation are both valid. They are not the same thing. `authored_by` keeps them distinct.

The `audience` block is written by those who received the work, regardless of `authored_by`.

---

## Design principles

- The core schema is small and will not change after v1.0
- Extensions may be proposed as `ECHO-EXT-*` by anyone
- No central registry is required
- No platform dependency
- Homage is self-declared, not algorithmically inferred

---

## Name

ECHO — Embedded Cross-media Homage Offering

See [PHILOSOPHY.md](./PHILOSOPHY.md) for the full reasoning.

---

## Related

[story-passport](https://github.com/sukoyaka-dopeness/story-passport) — a novel-specific implementation of ECHO, with a browser extension reader and Japanese typography support.

---

## License

MIT

## Author

[sukoyaka-dopeness](https://github.com/sukoyaka-dopeness)

---

## 日本語

**ECHO — Embedded Cross-media Homage Offering**

すべての創作物が、自分のエコーを持ち歩けるように。メディアを横断するオマージュのためのメタデータ仕様です。

---

### ECHOとは

ECHOは、あらゆる創作物が自分の来歴と共鳴を持ち歩くための、最小限のメタデータ仕様です。

小説、絵画、音楽、3Dモデル——どんなファイルにも、`echo.yaml`というサイドカーファイルを添えることができます。そこには、この作品がどこから生まれたか、何に形づくられたか、何に語りかけているかが記述されます。

この情報をプラットフォームは所有しません。作品自身が持ち歩きます。

---

### Dublin Coreではできないこと

Dublin Coreにも`relation`要素があります。しかしそのタイプ——`HasPart`、`IsVersionOf`、`HasFormat`——は図書館的な概念であり、創作的な概念ではありません。

Dublin Coreで記述できないもの：

- 「あの絵画に形づくられた」
- 「同じ感情から生まれた、別の作品」
- 「あの詩への返答として書いた」

ECHOは発見のプロトコルではありません。オマージュのプロトコルです。

---

### スキーマ (v1.0)

`echo_version`と`authored_by`以外のすべてのフィールドは省略可能です。最小限の`echo.yaml`はこれだけで成立します：

```yaml
echo_version: 1.0
authored_by: creator

resonance:
  - url: https://en.wikipedia.org/wiki/Vermeer
    type: influence
    note: 左から差し込む光の使い方
```

`authored_by`には`creator`（作者本人）、`curator`（学芸員・研究者）、`researcher`、`community`が入ります。作者自身の宣言と、第三者による解釈を区別するためのフィールドです。

---

### resonance typesの意味

| type | 意味 |
|---|---|
| `influence` | あの作品に形づくられた |
| `derived` | 直接の派生・二次創作 |
| `parallel` | 同時期、同じ問い、同じ感情から |
| `response` | 返答・続き・アンサー |
| `homage` | 明示的なオマージュ |
| `contrast` | 反発・アンチテーゼ——対立もまたリスペクト |
| `sample` | 引用・サンプリング |

---

### どんなファイルにも、どんなメディアにも

ECHOはプラットフォームに依存しません。GitHubは使える場所のひとつであり、前提ではありません。`resonance`の`url`フィールドには、識別子を持つものであれば何でも記述できます。

---

### 三つの層

`echo.yaml`は三種類の書き手によって書かれ、それぞれは混在しません。

| 層 | 書き手 | 内容 |
|---|---|---|
| `_generated` | ツール・自動化 | ファイルサイズ、fork元など |
| `meta` `origin` `resonance` | 作者 | 意図、影響、来歴 |
| `audience` | 受け手 | 体験、入口、個人的な記録 |

作者が意図したことと、受け手が感じたことは別のものです。ECHOはそれを混ぜません。

---

### 設計原則

- コアスキーマは小さく保たれ、v1.0以降変更されません
- 拡張は`ECHO-EXT-*`として誰でも提案できます
- 中央レジストリは不要です
- プラットフォームに依存しません
- オマージュは自己申告です。アルゴリズムが判定するものではありません

---

### 名前について

ECHO — Embedded Cross-media Homage Offering

詳細は [PHILOSOPHY.md](./PHILOSOPHY.md) を参照してください。

---

## License

MIT

## Author

[sukoyaka-dopeness](https://github.com/sukoyaka-dopeness)
