# DB定義書
## ER図
[ER図はこちら]("ER図はこちら")

[画面遷移図はこちら](https://github.com/usagiame/2021sys-design/blob/main/%E3%82%AA%E3%83%BC%E3%83%80%E3%83%BC%E3%83%A1%E3%82%A4%E3%83%89%E3%82%B7%E3%83%A7%E3%83%83%E3%83%94%E3%83%B3%E3%82%B0%E3%82%B5%E3%82%A4%E3%83%88.md"画面遷移図")

# DBテーブルカラム詳細一覧
### 購入テーブル（d_purchase）
|和名|属性名（カラム名）|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|オーダーID|order_id|bigint(20)|〇|〇||
|顧客コード|customer_code|varshar(50)||〇||
|購入日|purchase_date|date||〇||
|総額|total_price|int(11)||〇||

### 購入詳細（d_purchase_detail）
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|オーダー詳細ID|detail_id|bigint(20)|〇|〇||
|オーダーID|order_id|bigint(20)|〇|〇|〇|
|商品コード|item_code|int(11)||〇|〇|
|価格|price|int(11)||〇||
|数量|num|int(11))||〇||

### 顧客マスタ（m_customers）
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|顧客コード|customer_code|varchar(50)|〇|〇||
|パスワード|pass|varchar(50)||〇||
|氏名|name|varchar(20)||〇||
|住所|address|varchar(100)||〇||
|電話番号|tel|varchar(20)||〇||
|メールアドレス|mail|varchar(100)||〇||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||

### カテゴリマスタ（m_category）
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|カテゴリID|category_code|int(11)|〇|〇||
|氏名|name|varchar(20)||〇||
|登録名|reg_date|date||〇||

### 商品マスタ（m_items）
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|商品コード|item_code|int(11)|〇|〇||
|商品名|item_name|varchar(50)||〇||
|価格|price|int(11)||〇||
|カテゴリID|category_id|int(11)||〇||
|画像ファイル名|image|varchar(200)||〇|〇|
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||

