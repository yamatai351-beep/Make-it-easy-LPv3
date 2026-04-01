# Make it easy - 5項目ナビゲーション版Webアプリ

学生証認証で安心のマッチングサービス

## 📱 概要

このWebアプリは、学生向けマッチングサービス「Make it easy」の5項目ナビゲーション構成版です。
元の8ページ構成のランディングページを、スマホに最適化された5つのセクションに再構成しました。

## 🎯 5つのナビゲーション項目

### 1. **ホーム（FV）**
- **内容**: 1ページ目のヒーロー部分
- **特徴**:
  - Make it easyロゴとキャッチコピー
  - 学生証認証バッジ
  - メインビジュアル画像
  - 期間限定キャンペーンバナー
  - CTAボタン（登録画面へ遷移）

### 2. **グループ**
- **内容**: 4ページ目の登録済みグループ（メンバー紹介）
- **特徴**:
  - 学生証認証済みメンバーカード
  - 無限スクロールアニメーション（20秒）
  - 大学名、学年、趣味タグ表示
  - 認証バッジ付き

### 3. **登録**
- **内容**: 新規ユーザー登録フォーム
- **特徴**:
  - 8つの入力フィールド:
    1. お名前
    2. メールアドレス
    3. 大学名
    4. 学年（セレクトボックス）
    5. 学生証アップロード（ファイル選択）
    6. プロフィール写真（ファイル選択）
    7. 興味・趣味
    8. 自己紹介（テキストエリア）
  - フォーム送信後、グループ画面へ遷移
  - ファイルアップロード機能付き

### 4. **説明**
- **内容**: 2,3,5,6ページを統合したシステム説明
- **構成**:
  - **MERIT（2ページ目）**: 4つのメリットカード
  - **3つの特徴（3ページ目）**: 学生証認証、マッチング、メッセージ機能
  - **利用の流れ（5ページ目）**: 5ステップの流れ
  - **返金ポリシー（6ページ目）**: 返金対象ケースの詳細
- **特徴**: 縦スクロールで全内容閲覧可能

### 5. **FAQ**
- **内容**: 7,8ページを統合したよくある質問とフッター
- **特徴**:
  - 8つのFAQ項目
  - フッター（ロゴ、リンク、SNSアイコン、コピーライト）
  - 縦スクロールで全内容閲覧可能

## 🎨 デザイン仕様

### カラーパレット
```css
--emerald-400: #34D399
--emerald-500: #10B981  /* メインカラー */
--emerald-600: #059669
--emerald-700: #047857
--blue-500: #3B82F6
--blue-600: #2563EB
--indigo-500: #6366F1
--indigo-600: #4F46E5
--pink-500: #EC4899
--orange-500: #F97316
--slate-50 ~ 900: グレースケール
```

### フォント
- **日本語**: Noto Sans JP (400/500/700/900)
- **ロゴ**: Montserrat (700)

### アイコン
- Font Awesome 6.4.0

### アニメーション
- **ticker**: 20秒の無限スクロール
- **pulse**: 2秒のキャンペーンバナー
- **hover effects**: translateY(-5px) + box-shadow

### レスポンシブ
- **最適化幅**: 430px × 932px（スマホ画面）
- **固定ナビゲーション**: 画面下部に固定（80px高さ）

## 🚀 使い方

### ローカル環境での実行

1. **ファイルを開く**
   ```bash
   # ブラウザで直接開く
   open index.html

   # または、ファイルをダブルクリック
   ```

2. **ローカルサーバーで実行（推奨）**
   ```bash
   # Python 3の場合
   python -m http.server 8000

   # Python 2の場合
   python -m SimpleHTTPServer 8000

   # Node.jsの場合
   npx http-server
   ```

   その後、ブラウザで `http://localhost:8000` にアクセス

### デプロイ方法

#### GitHub Pagesへのデプロイ

1. GitHubリポジトリを作成
2. ファイルをプッシュ
   ```bash
   git init
   git add index.html README.md
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/username/repo.git
   git push -u origin main
   ```
3. リポジトリ設定 → Pages → Source: main branch → Save
4. `https://username.github.io/repo/` でアクセス可能

#### Netlify Dropへのデプロイ

