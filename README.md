# プロキシ経由で docker を使うためのパッチ
Docker でプロキシのダイジェスト認証(Proxy-Authentication: Digest Access Authentication)を使えるようにするパッチです。

## Build
Docker コンテナをビルド環境として使います。普通に Docker が使える環境でビルドしてください。

1. プロキシ対応した go Docker イメージをビルドしてください。 https://github.com/yutakimura-monex/go
2. make
3. bundles ディレクトリにバイナリが出力されます。利用環境に配備して使用してください。

## 補足事項
- 15GB程度のディスク容量が必要です。
- Go言語の net/http をダイジェスト認証プロキシに対応させたSDKを使います。
- tag v20.10.5 から派生した main ブランチを使用しています。
