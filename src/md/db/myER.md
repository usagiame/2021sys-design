@startuml
package "ECサイト" as target_system {
entity "購入テーブル" as purchase <d_purchase> {
+ order_id [PK]
--
# customer_code [FK]
purchase_date
total_price
}

entity "購入詳細テーブル" as purcher_detail <d_purchase_detail> {
+ detail_id [PK]
+ order_id [PK] [FK]
--
# customer_code [FK]
purchase_date
}

entity "顧客マスタ" as customer <m_customers> {
+ customer_code [PK]
--
pass
name
address
tel
mail
del_flag
reg_date
}

entity "購入履歴" as rireki <m_rireki> {
+ rireki_code [PK]
--
syouhinn
date
}

entity "カテゴリマスタ" as category <m_category> {
+ category_id [PK] [FK]
--
name
reg_date
}

entity "商品マスタ" as items <m_items> {
+ item_id[FK][PK]
--
item_name
price
# category_id[FK]
image
detail
del_flag
reg_date
}

entity "イベントテーブル" as ibento <m_ibento> {
+ ibento_id[PK][FK]
--
date
}
}

purchase --|{ purcher_detail
purchase --|{ rireki
purcher_detail ---- rireki
customer }o--|{ purchase
items }o--|{ purchase
items }o--|{ category
category }|-d-o{ ibento
@enduml
