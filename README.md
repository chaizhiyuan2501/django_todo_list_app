# 💻 Django Todoリストアプリ(編集中)

## 📄 概要
このプロジェクトは Django で作成した**Todoリスト**アプリケーションのです。

---

## 🛠️ 使用技術
- **フレームワーク**: Django
- **プログラミング言語**: python:3.11-slim
- **データベース**: PostgreSQL
- **フロントエンド**: HTML / CSS / bootstrap5
- **仮想環境**: Docker

---

## 画面遷移図

このドキュメントでは、Todoリストの画面遷移について説明します。

## 🎯 画面一覧
| 画面名             | URL パス           | 説明                           |
|-----------------|-----------------|--------------------------|
| ホーム          | `/`             | メインページ               |
| ユーザー登録    | `/register/`    | 新しいユーザーを登録する     |
| ログイン        | `/login/`       | ユーザーログインページ       |
| パスワード更新  | `/update_password/<int:pk>` | パスワードを変更する |
| プロフィール更新 | `/update_profile/<int:pk>` | ユーザーのプロフィール編集 |
| ログアウト      | `/logout/`      | ユーザーをログアウト         |
| ユーザーページ  | `/user/`        | ユーザー情報を表示         |

## 🔗 画面遷移フロー
```
+----------------+        +----------------+
| ホームページ   | ----> |  新規登録      |
| (/)           |        |  (/register/)  |
+----------------+        +----------------+
       |                        |
       v                        v
+----------------+      +----------------+
|  ログイン      | <--> | パスワード変更 |
| (/login/)     |      | (/update_password/<int:pk>/) |
+----------------+      +----------------+
       |
       v
+----------------+      +----------------+
| プロフィール画面 | <--> | プロフィール変更 |
| (/user/)      |      | (/update_profile/<int:pk>/) |
+----------------+      +----------------+
       |
       v
+----------------+
|   ログアウト    |
|   (/logout/)   |
+----------------+
       |
       v
+----------------+
| ホームページ   |
| (/)           |
+----------------+
```


## 🚀 実行方法

### 1️⃣ **リポジトリをクローン**
```bash
git clone https://github.com/chaizhiyuan2501/django_user_app.git
cd django_user_app
```

### 2️⃣ **Docker を使用してコンテナを起動**
```bash
docker-compose up --build
```

### 3️⃣ **データベースのマイグレーション**
```bash
docker-compose exec web python manage.py makemigrations
```
```bash
docker-compose exec web python manage.py migrate
```

### 4️⃣ **スーパーユーザーの作成（管理者アカウント）**
```bash
docker-compose exec web python manage.py createsuperuser
```

### 5️⃣ **テストツールを実行する**
```bash
docker-compose exec web python manage.py test
```
### 6️⃣ **テスト用ユーザーを作成する**
```bash
docker-compose exec web python main.py
```

### 7️⃣ **サーバーの起動**
コンテナはすでに起動しているので、以下の URL にアクセスしてください。
```
http://127.0.0.1:8000/
```

---

## 🎯 主な機能
- ユーザー認証(新規登録､ログイン､ログアウト)
- ユーザー管理（プロフィール追加・編集）
- レスポンシブデザイン（Bootstrap 5 使用）

---


---

## 📑 今後の改善点
- [ ] Viewテストコードの追加
- [ ] Googleアカウントと連携しログインする
- [ ] メール認証機能の追加
- [ ] 例外処理ページの追加
- [ ] Todoリスト機能の追加
---

## 👨‍💻 作者
[Chai ZhiYuan](https://github.com/chaizhiyuan2501)
お問合せ: chaizhiyuan2501@gmail.com

---
