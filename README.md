## Advent Calender遅刻いい訳
1. 年末忙しすぎた
2. ネタと期待していたいくつかがまともに結果が出ずに苦しい思いをしていた
3. 元URLの喪失

## バイト列から文字コーディングを推定する

Twitterで時々バズるネタとして、機械学習がこれほどもてはやされるのに、今だにBrowserは時々文字化けし、ExcelはUTF8を突っ込むと文字化けし、到底、文化的で咲い
最低限の人権が保護された状態ではありません。  


その度、「それ、できると思うよ」って言い返していたのですが、実証実験を行いたいと思います。  

## なんの機械学習アルゴリズムがいいか
ニュースサイトをスクレイピングすると、大量のUTF8のテキスト情報が取得できます  

このテキスト情報をもとに、nkfというコマンドで、euc, sjisの文字コードに変換して、様々な文字コードのバージョンを作ります  

Pythonやいくつかの言語では、UTF8以外を扱うとバグるのですが、バイト列としてみなすと読み込みが可能になり、バイト列にはなんらかの特徴が見て取れそうです（仮説）  

バイト列をベクトル化して、CNNのテキスト分類の機械学習で分類することが良さそうです  


## ネットワーク
VGGのネットワークを参考に編集しました。

<div align="center">
  <img width="200px" src="https://user-images.githubusercontent.com/4949982/34658318-57ee45fc-f471-11e7-8e4a-7a742e1e3f2b.png">
</div>
