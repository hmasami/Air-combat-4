# Air-combat-4

SIGNATE 第4回 空戦AIチャレンジ用のリポジトリです。

---

## セットアップ手順（WSL2 + Python仮想環境 + SIGNATE CLI）

以下は、このリポジトリをクローンしてから開発環境を整えるまでの手順です。

### 1. リポジトリのクローン

```bash
git clone https://github.com/hmasami/Air-combat-4.git
cd Air-combat-4
```

### 2. WSL2 ターミナルで Python 仮想環境の構築

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. 必要なライブラリのインストール

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. SIGNATE CLI のセットアップ

```bash
pip install signate
signate token -e あなたの登録メールアドレス
```

※ パスワード入力後、API トークンが `~/.signate/signate.json` に保存されます。

> Google アカウントログインの場合は、[パスワードリセット](https://signate.jp) からメールアドレス＋パスワード方式に変更してください。

### 5. データのダウンロード例（ユース部門）

```bash
signate competition-list
signate task-list --competition_key <コンペキー>
signate file-list --task_key=<タスクキー>
signate download --task_key=<タスクキー> --file_key=<ファイルキー>
```

※ ZIP ファイルは `.gitignore` に追加してください（GitHub の 100MB 制限回避のため）

```bash
echo "simulator_dist.zip" >> .gitignore
git add .gitignore
git commit -m "Ignore large zip file"
```

---

## 補足

* Python: 3.10 以上推奨
* OS: Windows 11 + WSL2（Ubuntu 22.04）
* エディタ: VSCode + Remote - WSL 拡張

---

## ライセンス

このプロジェクトは SIGNATE のコンペ参加目的で使用されるものです。

---

## 作者

* GitHub: [hmasami](https://github.com/hmasami)

**Happy Hacking!! ✈️**
