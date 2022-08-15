# Churn-Prediction-Analysis

Dataset Summary 
![image](https://user-images.githubusercontent.com/61017058/184572093-4aa4af07-9fb1-44cc-b98e-9deacc3b34df.png)

Note : 
1. Terdapat missing value di beberapa kolom seperti Tenure, WarehouseToHome, HourSpendOnApp, OrderAmountHikeFromlastYear, CouponUsed, OrderCount, DaySinceLastOrder
2. Tipe data sudah sesuai.

Individual Boxplot (Numerical)
![image](https://user-images.githubusercontent.com/61017058/184572175-d70dbfd1-a23b-4ef2-8222-83ef7021809f.png)

Note : 
1. Dari visualisasi boxplot di atas terdapat outlier yang sangat jauh jaraknya yaitu ada di kolom Tenure, WarehouseToHome, NumberOfAddress, dan DaySinceLastOrder.
2. Dan diketahui ada kolom yang menjalar skewed ke kanan yaitu Tenure, WarehouseToHome, NumberOfAddress, CouponUsed, OrderCount, dan DaySinceLastOrder.

Individual Countplot (Categorical)
![image](https://user-images.githubusercontent.com/61017058/184572299-a6c33ec5-6fee-47dc-8b40-710769369f8a.png)

Note: 
1. Kolom PrefferedLoginDevice mempunyai nilai yang mendominasi pada kategori Mobile Phone
2. Kolom PrefferedPaymentMode mempunyai nilai yang mendominasi pada 2 kategori yaitu Debit Card dan Credit Card
3. Kolom Gender mempunyai nilai yang mendominasi pada kategori Male
4. Kolom PreferedOrderCat mempunyai nilai yang mendominasi pada kategori Laptop & Accessory
5. Kolom MaritalStatus mempunyai nilai yang mendominast pada kategori Married

Correlation Heatmap
![image](https://user-images.githubusercontent.com/61017058/184572407-fddd0ae5-b7c8-4f20-96ad-cee84d2632f5.png)

Note : 
1. Target (Churn) memiliki kolerasi positif dengan CityTier, WarehouseToHome, NumberOfDeviceRegistered, SatisfactionScore, Complain
2. Target (Churn) memiliki kolerasi negatif Tenure, DaySinceLastOrder, dan CashbackAmount.
3. Target (Churn) dengan HourSpendOnApp,NumberOfAddress, OrderAmoundHikeFromlastYear, CouponUsed, OrderCount memiliki kolerasi sangat lemah ~0, ini menandakan bisa jadi fitur tersebut tidak potensial
4. OrderCount memiliki kolerasi cukup kuat dengan CouponUsed. Hal tersebut bisa dikatakan redundant

Pre-Processing : 
1. Train Test Split data
2. Label Encoding
3. Handling Missing Value

Hasil machine learning Model : 
![image](https://user-images.githubusercontent.com/61017058/184574525-1424f2f5-e819-4b4e-b685-00febd66bbec.png)

1. Hasil Modeling dengan Decision Tree recall sebesar 87% 

Hasil modeling dengan Hyperparameter : 
![image](https://user-images.githubusercontent.com/61017058/184575071-86de27c4-931b-4a09-a181-c14e32a02ae0.png)

1. ada perubahan yang cukup signifikan dari hasil machine learning dengan model catboost 93%. ini adalah yang di ambil menjadi implementasi bisnis nantinya.
