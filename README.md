# Jenn's Note

![image](https://github.com/NARAEIM/tp2-da/assets/107841791/49df74ef-b33e-41d3-bd10-13fb7e4ba92d)
![image](https://github.com/NARAEIM/tp2-da/assets/107841791/73e221d1-d1bd-4229-8c1a-a5b3702fa3f1)

---
### most active customer influx
2021: 22.7%. <br/>
July: 14.7%.<br/>
check promo's impact on influx in transaction dataset.<br/>
-> promo most used in July: AZ2022<br/>
-> promo mostly used in 2021: AZ2022<br/>

---
### 전체 중 first created_at(first_transaction)에서 promo가 사용된 customer의 비율
```
first_transaction = merged_new.groupby('customer_id')['created_at'].min()
completed_promo_transactions = merged_new[merged_new['w_promo'] == 1]
customers_completed_promo = first_transaction[first_transaction.isin(completed_promo_transactions['created_at'])]
proportion = len(customers_completed_promo) / merged_new.shape[0]
proportion
```
result: 0.040414957934296995 -> 4%

### total_amount in transaction 비교
first created_at(first_transaction)에서 promo가 사용된 customer의 비율에서 first 

### the number of promo code usages by each customer
