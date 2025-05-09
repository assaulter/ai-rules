# Cursor用 Swift/iOSプロンプトテンプレート集

このドキュメントでは、Cursor IDEでiOSアプリ開発を効率化するためのプロンプトテンプレートを提供します。これらのテンプレートをカスタムプロンプトとして登録して活用できます。

## 基本的なコード生成

### SwiftUIビュー作成

```
以下の要件に基づいて、SwiftUIでの【画面名】ビューを実装してください：

機能要件：
- 【機能1】
- 【機能2】
- 【機能3】

UI要件：
- 【UIコンポーネント1】
- 【UIコンポーネント2】

アーキテクチャ: MVVM
iOS対応バージョン: 15以上
使用するフレームワーク: SwiftUI, Combine

必要に応じて以下のモデルを使用します：
```swift
【モデル定義】
```

コードには適切なコメントを含め、SwiftUIのベストプラクティスに従ってください。
```

### UIKit ViewController作成

```
以下の要件に基づいて、UIKitでの【画面名】ViewControllerを実装してください：

機能要件：
- 【機能1】
- 【機能2】
- 【機能3】

UI要件：
- 【UIコンポーネント1】
- 【UIコンポーネント2】

レイアウト方法: Auto Layout（コードで実装）
アーキテクチャ: MVC（または指定のアーキテクチャ）
iOS対応バージョン: 13以上

以下のプロトコルを実装する必要があります：
- 【プロトコル1】
- 【プロトコル2】

メモリリークを防ぐために適切な参照管理を行い、UIライフサイクルメソッドを適切に実装してください。
```

## アーキテクチャパターン

### MVVMパターン実装

```
以下のモデルに基づいて、MVVMパターンに従った完全な実装を提供してください：

モデル：
```swift
struct 【モデル名】 {
    【プロパティ定義】
}
```

必要な機能：
1. 【機能1】
2. 【機能2】
3. 【機能3】

必要なコンポーネント：
- Model: 上記のデータモデル
- ViewModel: モデルを操作し、ビューに表示するデータを準備
- View (SwiftUI): ViewModelを監視し、UIを更新

Combine（または他の指定のリアクティブフレームワーク）を使用したバインディングを実装してください。
```

### クリーンアーキテクチャ実装

```
以下の機能のためのクリーンアーキテクチャ実装を提供してください：

機能概要：【機能の簡潔な説明】

以下のレイヤーを実装してください：
1. Domain Layer:
   - Entities: 【エンティティの説明】
   - Use Cases: 【ユースケースの説明】
   - Repository Interfaces: 【リポジトリインターフェースの説明】

2. Data Layer:
   - Repository Implementation: 【リポジトリ実装の説明】
   - Data Sources: 【データソースの説明】
   - DTOs/Mappers: 【DTOの説明】

3. Presentation Layer:
   - ViewModels/Presenters: 【ViewModelの説明】
   - Views: 【Viewの説明】

依存性注入の方法も含めて実装してください。
```

## 特定機能の実装

### ネットワーキング

```
以下のAPIエンドポイントのためのネットワーキングレイヤーを実装してください：

エンドポイント: 【エンドポイントURL】
メソッド: GET/POST/PUT/DELETE
ヘッダー:
- 【ヘッダー1】: 【値1】
- 【ヘッダー2】: 【値2】

リクエストモデル:
```swift
struct 【リクエストモデル名】: Codable {
    【プロパティ定義】
}
```

レスポンスモデル:
```swift
struct 【レスポンスモデル名】: Codable {
    【プロパティ定義】
}
```

使用するネットワークライブラリ: URLSession / Alamofire
エラーハンドリング: 適切なエラーモデルとハンドリング方法を実装
非同期処理: async/await または Combine を使用
```

### Core Data統合

```
以下のエンティティに対するCore Dataの完全な実装を提供してください：

エンティティ名: 【エンティティ名】
属性:
- 【属性名1】: 【型】, 【オプション/必須】, 【制約】
- 【属性名2】: 【型】, 【オプション/必須】, 【制約】

リレーションシップ:
- 【リレーションシップ名1】: 【対象エンティティ】, 【カーディナリティ】, 【削除ルール】
- 【リレーションシップ名2】: 【対象エンティティ】, 【カーディナリティ】, 【削除ルール】

以下のCRUD操作を実装してください：
- 作成
- 読み取り（単一/複数/検索）
- 更新
- 削除

また、NSFetchedResultsControllerまたはPublisherを使用した変更監視機能も実装してください。
```