1. [Netlify Drop](https://app.netlify.com/drop)にアクセス
2. `index.html`をドラッグ&ドロップ
3. 即座にデプロイ完了！

#### Vercelへのデプロイ

1. [Vercel](https://vercel.com)にログイン
2. 「New Project」をクリック
3. GitHubリポジトリをインポート、またはファイルをアップロード
4. デプロイ

## 🔧 カスタマイズ

### 画像の変更
```html
<!-- Hero画像 -->
<img src="https://page.gensparksite.com/slides_images/e73023cb177b6c993bbb3f3376bb2cd1.webp" 
     alt="Make it easy Hero Image" 
     class="hero-image">
```

### カラーテーマの変更
```css
:root {
    --emerald-500: #10B981;  /* メインカラー */
    --blue-500: #3B82F6;     /* アクセントカラー */
}
```

### メンバーカードの追加
```html
<div class="member-card">
    <div class="member-header">
        <div class="member-avatar">E</div>
        <div class="member-info">
            <h3>新しいメンバー</h3>
            <p>○○大学 2年</p>
        </div>
    </div>
    <div class="verified-badge">
        <i class="fas fa-check-circle"></i>
        学生証認証済み
    </div>
    <div class="member-tags">
        <span class="tag">趣味1</span>
        <span class="tag">趣味2</span>
    </div>
</div>
```

## 📋 技術スタック

- **HTML5**: セマンティックマークアップ
- **CSS3**: 
  - Flexbox/Grid レイアウト
  - CSS Variables（カスタムプロパティ）
  - Animations & Transitions
  - Media Queries
- **JavaScript（Vanilla）**: 
  - DOM操作
  - イベントハンドリング
  - セクション切り替えロジック
- **外部ライブラリ**:
  - Google Fonts（Noto Sans JP, Montserrat）
  - Font Awesome 6.4.0

## 🎯 主要機能

### 1. セクション切り替え
```javascript
function showSection(sectionId) {
    // 全セクションを非表示
    document.querySelectorAll('.section').forEach(section => {
        section.classList.remove('active');
    });

    // 選択されたセクションを表示
    document.getElementById(sectionId).classList.add('active');

    // ナビゲーションのアクティブ状態を更新
    document.querySelectorAll('.nav-item').forEach(item => {
        item.classList.remove('active');
        if (item.getAttribute('data-section') === sectionId) {
            item.classList.add('active');
        }
    });
}
```

### 2. フォーム送信処理
```javascript
function handleRegister(event) {
    event.preventDefault();
    alert('✅ 登録が完了しました！');
    showSection('groups');  // グループ画面へ遷移
}
```

### 3. ファイルアップロードプレビュー
```javascript
document.getElementById('student-id-file').addEventListener('change', function(e) {
    if (e.target.files.length > 0) {
        const fileName = e.target.files[0].name;
        e.target.parentElement.querySelector('p').textContent = `選択済み: ${fileName}`;
    }
});
```

## 📱 動作確認済み環境

### ブラウザ
- ✅ Google Chrome（最新版）
- ✅ Safari（最新版）
- ✅ Firefox（最新版）
- ✅ Microsoft Edge（最新版）

### デバイス
- ✅ iPhone（iOS 14+）
- ✅ Android（Android 10+）
- ✅ デスクトップ（Chrome DevToolsのモバイルビュー）

## 🐛 トラブルシューティング

### アニメーションが動かない
- **原因**: ブラウザの省電力モード
- **解決**: デベロッパーツールで`prefers-reduced-motion`を無効化

### ファイルアップロードが反応しない
- **原因**: JavaScriptの読み込みエラー
- **解決**: ブラウザのコンソールでエラーを確認

### 画像が表示されない
- **原因**: ネットワーク接続の問題
- **解決**: インターネット接続を確認

### ナビゲーションボタンが効かない
- **原因**: JavaScriptの実行エラー
- **解決**: ブラウザのコンソールでエラーを確認、キャッシュをクリア

## 📄 ライセンス

© 2024 Make it easy. All rights reserved.

## 📞 お問い合わせ

- **サポート窓口**: support@makeiteasy.example.com
- **公式サイト**: https://makeiteasy.example.com

---

**開発者向けメモ**:
- 単一HTMLファイル構成（依存関係なし）
- CDNを使用（フォント、アイコン）
- モバイルファースト設計
- アクセシビリティ対応（セマンティックHTML、適切なARIA属性）
