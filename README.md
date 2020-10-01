# Release機能のチェック

## GitHubのRelease機能

### 手順

1. リポジトリのCodeページを開く
2. 右側のReleaseボタン押下(Releaseページに遷移)
3. Draft new release押下
4. "Tag version"と"Releaseするbranch"を指定
5. Publish release押下

### 結果

- Releaseページに角丸で"Release"とマークされる
- "Releaseするbranch"に対してTagが生成される
- 最新のbranchのコードが圧縮されたファイルが記録される

## SourceTreeのRelease機能

### 手順

1. SourceTreeの上部タブメニューから「リポジトリ/Git flow/新しいReleaseを開始」  
   - developブランチからreleaseブランチを生成
2. SourceTreeの上部タブメニューから「リポジトリ/Git flow/新しいReleaseを終了」  
   - releaseブランチをmasterにマージ
   - masterブランチからdevelopブランチにマージ
   - masterにタグ生成される

### 結果

- releaseブランチをmasterにマージ
- masterブランチからdevelopブランチにマージ
- masterにタグ生成される
- Releaseページに角丸で"Release"とマークされない
- "Releaseするbranch"に対してTagが生成される
- 最新のbranchのコードが圧縮されたファイルが記録される
