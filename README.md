# MySQL_hands_on_check
スキル面談用MySQLハンズオン

## Setup

以下の手順でMySQLのハンズオン環境をセットアップします。

リポジトリをクローン
```bash
git clone git@github.com:RareTECH-Mentor/MySQL_hands_on_check.git
```

リポジトリのディレクトリに移動
```bash
cd MySQL_hands_on_check
```


Docker Composeを使用してMySQLコンテナを起動
```bash
docker compose up -d --build
```

MySQLコンテナに接続
```bash 
docker exec -it mysql-container mysql -u root -p
# パスワードは `rootpassword` です。
```

## テーブル情報

usersテーブル
| **id** | **username** | **email** |
| --- | --- | --- |
| 1 | 山田太郎 | [yamada@example.com](mailto:yamada@example.com) |
| 2 | 佐藤花子 | [sato@example.com](mailto:sato@example.com) |
| 3 | 鈴木一郎 | [suzuki@example.com](mailto:suzuki@example.com) |
| 4 | 田中美咲 | [tanaka@example.com](mailto:tanaka@example.com) |

channels テーブル
| **id** | **name** |
| --- | --- |
| 1 | general |
| 2 | random |
| 3 | tech |

messages テーブル
| **id** | **user_id** | **channel_id** | **content** | **created_at** |
| --- | --- | --- | --- | --- |
| 1 | 1 | 1 | こんにちは！ | (自動生成: 現在日時) |
| 2 | 2 | 1 | おはよう。 | (自動生成: 現在日時) |
| 3 | 3 | 2 | 雑談しましょう | (自動生成: 現在日時) |
| 4 | 4 | 3 | 最新の技術について話しましょう。 | (自動生成: 現在日時) |
| 5 | 1 | 3 | Pythonが好きです。 | (自動生成: 現在日時) |
| 6 | 2 | 2 | 今日はいい天気ですね。 | (自動生成: 現在日時) |
