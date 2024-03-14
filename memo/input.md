# 2024.02.23
## Git setup
Macを変えていたのでsshをGitに登録

## Intro & Demo
## Additional content
## Setup
shadcn/uiというのを使ってコンポーネントは楽できる
https://ui.shadcn.com/docs/components/button

npm run dev
実行

# 2024.02.24
## Routing concepts
page.tsxというファイル名にするとpageとして扱ってくれる
APIはroute.tsとする

### Layout
ディレクトリにlayout.tsxを作り、{children}を渡し(?)div内に{children}を置くと、その子ディレクトリ内のpage.tsx全体をchildrenとして扱ってレイアウトを組める
例えばloginとregisterで同じヘッダーを使いたい時にAuthLayout.tsxでヘッダー,childrenを並べれば、それぞれのpageでヘッダーがつく

### カッコ付きのディレクトリ名
通常ディレクトリの階層がそのままURLになるが
ex:
auth
 login
-> auth/login

ディレクトリ名をカッコで囲うとURLに表示されない
ex:
(auth)
 login
-> login

### component
appFolder内に作られたファイルはすべてserver component
server componentの中にclient componentがあるイメージ

"user client"と書くと、そのコンポーネント+子はclient componentになる

# Authentication
https://clerk.com/

# Dark mode
アンダースコア始まりのフォルダ: ルーティングに影響を及ぼさないフォルダ（プライベートフォルダ）
- なるべくpageとcomponentは近いところに書きたい（appの外のcomponentsに書くことも可能だが可読性が×）
- UI ロジックをルーティング ロジックから分離する役割

パラグラフ内でカンマを使いたい時は&aposとする