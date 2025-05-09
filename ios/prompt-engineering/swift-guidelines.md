# Swift コード生成のためのプロンプトエンジニアリングガイドライン

このドキュメントでは、AIを使用してSwiftコードを生成する際の効果的なプロンプト作成のガイドラインを提供します。

## 基本原則

1. **具体的な要件を提示する**
   - 実装したい機能を明確に説明する
   - 使用するフレームワーク（UIKit、SwiftUI、Combine等）を指定する
   - ターゲットのiOSバージョンを明記する

2. **コンテキストを提供する**
   - 既存のプロジェクト構造について説明する
   - 使用している依存関係やライブラリを列挙する
   - 既存のデータモデルやアーキテクチャパターン（MVVM、Clean Architecture等）について説明する

3. **具体的な出力形式を指定する**
   - 完全なクラスまたは構造体の実装を求める
   - 特定のメソッドやプロパティのみを求める
   - ユニットテストの生成を求める

## プロンプト例

### 良いプロンプト例

```
SwiftUIを使ってiOS 15以上で動作するToDo管理アプリのメイン画面を実装してください。
以下の機能が必要です：
- ToDoリストの表示（タイトル、期限日、完了/未完了ステータスを含む）
- 新しいToDoアイテムの追加機能
- スワイプでの削除機能
- 完了時のチェックマーク機能

アーキテクチャはMVVMを使用しています。CoreDataをデータストレージとして使用します。
既存のToDoアイテムのモデルは以下の構造になっています：
```swift
struct TodoItem: Identifiable {
    let id: UUID
    var title: String
    var dueDate: Date
    var isCompleted: Bool
}
```
```

### 悪いプロンプト例

```
SwiftでToDoアプリを作ってください。
```

## Swiftに特化したプロンプトテクニック

1. **メモリ管理の指定**
   - 参照サイクルを避けるための弱参照（weak self）などの要件を明記する
   - ARC（自動参照カウント）の動作に関する懸念点を説明する

2. **非同期処理の明確化**
   - async/awaitを使用するか、Combinationやクロージャベースの非同期処理を使用するかを指定する
   - エラーハンドリングの方法を明記する

3. **UIライフサイクルの考慮**
   - ViewControllerまたはSwiftUI Viewのライフサイクルイベントでの処理を明記する
   - メモリ警告やバックグラウンド遷移時の動作を指定する

## プロンプトテンプレート

### SwiftUI画面実装テンプレート

```
以下の要件に基づいて、SwiftUIで[画面の目的]を実装してください：

機能要件：
- [機能1]
- [機能2]
- [機能3]

UI要件：
- [UIコンポーネント1]
- [UIコンポーネント2]
- [UIコンポーネント3]

技術的制約：
- iOS [バージョン]以上をサポート
- [アーキテクチャパターン]を使用
- [データストレージ方法]を使用

関連するモデル：
```swift
[モデル定義]
```

その他の注意点：
- [注意点1]
- [注意点2]
```

## 注意事項

- 生成されたコードは常に手動でレビューし、ベストプラクティスに従っていることを確認してください
- 特にセキュリティに関わる機能（認証、データ暗号化等）では、生成されたコードを慎重に検証してください
- Apple特有のガイドラインやベストプラクティスに従っていることを確認してください