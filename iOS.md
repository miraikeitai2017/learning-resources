# iOS Application
ミライケータイプロジェクトのiOSアプリケーションは[Swift](https://swift.org/)を用いて開発します。

## プロジェクトの作り方
[Xcode](https://developer.apple.com/jp/xcode/)という開発ツールを用いてプロジェクトを進めます。  

初めての方はこちらを参考に、アプリを立ち上げてみてください。  
[初心者でも絶対に始められるiPhoneアプリの作り方＆Xcode・シミュレーターの使い方](http://www.atmarkit.co.jp/ait/articles/1601/08/news059.html)

## Xcodeのパーツ名一覧
- [《Xcode入門向け》Xcodeの各部品を一つずつ丁寧に解説してみた](https://blog.codecamp.jp/xcode_function)

## Interface Builder
iOSの画面レイアウト設計はXcodeが提供しているInterface Builderを用いて行います。
`.xib`ファイルや`.storyboard`ファイルをXcodeで開くとInterface Builderが開きます。  
オブジェクトペインからドラッグ&ドロップしたり、インスペクターから値を設定してレイアウトを設計します。

初めての方はこちらを参考に、レイアウトを設計してみてください。  
[初めてiPhoneアプリをデザインするには、どうすればいい？](http://www.atmarkit.co.jp/ait/articles/1602/17/news031.html)

## ライブラリ管理
iOS開発の依存ライブラリを管理するために、`CocoaPods`や`Carthage`といったパッケージマネージャーが使用されています。
### CocoaPodsとCarthageの違い
- [[Swift] CocoaPodsとCarthageの違い / ライブラリ管理](http://qiita.com/nori0620/items/b81ae171f0e82b0c2d8a)
>CocoaPodsは（デフォルトでは）、自動的にアプリケーション用のXcodeのワークスペースと全ての依存関係を作成及び更新を行います。  
>Carthageはframeworkのバイナリをxcodebuildを使ってビルドしますが、プロジェクトへの統合まではせず、統合する作業はユーザに任せます。  
>CocoaPodsのアプローチはユーザにとって使いやすく、一方でCarthage側は柔軟で押し付けがましくないアプローチです。  

CocoaPodsを使うのに比べ、コンパイル時間を短くすることができるため、基本的にはパッケージマネジャーに`Carthage`を使用します。
(一部Objective-C製のライブラリでCocoaPodsにしか対応していないものがあるので、場合によっては`CocoaPods`を併用します。)

### Carthageを使ったライブラリ導入の方法
- [Carthageを使ってビルド時間を短縮しよう](http://qiita.com/yutat93/items/97fe9bc2bf2e97da7ec1)

### CocoaPods導入手法
- [【Swift】CocoaPods導入手順](http://qiita.com/ShinokiRyosei/items/3090290cb72434852460)

## データベース
スマートフォンアプリはモバイルデータベースのRealmをデータベースに使うことが多いです。  
SQLiteなどを使用することもありますが、通常のオブジェクトと同じように扱うことができ、アクセスが高速で、タイプセーフな点からRealmを使うことをオススメします。  
- [Realm](https://realm.io/jp/docs/swift/latest/)

## アーキテクチャ
Appleが推奨しているMVC(Model-View-Controller)パターンを使用する予定です。
iOSの入門書の多くで使用しているのもMVCパターンです。  
[Model-View-Controller - Apple Developer](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/MVC.html)

ただ、ViewControllerの肥大化や役割依存などの問題から、MVC以外のアーキテクチャもiOS開発で用いられています。  
下記のようなアーキテクチャパターンも調べておくとよいかもしれません。

- MVVM (Model-View-ViewModel)  
[MVVMをベースに複雑な振る舞いをしっかり把握できるアプリ開発](http://qiita.com/susieyy/items/2af5321b287b8d2f49f6)

- VIPER (View-Interactor-Presenter-Entity-Router)  
[iOS Project Architecture : Using VIPER [和訳]](http://qiita.com/YKEI_mrn/items/67735d8ebc9a83fffd29)

- Clean Architecture  
[まだMVC,MVP,MVVMで消耗してるの？ iOS Clean Architectureについて](http://qiita.com/koutalou/items/07a4f9cf51a2d13e4cdc)

## リファレンス
### iOS開発
- [Start Developing iOS Apps (Swift)](https://developer.apple.com/library/content/referencelibrary/GettingStarted/DevelopiOSAppsSwift/BuildABasicUI.html#//apple_ref/doc/uid/TP40015214-CH5-SW1)
- [詳細! Swift 3 iPhontアプリ開発 入門ノート (Amazon)](https://www.amazon.co.jp/Swift-iPhone%E3%82%A2%E3%83%97%E3%83%AA%E9%96%8B%E7%99%BA-%E5%85%A5%E9%96%80%E3%83%8E%E3%83%BC%E3%83%88-Swift3-Xcode/dp/4800711487)

### Swiftの文法
- [Swift3.0まとめ -文法- ](http://qiita.com/merrill/items/b3a57acf38afdd3023f0)
- [The Swift Programming Language (Swift 3.1)]( https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/index.html#//apple_ref/doc/uid/TP40014097-CH3-ID0)
- [詳解Swift 第3版 (Amazon)](https://www.amazon.co.jp/dp/4797390530/ref=pd_lpo_sbs_14_t_1?_encoding=UTF8&psc=1&refRID=EQSEVGK1JWBC0GJMDTZ5)
- [Swift実践入門 (Amazon)](https://www.amazon.co.jp/Swift%E5%AE%9F%E8%B7%B5%E5%85%A5%E9%96%80-%E7%9B%B4%E6%84%9F%E7%9A%84%E3%81%AA%E6%96%87%E6%B3%95%E3%81%A8%E5%AE%89%E5%85%A8%E6%80%A7%E3%82%92%E5%85%BC%E3%81%AD%E5%82%99%E3%81%88%E3%81%9F%E8%A8%80%E8%AA%9E-WEB-PRESS-plus/dp/4774187305/ref=pd_sim_14_1?_encoding=UTF8&psc=1&refRID=97VY019VBS3JKCWDHGEG)

### UIKit、Framework関連
- [逆引きSwift(iOS編)](https://sites.google.com/a/gclue.jp/swift-docs/ni-yinki100-ios)
- [iOS-10-Sampler](https://github.com/shu223/iOS-10-Sampler)

### AutoLayout
- [iOSのAuto Layout](http://qiita.com/dearboy15/items/8f55404298954784c8ff)
- [Auto Layoutガイド](https://developer.apple.com/jp/documentation/UserExperience/Conceptual/AutolayoutPG/)

### Unit Test
- [iOS アプリの Unit Test - Swift 編](http://qiita.com/s-harada_i-enter/items/5a8c12b0c456d155ba53#_reference-aa464051adbd73526ffe)
- [QuickでSwiftコードのUnitテストをしよう！](http://grandbig.github.io/blog/2016/01/16/quick/)
- [テストの書き方、Quickの使い方](https://github.com/Quick/Quick/blob/master/Documentation/ja/README.md)

### Libraries
- [awesome-swift](https://github.com/matteocrippa/awesome-swift)
