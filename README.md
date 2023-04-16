# Placementproject
# Problem Statement

You are a data analyst and your client has a large ecommerce company in India (let’s call it X). 
X gets a thousand orders via their website on a daily basis and they have to deliver them as fast 
as they can. For delivering the goods ordered by the customers, X has tied up with multiple 
courier companies in India as delivery partners who charge them some amount per delivery.

The charges are dependent upon two factors:

● Weight of the product

● Distance between the warehouse (pickup location) and customer’s delivery address 
(destination location)

On an average, the delivery charges are Rs. 100 per shipment. So if X ships 1,00,000 orders 
per month, they have to pay approximately Rs. 1 crore to the courier companies on a monthly 
basis as charges.
As the amount that X has to pay to the courier companies is very high, they want to verify if the 
charges levied by their Delivery partners per Order are correct.

**Step 1** :- Reading all the 5 excels LHS and RHS

**step 2** :- merging df_order_report and df_SKU_Master based on SKU's

**step 3** :- checking the duplicated rows in df_pincode

**step 4** :- dropping duplicates, and merging df_pincode_zones with df_cc_invoice.
Choosing specified columns in df_cc_invoice and storing it in separate variable

**step 5** :- merging the df_cc_inv_pin with df_order_SKU_mg based on order id(ref:step2)

**step 6** :- *Conerting grams to Kilo grams* for that we need rename the columns because column names are with spaces.df.rename(columns={'Order Qty':'Order_Qty','Weight (g)':'Weight_g'}) (here the dataframe named as df.rename)

**step 7** :-Assiging the weight slab and round up the values to nearest for example:- 0.3 to 0.5 , 1.2 to 1.5 .adding those values new column.

Applying the same function in df_cc_invoice

**step 8** :-computing expected charges based on [df_cc_rates] and type of shipment
['Forward charges' 'Forward and RTO charges']

**step 9** :- **renaming the column names** to visualize/differentiate the differences when it merges with actual courier company invoice dataframe
then merging both df_renmae(Output=df_rename with specific coulmns) and df_cc_invoive(output1= df_cc_invoive with specific coulmns)

**step 10** :-
Defference between Expected Charge as per X (Rs.) and Charges Billed by Courier Company. Renaming the columns according to the problemstatment output

**Step 11**:-

1)**writing the dataframe object in to excel**

2)**computing charges on total orders**

3)**writing the query according to format:Total orders where X has been correctly charged <count> <total invoice amount>**

**step 12**:- writing the outputs in given sheets_name 'Calulation', 'Summary' and dowloading it in a zip format
