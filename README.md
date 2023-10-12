[EB Garamond](https://fonts.google.com/specimen/EB+Garamond) は古風なセリフ体で、なおかつ癖がなく使いやすい。[源流明朝](https://github.com/ButTaiwan/genryu-font)と[源石ゴシック](https://github.com/ButTaiwan/genseki-font)はそれぞれ源ノ明朝と源ノ角ゴシックを加工して古風な印象にしたものだが、自動生成とは思えないほど良く出来ている。[Grenze Gotisch](https://fonts.google.com/specimen/Grenze+Gotisch) はブラックレターでありながら可読性に優れる。[Outfit](https://github.com/Outfitio/Outfit-Fonts)は Keep Calm のパロディをするために似たフォントを探していて見つけた。端正なジオメトリック・サンセリフで、デザインの幅を広げるのに役立つ。[佑字](https://github.com/Kinutafontfactory/Yuji)は珍しいオープンソースの筆文字フォント。[Zen Maru Gothic](https://fonts.google.com/specimen/Zen+Maru+Gothic) は、角ゴシックの加工では出せない雰囲気を持つ本格的な丸ゴシック。[Inter](https://github.com/rsms/inter)は現代的なグロテスク・サンセリフと言うべきもので、Helveticaに似た端正さと可読性の高さを両立させている。ヒューマニストの方が可読性が高いとは限らないことを実感させられた。ただ、Interは大きなサイズだと間延びして見えるので、そういう時は [Public Sans](https://github.com/uswds/public-sans) を代わりに使っている。

[Arimo](https://fonts.google.com/specimen/Arimo)は、多くのオープンソースOSでHelveticaとArialの代替フォントとして使われている。しかし、文字幅に互換性を持たせた上で文字を大きくデザインしたせいで、字間が狭く読みにくいと感じる。他の代替フォントにも同様の問題が見受けられ、システムフォントにするにはふさわしくないと考える。文字幅の互換性を求めるのは印刷やPDFなどに限り、UIやウェブサイトはアクセシビリティの観点から、特定のフォントに依存したデザインを避けるべきだと思う。

# Wineでフォントを代替する
ターミナルで```wine regedit```を実行し、Wine版のレジストリエディタを起動する。```HKEY_CURRENT_USER\Software\Wine\Fonts\Replacements```キー（無ければ作成する）に文字列値を作成し、名前に代替されるフォント名（ＭＳ ゴシックなど）、データに代替するフォント名を入力する。（Wine 6.0.3）

Windowsのシステムフォントと互換性を持たせたオープンソースのフォントはあるが、個人的には互換性より読みやすさを優先して[BIZ UDゴシック](https://github.com/googlefonts/morisawa-biz-ud-gothic)を選んでいる。
