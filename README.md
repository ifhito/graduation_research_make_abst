
# 卒業研究で使った文章要約コード

## 要約アルゴリズム

中で書かれている要約アルゴリズムはLexRank、SemanticVolume、TopicRank

LexRankは[このサイト](https://qiita.com/riverwell/items/310e0a31f2e5097df7ff)、SemanticVolumeは[このサイト](https://qiita.com/m__k/items/fc6f28b3b7ca7fdea162)のコードをほぼパクった。

TopicRankは以下の二つの論文を元に上記のLexRankのコードを書き換えている

[「潜在的トピックの類似度グラフに基づく要約文生成」](https://anlp.jp/proceedings/annual_meeting/2012/pdf_dir/F4-6.pdf)

[「トピックを考慮したグラフによる複数文書要約への一考察」](https://www.anlp.jp/proceedings/annual_meeting/2013/pdf_dir/A5-4.pdf)

## MMR

要約文を最適化するためにMMRのアルゴリズムを書いており、LexRankとTopicRankには適応した。(TopicRankは前述の論文に書かれているMMRを使用した、LexRankに使用したMMRは書籍「言語処理のための機械学習入門」内のアルゴリズムを参考にした)

## 要約文の変換

研究では要約文の変換を行なった。そのため、以下のように要約文を変換するコードが含まれている。(不完全な変換であるため参考にしない方が良い)

- 敬語文変換 - 文末をですます調に変換
- 話し言葉変換 - 論文「学生のレポートにおける話し言葉とその出現傾向」の話し言葉変換表に準じた変換と、文末に「よ」を追加
- 話し言葉と絵文字変換 - 話し言葉に変換した文中に「長岡技術科学大学 自然言語処理研究室日本語感情表現辞書」内の感情語が含まれていた場合、その感情後の直後に対応の絵文字を挿入する。

## その他

適当に読んで

