# agorack-handbook

Agorack と、Agorack がつなぐ部品（文之助・drive-logger）について、設計の考え方・開発の経緯・仕組みとロジックをまとめた解説のリポジトリです。

コードはありません。各システムのコードと、開発のための文書（設計書・決めごとの記録・手順）は、それぞれのリポジトリにあります。このリポジトリは、3つをまたいで「なぜこう作ったか」「中で何が起きているか」を理解するための読み物です。

| システム | 役目 | リポジトリ |
|---|---|---|
| Agorack | 部品を MCP で呼び分けて、利用者の質問に根拠付きで答えるチャット（親） | [abeouga/agorack](https://github.com/abeouga/agorack) |
| 文之助 | 紙の帳票を写真から読み取り、人が確定した値だけを Excel・検索・MCP に出す（部品） | [abeouga/fuminosuke](https://github.com/abeouga/fuminosuke) |
| drive-logger（カブロガー） | バイクに付けた機器で位置と振動を記録し、クラウドで処理して地図で振り返る（部品） | [abeouga/drive-logger](https://github.com/abeouga/drive-logger) |

## 置き場所

| 場所 | 中身 |
|---|---|
| [`overview/`](overview/) | 3つの関係、3つに共通する設計の考え方、開発の経緯 |
| [`agorack/`](agorack/) | Agorack の解説 |
| [`fuminosuke/`](fuminosuke/) | 文之助の解説 |
| [`drive-logger/`](drive-logger/) | drive-logger の解説 |

## 読む順番

1. [3つのシステムの関係](overview/01-3つのシステムの関係.md)
2. [共通の設計の考え方](overview/02-共通の設計の考え方.md)
3. [開発の経緯](overview/03-開発の経緯.md)
4. 知りたいシステムの `01-全体像.md` から番号の順に読む

各システムの解説は、番号の小さいものほど全体の話、大きいものほど細かい仕組みと、できないこと・分かっている問題です。

## 書き方の決まり

- 事実は、各リポジトリのコード・文書・Issue・PR で確かめたものだけを書く。確かめられなかったことは「未確認」と書く。
- 出どころ（元のリポジトリのファイル名と節、Issue・PR の番号）を括弧で添える。
- ファイルのパスと Issue・PR の番号は、そのフォルダーのシステムのリポジトリのもの（`agorack/` なら abeouga/agorack）。`overview/` では、リポジトリの名前を付けて書く。このリポジトリ自身では Issue・PR を使わない。
- 元のリポジトリの決めごとの記録を写し直さず、要点と理由を書いて、元の文書へリンクする。
- 図は Mermaid で書く。
- 数字や状態は、書いた日の時点のもの。元のリポジトリが変わったら、こちらも直す。
