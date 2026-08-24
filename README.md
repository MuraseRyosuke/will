# Public Will & Digital Declaration (デジタル遺言・置文)

[![Website](https://img.shields.io/badge/Web-will.muraseryosuke.info-blue)](https://will.muraseryosuke.info)
[![OpenPGP](https://img.shields.io/badge/OpenPGP-Ed25519-green)](https://will.muraseryosuke.info/gpgkey.txt)
[![License: CC BY-SA 4.0 / CC0](https://img.shields.io/badge/License-CC%20BY--SA%204.0%20%2F%20CC0-orange)](https://creativecommons.org/licenses/by-sa/4.0/)

村瀨亮介（[@muraseryosuke](https://github.com/muraseryosuke)）のデジタル遺言（パブリック・ウィル / 置文）およびOpenPGP公開鍵の公開用リポジトリです。  
山形浩生氏（[cruel.org](https://cruel.org/will.html)）や橋本麦氏（[baku89.com](https://baku89.com/ja/will)）の意思表明に倣い、不測の事態における創作物の死後ライセンスおよびデジタル資産の運用方針を定めています。

🌐 **Web Page**: [https://will.muraseryosuke.info](https://will.muraseryosuke.info)

---

## 🔑 GPG Key Information

- **User ID**: `Ryosuke Murase <mail@muraseryosuke.info>`
- **Key ID**: `ACE91C7A58FBB001`
- **Key Type**: `ed25519 / cv25519`
- **Fingerprint**: `1E7B 5BA3 FF10 F030 DAE0 51C1 ACE9 1C7A 58FB B001`
- **Public Key File**: [gpgkey.txt](./gpgkey.txt) / [https://will.muraseryosuke.info/gpgkey.txt](https://will.muraseryosuke.info/gpgkey.txt)

---

## 🔍 Verification (署名検証)

ターミナルから以下のコマンドを実行することで、公開鍵のインポートおよび文書の真正性（改ざんされていないこと）を検証できます。

```bash
# 1. 公開鍵のインポート
curl -s [https://will.muraseryosuke.info/gpgkey.txt](https://will.muraseryosuke.info/gpgkey.txt) | gpg --import

# 2. 署名付き遺言の検証
curl -s [https://will.muraseryosuke.info/index.txt](https://will.muraseryosuke.info/index.txt) | gpg --verify
```

---

## 📁 Repository Structure

```text
.
├── CNAME           # GitHub Pages用カスタムドメイン設定
├── .nojekyll       # Jekyll無効化設定
├── gpgkey.txt      # GPG公開鍵（ASCII Armor形式）
├── index.html      # Web表示用フロントエンド
├── index.txt       # GPGクリア署名付き遺言テキスト（確定版）
├── will.txt        # 遺言テキスト原本（編集用ソース）
└── README.md       # 本ドキュメント
```

---

## 🛠 For Author (更新手順メモ)

文面を更新する際の再署名・デプロイ手順：

```bash
# 1. will.txt を編集
# 2. 再署名（index.txt を再生成）
gpg --clearsign --output index.txt --yes will.txt

# 3. リポジトリに反映してプッシュ/アップロード
```

---

## 📜 References
- [cruel.org/will.html](https://cruel.org/will.html) - 山形浩生氏の遺言状
- [baku89.com/ja/will](https://baku89.com/ja/will) - 橋本麦氏の置文