## テストとデバッグ

### ユニットテスト作成

```
以下のクラス/メソッドに対するXCTestを使用した完全なユニットテストを作成してください：

テスト対象:
```swift
【テスト対象のコード】
```

テストすべき条件：
1. 【テストケース1】
2. 【テストケース2】
3. 【テストケース3】

モックが必要なプロトコル：
- 【プロトコル1】
- 【プロトコル2】

テストでは、適切なアサーションとエラーメッセージを使用し、セットアップと後処理を適切に実装してください。
```

### デバッグヘルパー作成

```
以下の問題をデバッグするためのヘルパーユーティリティを作成してください：

問題の種類: 【メモリリーク/クラッシュ/パフォーマンス/その他】
問題の詳細: 【問題の詳細な説明】

必要な機能：
1. 【機能1】
2. 【機能2】
3. 【機能3】

デバッグ情報は適切にフォーマットしてコンソールに出力し、必要に応じてファイルに保存できるようにしてください。
```

## UI/UX改善

### アクセシビリティ強化

```
以下のコードにアクセシビリティ機能を追加してください：

```swift
【元のコード】
```

以下のアクセシビリティ機能を実装してください：
1. VoiceOver対応（適切なラベルと説明）
2. Dynamic Type対応
3. 適切なコントラスト比の確保
4. キーボードナビゲーション（UIKitの場合）

アクセシビリティインスペクタでのテスト方法も記述してください。
```

### アニメーション追加

```
以下のUIコンポーネントに自然で滑らかなアニメーションを追加してください：

```swift
【元のコード】
```

以下のイベントにアニメーションを追加：
1. 【イベント1】: 【期待するアニメーション】
2. 【イベント2】: 【期待するアニメーション】

アニメーションの要件：
- 期間: 【秒数】秒
- タイミングカーブ: イーズイン/イーズアウト/その他
- 中断可能: はい/いいえ

パフォーマンスを考慮し、過度なGPU/CPU使用を避けるようにしてください。
```

## プロジェクト設定

### SwiftPackageの作成

```
以下の機能を持つSwift Packageを作成してください：

パッケージ名: 【パッケージ名】
説明: 【パッケージの簡潔な説明】

提供する機能：
1. 【機能1】
2. 【機能2】
3. 【機能3】

依存関係：
- 【依存パッケージ1】: 【バージョン】
- 【依存パッケージ2】: 【バージョン】

公開インターフェース：
- 【クラス/構造体/プロトコル1】
- 【クラス/構造体/プロトコル2】

サポートするプラットフォーム: iOS 【バージョン】以上, macOS 【バージョン】以上, etc.
Swiftバージョン: 【バージョン】以上

README.mdとドキュメントコメントを含めてください。
```

### アプリパフォーマンス最適化

```
以下のコードをパフォーマンス観点で最適化してください：

```swift
【元のコード】
```

以下の観点から最適化を行ってください：
1. メモリ使用量
2. CPU使用率
3. バッテリー消費
4. 応答性と滑らかさ

最適化前後でのパフォーマンス比較予測と、使用した最適化テクニックの説明を含めてください。
```

## プロジェクト管理

### 技術的負債クリーンアップ

```
以下のコードの技術的負債を特定し、リファクタリングしてください：

```swift
【元のコード】
```

以下の観点からリファクタリングを行ってください：
1. コードの重複排除
2. 命名の改善
3. 責任の分離
4. 不要なコードの削除
5. 最新のSwift機能の活用

リファクタリング前後の比較と、各変更点の根拠を説明してください。
```

### コードレビュー

```
以下のコードをレビューし、問題点と改善提案を提供してください：

```swift
【レビュー対象コード】
```

以下の観点からレビューしてください：
1. コーディング規約準拠
2. パフォーマンス
3. メモリ管理
4. エラー処理
5. セキュリティ
6. テスト容易性
7. 保守性

それぞれの問題に対して具体的な改善提案を提示してください。
```

## ドキュメント作成

### APIドキュメント

```
以下のクラス/メソッドに対する完全なドキュメントコメントを作成してください：

```swift
【コード】
```

以下の要素を含めたSwift形式のドキュメントコメントを作成してください：
1. 概要説明
2. 詳細説明
3. パラメータ説明
4. 戻り値説明
5. スローされる例外の説明
6. 使用例
7. 注意事項
8. SeeAlsoリンク

ドキュメントはDoxygenまたはSwift-DocCに準拠するフォーマットにしてください。
```