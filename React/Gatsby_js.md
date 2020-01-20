
## GatsbyJsって?
- React製の静的サイトジェネレータ
- 高度なパフォーマンス最適化をよしなにやってくれる
- Webpackなどの煩雑な設定を隠蔽、Web制作を楽に
- JAMStackの申し子

## 早い!
- starter(Pull Requestで誰でも追加できる)
- theme(Wordpressにあるような機能)
- 静的サイトならではのデプロイの簡単さ
- PWA対応などがプラグインですぐに出来る

## うまい!!!
- データを取得する操作はGraphQLで統一
- 内部の状態管理にReduxを利用(外からは意識しなくていい)
- mdx, Server Side Renderingの考え方


## 環境構築
### エラー
```
Error in "/home/workspace/node_modules/gatsby-transformer-sharp/gatsby-node.js": 'darwin-x64' binaries cannot be used on the 'linuxmusl-x64' platform. Please remove the 'node_modules/sharp/vendor'
```

node_modules/sharpを削除してから再度`yarn install`


## 参考サイト
[公式ページ](https://www.gatsbyjs.org/)
