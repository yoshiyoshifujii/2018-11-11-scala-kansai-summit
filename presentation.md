title: akka-httpでの総当たり攻撃対策ライブラリakka-guardの紹介
class: animation-fade
layout: true

<!-- This slide will serve as the base layout for all your slides -->
.bottom-bar[
  {{title}}
]

---

class: impact

# .my-title[{{title}}]
## @yoshiyoshifujii

---

# 自己紹介

.col-6[

- Yoshitaka Fujii [@yoshiyoshifujii](https://twitter.com/yoshiyoshifujii)
- ChatWork株式会社 (2ヶ月)
- Scala関西 Summit スタッフ
- Scala歴 4年
- Contributors of Akka
- [chatwork/akka-guard](https://github.com/chatwork/akka-guard)
- 🍣 🍶

]

.col-6[

.right[<img src="https://pbs.twimg.com/profile_images/907421547551277056/_vQ3f2Fg_400x400.jpg">]

]

---

class: impact

# .my-title[みなさん<br>総当たり攻撃対策<br>どうされてますか？]

---

# 総当たり攻撃とは

> 総当たり攻撃（そうあたりこうげき）とは、暗号解読方法のひとつで、可能な組合せを全て試すやり方。力任せ攻撃、または片仮名でブルートフォースアタック（英: Brute-force attack）とも呼ばれる。

.right[.small[https://ja.wikipedia.org/wiki/%E7%B7%8F%E5%BD%93%E3%81%9F%E3%82%8A%E6%94%BB%E6%92%83]]

---

# 総当たり攻撃とは

## 最も原始的かつ最も確実な攻撃

- 時間を掛ければいつかは正解に行きつくという確実性を持った攻撃
- コンピュータの性能が向上することによって反復処理のスピードも速くなっている

---

# どのような対策があるか

- パスワードの桁数を増やす（長さを大きくする）
- パスワードに使える文字数に記号や漢字など他の文字を許可しパターンを増加させる
- 第２のパスワードを用意する（セキュリティーコードなど）
- パスワードの試行回数を制限する
- アクセス元を制限する

---

# どのような対策があるか

- 一定の速度以上でのパスワード試行を禁止する
- 数分ごとに自動変化するパスワードにする
  - （ワンタイムパスワード、セキュリティトークンを参照）
- 一定以上のミスに対して、警告メールを管理者に送信する
- 人による常時監視システムにて、異常なパスワード試行がないか監視する

---

# 総当たり攻撃対策にも使えるakka-guard

- 特定の失敗条件を元に
- 特定のリクエストをブロック
- パスワードの試行回数を制限する
- 失敗回数が閾値を越えるとリクエストをブロック
- サーバーリソースの消費を抑えることができる

---

# 設計思想

---

# 実装

---

# 使い方

---

# 効果測定

---

