# next-react-memo
Next.js、Reactのメモ

# Node.jsのバージョンアップ方法
Mac / Linux の場合
① nvmが入っているか確認
```
nvm -v
```
出なければインストール：
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```
その後ターミナル再起動。

② Node最新版インストール
安定LTS（おすすめ）
```
nvm install 22
```
または
```
nvm install 20.19.0
```
③ 使うバージョンを切り替え
```
nvm use 22
```

④ デフォルトに設定
```
nvm alias default 22
```

⑤ 確認
```
node -v
```

→ v22.x.x ならOK

# Next.jsの考え方
https://zenn.dev/akfm/books/nextjs-basic-principle/viewer/intro

### Reactのコンテンツ
- React Road

https://react-road.b13o.com/roadmap

- サイト

https://qiita.com/KNR109/items/af433f1013221c5ed529

### Reactの条件付きレンダリング
Reactの条件付きレンダリング（Conditional Rendering）とは、特定の条件に応じて表示するコンポーネントや要素を切り替えるテクニック。
たとえばログインしているかどうかで表示を変える、ローディング中かどうかで内容を切り替えるなど、UIを動的に制御するために使う。

ex)
 - if 文
 - 三項演算子（? :）（よく使う！）
 -  論理 AND（&&）演算子
 -  要素の変数化

- 応用例：ボタンの切り替え
```tsx
function LoginControl({ isLoggedIn, onLogin, onLogout }) {
  return (
    <div>
      {isLoggedIn
        ? <button onClick={onLogout}>ログアウト</button>
        : <button onClick={onLogin}>ログイン</button>}
    </div>
  );
}



```
 
