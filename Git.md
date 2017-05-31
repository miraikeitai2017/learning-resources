# Git

## Gitとは
プログラムのソースコードなどの変更履歴を記録・追跡するための分散型バージョン管理システム

バージョン管理を行う目的
> 1. 以前の状態に戻る  
> 2. 変更履歴を調査する  
> 3. プロジェクトを管理する  
> 4. 変更者と変更理由を知る
>
> "[バージョン管理の目的 - Qiita](http://qiita.com/MasayaMizuhara/items/9503eb66d3125d8c5f41)より引用

分散型と言われる理由
> 共有リポジトリの他に、ローカルPC上にローカルリポジトリを作成します。  
> commitはローカルリポジトリに対して行い、そのcommit内容を共有リポジトリに反映させる(push)仕組みです。  
>
> "[Subversion 対 Git：どちらを使うべきなのか？いろいろな観点から比較してみた](http://tracpath.com/works/development/subversion_vs_git/)より引用

## Gitの勉強用リソース
- [サルでもわかるGit入門](http://www.backlog.jp/git-guide/intro/intro1_1.html)
- [こわくないGit](https://www.slideshare.net/kotas/git-15276118?qid=ad0390a6-d824-4103-a3d8-b30a49cccbb1)
- [いつやるの？Git入門](https://www.slideshare.net/matsukaz/git-28304397?ref=http://www.north-geek.com/entry/git)
- [git-it-electron 実践入門 (前編)](http://ikenji.tech/git/72/)

**ゲーム感覚で勉強できるサイト**
- [LearnGitBranching](http://k.swd.cc/learnGitBranching-ja/)

**みんな大好きドットインストール**
- [git入門 (全22回) - ドットインストール](http://dotinstall.com/lessons/basic_git)

## Gitクライアント
下記のようなアプリケーションを使用することで、GitをGUIで利用することができます。

- [GitHub Desktop](https://desktop.github.com/)  
GitHubの公式Gitクライアント。

- [Source Tree](https://ja.atlassian.com/software/sourcetree)  
Atlassian製のGitクラアント。デファクトスタンダードはおそらくこれ。

- [GitKraken](https://www.gitkraken.com/) [おすすめ]   
axosoft製のGitクライアント。Electron製なので、マルチプラットフォームで利用できる。
デザインが美しく、nodegitを使用しているため、Gitの環境を用意しなくても利用できるのが強み。  
チュートリアル: [learning-GitKraken](http://tracpath.com/bootcamp/learning_git_gitkraken.html)
