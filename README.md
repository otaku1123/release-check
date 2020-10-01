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

## まとめ

Releaseする手順は、下記が良さそう

1. SourceTreeでgit flowの手順でマージ作業を実施
2. pushする。（GitHub上にタグ情報が登録される）
3. GitHubでpushしたタグページを開く
4. 「Release title」にバージョン情報などを記入
5. Update releaseボタンを押下

上記手順を行うと

- Git flowの流れでマージできる
- GitHub上でReleaseページが生成される
