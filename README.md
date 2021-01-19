<img src="src/Resouces/LiwingIcon.png" width="64">

This README is written in English and Japanese.

この README は、英語と日本語で記します。

# Liwing
Liwing is a tool that allows you to click on a UNC path link in Slack to open a file directly.  
For example, if you post the link to an Excel file path called `\\servername\test.xlsx` to Slack, all you have to do is click on the link and Excel will open the file.

Liwingとは、Slack で UNCパスのリンクをクリックして直接ファイルが開けるようになるツールです。  
例えば、`\\servername\test.xlsx` というExcelファイルパスのリンクを Slack に投稿すると、そのリンクをクリックするだけで Excel を起動してそのファイルを開きます。


## Basic Usage (基本的な使い方)

### How to install (インストール方法)
Download and install LiwingSetup.msi from the link below, it is a Windows-only tool.  

以下のリンクから LiwingSetup.msi をダウンロードしてインストールしてください。Windows専用のツールです。 

[LiwingSetup.msi](https://github.com/kojimadev/Liwing/raw/master/src/ReleaseProduct/LiwingSetup.msi)

If the window shown below appears when running the installer, click the [More Info] link and then click the [Run] button.

インストーラの実行時に下図のウィンドウが表示された場合は、[詳細情報]リンクをクリックした上で[実行]ボタンを押してください。

<img src="images/install1.png" width="333">
<img src="images/install2.png" width="333">

### How to post a link to Slack (Slackにリンクを投稿する方法)
For example, if you want to create a link to a file path of  `\\servername\test.xlsx`, select that file and run the menu Send-Liwing in the context menu of Explorer.  
(Installing Liwing will add the Send menu.)

例えば、`\\servername\test.xlsx` のファイルパスのリンクを作成したい場合、そのファイルを選択して、エクスプローラーのコンテキストメニューの [送る] - [Liwing] というメニューを実行します。  
(Liwingをインストールすることで、[送る]メニューが追加されます)  

![image.png](Images/SendToMenu.png)  

When you do the above, a URL called `lw://file/servername/test.xlsx` is copied to the clipboard, using a custom URL scheme.  
When you post the URL to Slack, it will appear as a link as shown below.

上記を実行すると、クリップボードに `lw://file/servername/test.xlsx` というカスタムURLスキームという技術を用いた形式のURLがコピーされます。  
そのURLをSlackに投稿すると、下図のようにリンク形式で表示します。

![image.png](Images/SlackPost.png)

### How to open the target file (対象のファイルを開く方法)
Click on the link that starts with "lw:" above, and the following dialog will appear.  
If you select Open Link here, it will open the target file. If the file has the xlsx extension, start Excel (start with the default application per extension).  

上記の「lw:」から始まるリンクをクリックすると、下図のダイアログが表示されます。  
ここで[リンクを開く]を選択すれば、対象のファイルを開きます。ファイルがxlsxの拡張子であれば、Excelを起動します(拡張子ごとの既定のアプリケーションで起動します)。  

![image.png](Images/OpenFile.png)

## Convenient Usage (便利な使い方)

## Install Liwing on all team members (チーム全員でLiwingをインストール)
In order to open links with custom URL schemes starting with "lw:", Liwing must be installed.
Therefore, if your team is storing files in UNC paths on the network, it is useful to have Liwing installed by all team members.

「lw:」から始まるカスタムURLスキームのリンクを開くためには、Liwingのインストールが必要です。
従って、ネットワーク上のUNCパスにファイルを格納しているチームの場合、チーム全員がLiwingをインストールしておくと便利です。

## Copy the URLs of multiple files (複数ファイルのURLをコピー)
You can copy the URLs of multiple files to the clipboard by selecting them in Explorer and executing the [Send] - [Liwing] menu.

エクスプローラーで複数ファイルを選択して [送る] - [Liwing] メニューを実行すれば、複数ファイルのURLをクリップボードにコピーします。

## Use for html files (htmlファイルに利用)
In addition to pasting into Slack, you can also use it to link html files.
Normally, you cannot open a file with UNC path directly from a browser, but you can create a link to open a file with UNC path from a browser by writing the URL copied by Liwing in the link path as follows.  
` (例) <a href="lw://file/servername/test.xlsx">test.xlsx</a>`

Slackに貼り付けるだけでなく、htmlファイルのリンクにも利用できます。
通常はブラウザからUNCパスのファイルを直接開くことはできませんが、以下のようにLiwingでコピーしたURLをリンク先パスに書くことで、ブラウザからUNCパスのファイルを開くリンクを作成できます。  
` (例) <a href="lw://file/servername/test.xlsx">test.xlsx</a>`

## Use for links to open local files (ローカルのファイルを開くリンクに利用)
It can be used to link not only UNC paths but also local paths (such as C: drive).
Therefore, if all team members have the same local path to clone GitHub repository, you can create a link to open the target document directly from Slack.  
(e.g.) If everyone on the team has cloned the target repository to drive L, the following link will open the target file.  
`lw://file/L:/docs/DesignDocuments/FeatureDesign.md`

UNCパスだけでなく、ローカルのパス(C:ドライブなど)のリンクにも利用できます。
従って、GitHubのリポジトリをクローンするローカルのパスをチーム全員で統一すれば、Slackから対象ドキュメントを直接開くリンクが作成できます。  
(例) チーム全員がLドライブに対象リポジトリをクローンしていた場合、以下のリンクで対象ファイルを開く。  
`lw://file/L:/docs/DesignDocuments/FeatureDesign.md`

## Support
Have a question? Come and talk to me: [@kojimadev](https://twitter.com/kojimadev)

## License
Liwing is released under the MIT license.