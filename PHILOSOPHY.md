# ECHO — Philosophy

---

## Why ECHO exists

Every creative work is shaped by something that came before it.

A novel carries the shadow of a painting. A song answers a poem written a century earlier. A sculpture was born from the same grief as a film made on the other side of the world.

These relationships exist. But no platform holds them. When a service shuts down, when an algorithm changes, when a ranking cycle buries a work — the connections disappear.

ECHO exists because a work's resonance belongs to the work, not to the platform that hosts it.

---

## What ECHO gives to creators

The act of writing an `echo.yaml` is not administrative. It is a creative act.

To name what shaped you is to understand your own work more clearly. To declare an influence is to place yourself inside a longer story — one that existed before you and will continue after you.

ECHO gives creators:

- A way to say "I was here, and this is what I was listening to"
- A record that travels with the work, not with the platform
- A map of influence that no algorithm could infer

---

## What ECHO gives to audiences

A work that carries its own `echo.yaml` is an invitation.

The audience can follow the resonance — from this novel to that painting, from that painting to a piece of music, from that music to a poem written four hundred years ago. Not because an algorithm suggested it. Because the creator pointed there.

This is discovery through trust, not through optimization.

---

## What ECHO contributes to creative culture

Platforms optimize for engagement. Engagement rewards what is already popular. What is already popular gets more exposure. The cycle continues.

ECHO does not oppose this. It simply exists elsewhere.

A constellation built from `resonance` links is not a ranking. It has no top. It has no algorithm. It grows as creators declare their influences, and it can be entered from any point.

This is what creative culture looked like before platforms — works in conversation with works, across media, across centuries, across languages. ECHO is an attempt to make that conversation legible again.

---

## On trust and forgery

ECHO contains no authentication mechanism. Any `echo.yaml` can be written by anyone. Timestamps can be altered. Influences can be fabricated.

This is intentional.

ECHO does not prove trust. It expresses it.

The weight of an expression depends on the relationship between the creator and the community around the work. A fabricated `resonance` link does not damage ECHO — it damages the creator who wrote it. The constellation simply does not grow in that direction.

This is how trust has always worked in creative culture. A painter who falsely claims Vermeer as an influence is not believed. Not because a system prevented the claim. Because the work does not carry it.

> ECHO records intention, not fact. The community decides what to follow.

---

## On platforms and independence

ECHO does not require GitHub. It does not require any platform.

An `echo.yaml` can live on a personal server, inside a file's metadata, behind a QR code on a physical object, embedded in an NFC tag beside a painting.

The spec is the only thing that needs to be shared. The files can live anywhere.

This is not anti-platform. It is platform-indifferent. Platforms are welcome to read and display `echo.yaml` data. They simply cannot own it.

---

## On the name

An echo does not ask permission.

It is what remains after something has been heard — shaped by the original, but no longer identical to it. It travels into spaces the original never reached. It fades into other echoes.

A creative work is the same. It leaves the creator and becomes something else in each person who receives it. The `echo.yaml` is a record of that outward movement — where the work came from, what it is still in conversation with, what it hopes to reach.

---

## On past works and absent creators

Vermeer cannot write an `echo.yaml`. Neither can Murasaki Shikibu, nor Coltrane.

This does not mean their works are excluded from the constellation. It means someone else must speak carefully on their behalf — and must say so.

ECHO distinguishes the source of a declaration through the `authored_by` field:

```yaml
echo_version: 1.0
authored_by: curator  # creator / curator / researcher / community

resonance:
  - url: https://en.wikipedia.org/wiki/Caravaggio
    type: influence
    note: the use of shadow as weight
```

A `curator` or `researcher` may write an `echo.yaml` for a past work. A `community` may collectively maintain one. The field is not a credential — it is a disclosure.

> Past works do not speak for themselves in ECHO. But others may speak carefully on their behalf — provided they say who is speaking.

This keeps the constellation open across centuries, while preserving the distinction between a creator's own declaration and an interpretation made by others.

---

## Relation to story-passport

