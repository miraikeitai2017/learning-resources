# 開発フロー
[GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)([日本語訳](https://gist.github.com/Gab-km/3705015))を使用します。

- masterブランチは常にデプロイ可能状態にしておく

- 新しく何か(機能追加、バグ修正...)に取り組む場合、masterからブランチを作成  
  - ブランチ名は`[user-name]/[branch-name]`で作成。(例: `natmark/APIClient` )

- 作成ブランチにローカルでコミットし、サーバ上の同じ名前のブランチにも定期的に作業内容をpushする

- masterへのマージはプルリクエスト経由で行い、masterへの直pushはしない。  
  - プルリクエストを作成後、以下の手順を経てmasterへマージする。  
    - 自動マージのチェックをパスする(コンフリクトがない状態にする)  
    - CIの自動ビルド、自動テストをパスする  
    - 一人以上にコードレビューをしてもらい、OKをもらう。  
    
GitHub Flowについては以下のURLを参考にしてみてください。
- [Github-flowを分かりやすく図解してみた](https://b.pyar.bz/blog/2014/01/22/github-flow/#clone)
- [チームソフトウェア開発のためのワークフロー](https://igaki.gitbooks.io/githubflow-practice/content/pre_github_flow.html)

issueとpull requestの作り方、コードレビューをうけるときのコツについても理解を深めてください。
- [開発フロー研修 @ Wantedly](http://qiita.com/awakia/items/c571e93e96a1ec28044f)
- [初めてコードレビューされる人のためのpull requestとcommitの作り方](http://qiita.com/reikubonaga/items/e3b3b19c14d4ef4efb95)
