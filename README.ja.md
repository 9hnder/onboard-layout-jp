# Onboard カスタムファイル 日本語キーボードレイアウト (OADG 109A Full Keyboard)

<img width="1055" height="312" alt="Image" src="https://github.com/user-attachments/assets/a84fe190-90e9-4e02-a569-9b0af0655b25" />
<img width="1055" height="312" alt="Image" src="https://github.com/user-attachments/assets/8e0d3c00-3446-4685-9cac-29f9fcd045f5" />

## :: 概要 ::

オンスクリーン・キーボード [Onboard](https://github.com/onboard-osk/onboard) のレイアウト定義カスタム・ファイルです。
日本語キーボード(OADG109A / JIS X 4064 に準拠)のレイアウトを再現しています。

これは "Linux Mint 22.3 Zena" の `/usr/share/onboard/layouts/` ディレクトリにある `Full Keyboard*` 、および `Compact*` ファイルをコピーしてカスタマイズしたものです。
それらと差分を取ることで、どこが改造されているのか調べることができます。

```console:
    ## e.g.:
    $ diff layouts/OADG109A_Full_Keyboard.onboard /usr/share/onboard/layouts/Full\ Keyboard.onboard
```

日本語環境がセットアップされた Linux デスクトップ環境が必要になります。


## :: インストール方法 ::

### >> 開発者向け

`git clone` コマンドでこのリポジトリを複製してください。
`layout` ディレクトリが作られますので、それを Onboard が解釈できる XDG 準拠のディレクトリへ置くだけです。
以下のコマンドでユーザーのホーム・ディレクトリにインストールできます:

```console:
    $ git clone https://github.com/9hnder/onboard-layout-jp.git
    $ mkdir -p ~/.local/share/onboard/
    $ cp -r onboard-layout-jp/layouts  ~/.local/share/onboard/
```

`theme` ディレクトリについてはデザインのみですので、お好みでどうぞ。
その場合 `fonts-migmix` フォントパッケージが必要です。もしくは `Nightshade.theme` を適切なフォントに書き換えてください。
フォントによってはグリフ バックスラッシュ `\` が 円記号 `¥` で表示されたりしますので、明確にそれらが区別できる `MigMix 1M`, `Migu 1M`, `Migu 1C`, `Source Code Pro` などのソースコード用フォントの使用をおすすめします。

⚠️ 警告 ⚠️  
もし、 `key_defs.xml` を既に改造してある場合は手動でマージしてください。

### >> 非開発者向け

1. GitHub の GUI から ZIP ファイルをダウンロードしてください。
2. ダウンロードされた `onboard-layout-jp-master.zip` を解凍します。
3. 全てのファイルを `~/.local/share/onboard/` ディレクトリに移動します。


## :: 使用方法 ::

インストールしたら Onboard が既に起動している場合は一度終了させ、起動し直します。
その後、 Onboard の設定画面を出して *[レイアウト] > [My Layouts] > [OADG109A_Full_Keyboard]* を選んでください。

CLI で試す場合は:

```console:
    $ pkill onboard
    $ onboard-settings
    -- (レイアウトに "OADG109A_Full_Keyboard" を設定する。または onboard -l を使ってください) --
    $ onboard &
```


## :: ライセンス ::

本家に倣い、以下となります。ライセンスを遵守していれば改変・再配布は自由です。

[GPL-3+](https://www.gnu.org/licenses/gpl.txt)

オリジナルとの差分部分にのみ、以下の者が著作権を有します。

© Ken Shirakawa (9hnder)
Since: 2026-04-18 - 2026-05-12


## :: 免責事項 ::

本設定を用いて、万が一不具合が起きた場合でも筆者は責任を負いません。
自己責任にてご利用ください。


## :: テスト環境 ::

筆者のテスト環境は以下です。仮想環境ではなく実機。... maybe.
neofetch コマンドの結果になります。

    OS: Linux Mint 22.3 x86_64
    Kernel: 6.17.0-19-generic
    Shell: bash 5.2.21
    Resolution: 2400x1600
    DE: Cinnamon 6.6.7
    WM: Mutter (Muffin)
    WM Theme: Mint-Y-Dark-Red (Mint-Y)
    Theme: Mint-Y-Dark-Red [GTK2/3]
    Icons: Mint-Y-Red [GTK2/3]
    Terminal: gnome-terminal
    CPU: Intel Pentium 4415Y (4) @ 1.600GHz
    GPU: Intel HD Graphics 615

    Onboard: 1.4.1+mint4+willma (base on 1.4.1-5ubuntu6)


## :: 参考 ::

制作に当たり、以下のWebページを参考にさせていただきました。感謝します。

[ぼちぼち書くブログ](https://mypace.sasapurin.com/entry/impossible-input-underscore-onboard/)

また、キートップのフォントを変更したい場合や Super キーの表記を変えたい場合は以下のページが参考になります。

[kledgeb](https://kledgeb.blogspot.com/2014/06/ubuntu-onboard-17.html)


## :: 筆者について ::

関連記事は以下で公開しています。

[Qiita ユーザーページ](https://qiita.com/9hnder/)

**Sorry, dear foreign friends! Only Japanese articles. DW.**


## :: 謝辞 ::

参考サイト、並びに Onboard の開発者たちに感謝します。
素晴らしいソフトウェアをありがとう！

<!-- vim:set ts=4 tw=0 ff=unix ft=markdown : This is vim modeline -->