[story-passport](https://github.com/sukoyaka-dopeness/story-passport) is a novel-specific implementation of ECHO, built around Japanese typography, a browser extension reader, and a Markdown dialect for ruby, emphasis dots, and vertical writing.

story-passport is where ECHO began. ECHO is where story-passport points.

---

## License

MIT

## Author

[sukoyaka-dopeness](https://github.com/sukoyaka-dopeness)

---

## 日本語

---

### なぜECHOは存在するか

あらゆる創作物は、何か先にあったものに形づくられています。

小説は一枚の絵画の影を持っている。ある歌は一世紀前に書かれた詩への返答です。ある彫刻は、地球の反対側で作られた映画と同じ悲しみから生まれた。

こうした関係は存在しています。しかしどのプラットフォームもそれを保持しません。サービスが終了するとき、アルゴリズムが変わるとき、ランキングの循環が作品を埋めるとき——繋がりは消えます。

ECHOは、作品の共鳴が作品自身のものであるべきだという考えから生まれました。それを預けるべきプラットフォームは存在しません。

---

### ECHOが作者に与えるもの

`echo.yaml`を書く行為は、事務作業ではありません。創作行為です。

自分を形づくったものに名前をつけることは、自分の作品をより深く理解することです。影響を宣言することは、自分をより長い物語の中に置くことです——自分より前から存在し、自分の後にも続いていく物語の中に。

ECHOは作者に与えます：

- 「私はここにいた、そしてこれを聴いていた」と言う手段
- プラットフォームではなく、作品と共に移動する記録
- どのアルゴリズムにも推測できない、影響の地図

---

### ECHOが受け手に与えるもの

`echo.yaml`を持つ作品は、招待状です。

受け手はその共鳴を辿ることができます——この小説からあの絵画へ、その絵画から音楽へ、その音楽から四百年前に書かれた詩へ。アルゴリズムが提案したからではなく、作者がそこを指し示したから。

これは最適化による発見ではなく、信頼による発見です。

---

### ECHOが創作文化に貢献するもの

プラットフォームはエンゲージメントを最適化します。エンゲージメントはすでに人気のあるものを報酬として与えます。すでに人気のあるものはより多くの露出を得ます。循環は続きます。

ECHOはこれに反対しません。ただ、別の場所に存在します。

`resonance`リンクから構築された星座はランキングではありません。頂点がない。アルゴリズムがない。作者たちが影響を宣言するにつれて育ち、どこからでも入ることができます。

これはプラットフォームが存在する前の創作文化の姿です——メディアを越え、世紀を越え、言語を越えて、作品が作品と対話していた。ECHOはその対話を再び読めるようにする試みです。

---

### 信頼と偽造について

ECHOには認証の仕組みがありません。`echo.yaml`は誰でも書くことができます。タイムスタンプは改ざんできます。影響は捏造できます。

これは意図的な設計です。

ECHOは信頼を証明しません。信頼を表明します。

表明の重さは、作者とその作品を取り巻くコミュニティの関係が決めます。捏造された`resonance`リンクはECHOを傷つけません——それを書いた作者の信頼を傷つけます。星座はその方向には育ちません。

これは創作文化において信頼が常にそうであり続けた方法です。フェルメールの影響を偽って主張する画家は、信じてもらえません。システムが主張を防いだからではなく、作品がそれを担っていないから。

> ECHOは意図を記録します、事実を記録するのではありません。何を辿るかはコミュニティが決めます。

---

### プラットフォームと独立性について

ECHOはGitHubを必要としません。どんなプラットフォームも必要としません。

`echo.yaml`は個人サーバーに置くことも、ファイルのメタデータの中に埋め込むことも、物理的なオブジェクトの横のNFCタグの中に入れることも、絵画の隣のQRコードの先に置くこともできます。

共有される必要があるのは仕様だけです。ファイルはどこにでも置けます。

これは反プラットフォームではありません。プラットフォーム非依存です。プラットフォームは`echo.yaml`のデータを読み、表示することを歓迎します。ただ、所有することができないだけです。

---

### 名前について

エコーは許可を求めません。

それは何かが聴かれたあとに残るものです——原音に形づくられながら、もはや同一ではない。原音が届かなかった空間へ移動します。他のエコーへと溶け込んでいきます。

創作物も同じです。作者を離れ、受け取った一人ひとりの中で別の何かになります。`echo.yaml`はその外向きの運動の記録です——この作品がどこから来たか、今もなお何と対話しているか、何に届こうとしているか。

---

### 過去の作品と不在の作者について

フェルメールは`echo.yaml`を書けません。紫式部も、コルトレーンも。

だからといって、彼らの作品が星座から排除されるわけではありません。誰かが彼らに代わって、慎重に語る必要があるということです——そして、誰が語っているかを明示しなければなりません。

ECHOは`authored_by`フィールドによって宣言の出所を区別します。

```yaml
echo_version: 1.0
authored_by: curator  # creator / curator / researcher / community
```

`curator`（学芸員・研究者）は過去の作品のために`echo.yaml`を書くことができます。`community`が共同で維持することもできます。このフィールドは資格証明ではありません——開示です。

> 過去の作品はECHOの中で自ら語りません。しかし他者が慎重に代わって語ることができます——誰が語っているかを明示する限りにおいて。

これにより、星座は何世紀にもわたって開かれたまま保たれます。同時に、作者自身の宣言と、他者による解釈の区別が守られます。

---

### story-passportとの関係

[story-passport](https://github.com/sukoyaka-dopeness/story-passport)はECHOの小説特化実装です。日本語タイポグラフィ、ブラウザ拡張リーダー、ルビ・傍点・縦書きのためのMarkdown方言を含みます。

story-passportはECHOが始まった場所です。ECHOはstory-passportが指し示す場所です。
