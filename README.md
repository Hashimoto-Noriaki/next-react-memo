# next-react-memo
Next.js、Reactのメモ

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
 
