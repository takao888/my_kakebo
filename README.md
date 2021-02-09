## userテーブル
| columns               | types  | options     |
| --------------------- | ------ | ----------- |
| name                  | string | null: false |
| email                 | string | null: false |
| password              | string | null: false |
| password_confirmation | string | null: false |

### association
- has_many :expenses

## expenseテーブル
| columns  | types      | options           |
| -------- | ---------- | ----------------- |
| memo     | text       |                   |
| day      | date       | null: false       |
| amount   | string     | null: false       |
| category | references | null: false       |
| user     | references | foreign_key: true |

### association
- belongs_to :user