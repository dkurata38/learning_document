# クリーンアーキテクチャ

## まえがき・序文

アーキテクチャとはシステムを形作る、変更コストの大きい重要の設計決定を表したものである。

ソフトウェアとそのアーキテクチャには難しさが3つある。

1. ソフトウェアは構造の数も種類も多様である。
2. ソフトウェアアーキテクチャの本質は目に見えない。
3. 将来の開発者やユーザのニーズを満たす必要がある一方でそれはとても困難である。

将来を予測することは難しいのでソフトウェアの柔軟性を受け入れるところから始まる。

作るソフトウェアやハードウェアが時代によって変化したりしても、アーキテクチャのルールは変わらない。
本書ではそのルールについて記す。

## 第1部

ソフトウェアを動かすのはそれほど難しくないが、ソフトウェアを正しくするのは難しい。
ソフトウェアを正しくすると以下のようなメリットがある。

1. 開発や保守に必要な人がはわずかで済む。
2. 変更が簡単で迅速になる。
3. 欠陥の数が少なくなる。

### 第1章 設計とアーキテクチャ

アーキテクチャと設計はそれぞれ上位レベルと下位レベルの構造や意思決定を指していると一般的に捉えられている。
実際にはアーキテクチャと設計は連続した構造を作っている。
最上位レベルから最下位レベルまで、決定の連続である。

ソフトウェアアーキテクチャの目的は、求められるシステムを最小限のコストで構築・保守するためのものである。
システム構築・保守の生産性は以下のメトリクスを確認する。

1. リリースごとのエンジニア数の増減
2. リリースごとのソースコード行数の増減
3. 1と2をもとにした、リリースごとのコード行あたりのコスト

システム開発では、リリースを急ぐあまりコードをクリーンするのを後回しにしがちである。
実際には、ソフトウェアアーキテクチャと向き合い、クリーンなコードを開発したほうが短期的にも長期的にも生産性が高い。
