+++
title = "レプリケーションタスクの作成と実行"
weight = 40
+++

### レプリケーションタスクの作成と実行

マネジメントコンソール上部の **「サービス」** から **<a href="https://console.aws.amazon.com/dms/v2/home?region=us-west-2" target="_blank">Database Migration Service (DMS)</a>** のページを開き、左のメニューから **「データベース移行タスク」** をクリックします。**「タスクの作成」** ボタンをクリックして、レプリケーションタスクの作成を開始します。

1. **「データ移行タスクの作成」** 画面で、以下のパラメータを入力します。

    | パラメータ               | 入力値                                               |
    | ---------------------- | --------------------------------------------------- |
    | タスク識別子             | replication-cdc                                     |
    | レプリケーションインスタンス   | replication-instance                             |
    | ソースデータベースエンドポイント        | source-endpoint                          |
    | ターゲットデータベースエンドポイント        | target-endpoint                       |
    | 移行タイプ         | 既存のデータを移行して、継続的な変更をレプリケートする              |
    | 作成時にタスクを開始      | チェックを入れる                                         |
    
    ![Create-task-1](/db-mig/Create-task-1.ja.png)

2. **「タスク設定」** のセクションで、以下の値を入力します（他はすべてデフォルトのままにしておきます）。

    | パラメータ              | 入力値                                               |
    | ---------------------- | --------------------------------------------------- |
    | ターゲットテーブル作成モード          |  何もしない          |
    | 検証の有効化      | チェックを入れる                                             |                 
    | CloudWatch ログを有効化 | チェックを入れる                                             |
    
    ![create-task-2](/db-mig/create-task-2.ja.png)
    
3. **「テーブルマッピング」** のセクションで、**「ガイド付き UI」** を選択し、**「新しい選択ルールの追加」** ボタンをクリックします。**スキーマ**のドロップダウンリストから **wordpress-db** を選択します。

    **スキーマ**のドロップダウンリストに wordpress-db が表示されない場合は、**スキーマ**のドロップダウンリストから、**「スキーマの入力」** を選択し、**スキーマ名**のフィールドに **wordpress-db** を入力します。
    
    ![Create-task-3](/db-mig/Create-task-3.ja.png)

4. 画面の一番下までスクロールし、**「タスクの作成」** ボタンをクリックしてタスクを作成し、データのレプリケーションを開始します。

    ![create-task-4](/db-mig/create-task-4.ja.png)