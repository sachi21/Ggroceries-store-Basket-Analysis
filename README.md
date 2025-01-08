# Groceries-store-Basket-Analysis
# What is Basket analysis: - " Analytical technique used to uncover the association between items " 
                            - Uncover the products commonly bought together! by consumers.
                            - Also called as Market Basket Analysis
                            - This analysis may reveal that Strawberries and Whipped cream are bought together.

## Use Cases Basket Analysis:-
-- A physical store can adjust the store layout by placing the two items frequently bought together.
-- An online retailer can recommend the products bought together by suggesting the second product to the consumer when buying the first one.
-- A Retailer can create CROSS-SELLING STRATERGIES to sell the products together.
-- And the store can create Promotion of PRICING & Sales Strategies by offering discounts on buying the products together.

## MORE USES Basket Analysis:- 
--- It is also useful to analyze the page visits of a website.
--- The questions raised in the support tickets.
--- Dishes Ordered in a restaurant.

### There are 3 KEY Concepts that are necessary to understand the Basket Analysis.:
---- 1. SUPPORT
---- 2. CONFIDENCE
---- 3. LIFT

[To Understand the above 3 concepts we use 10 data from our sample Groceries Data]
1.berries        ||  Whipped Cream
2. whole milk     ||  root vegetables
3.berries        ||  whipped cream
4. whipped cream  ||  onions
5. berries        ||  coffee 
6. whole milk     ||  whipped cream
7.berries        ||  whipped cream
8. root vegetables||  onions
9. whole milk     ||  root vegetables
10. root vegetables|| whole milk

Sample Data Explanation:- - Sample Grocery store transaction
                          - Consists of 10 transaction
                          - One row = one transaction
                          - Each transaction contains two items
                          The set of items contained in a transaction is called a Basket
                          - Analyse basket of [berries and whipped cream]
                          - 4 transactions with berries
                          - 5 transactions with whipped cream

SUPPORT Explanation :
-- Indicates the percentage of transactions that include two specific products.
[CALCULATION]
    SUPPORT = Number of transactions including both products / total no. of transactions.
Calculating support:-
  For a basket of berries and whipped cream 
  Number of transactions including both products = 3
  Total no. of transaction                       = 10
  Support for basket                             = 3/10 = 30% (percentage convert)
- So SUPPORT indicates the frequency of the products being bought together. So in our example of berries and whipped cream, 30% of the transaction contains these two items together.

CONFIDENCE Explanation:-
-- Confidence is the % of transactions that contain the two products together, out of the transaction containing one of the two products.
-- Confidence is calculated separately for each product in the basket.
    Confidence of product one  = Support of basket / Support of product one
    Confidence of product two = Support of basket / Support of product two.

Calculating Confidence :
For berries and whipped cream  support for basket = 30%
Number of transactions including berries = 4
Support of berries = 4/10 = 40%
Confidence of berries = 30 / 40 = 75%

Confidence of whipped cream
Support of whipped cream = 5/10 = 50%
Confidence of whipped cream = 30/50 = 60%
The two confidence values mean: --75% of customer buy whipped cream when they add berries to their basket.
                                --60% of customers buy berries when they add whipped cream to their basket.
NOTE:-  Confidence indicates the direction of the cross-selling.
        Confidence does not provide the strength of the relationship between the two products.

### LIFT
  Lift gives the strength of the relationship for a basket of two products.
  Formula: LIFT = Support of basket / Support of product one * support of product two
[Calculation LIFT]
  For berries and whipped cream
  Support for basket = 30%
  Support of berries = 40%
  Support for whipped Cream = 50%
  LIFT = 30 / (40 * 50) = 1.5

  NOTE: Lift is not calculated in %, calculated in decimal format.

  Summary: --Lift ~1: No important relationship.
          --Lift > 1:Two products bought together.
          --Lift < 1:Two products not bought frequently.

## Dax Formula used in creating new measures and new table From Grocery Table.

To create a new table from a grocery table we will select new table from Home tab.
![image](https://github.com/user-attachments/assets/6ddf368e-96f3-435c-9a05-2251c4aecc98)

To create total transactions in Grocery table:- 
![image](https://github.com/user-attachments/assets/b0d83d95-fabf-41da-91db-8e95372b8d48)

To create total product count in the grocery table:-
![image](https://github.com/user-attachments/assets/c24e7c1b-0856-45f0-af33-b4b83be9d47e)

New table named Basket Analysis Dax Measures:-
Calculating Support:
![image](https://github.com/user-attachments/assets/fb51398c-0ac6-4127-a8ba-0258313b416c)

Calculating Confidence: for product 1
![image](https://github.com/user-attachments/assets/c5b7fd73-846e-4c5c-83ef-979f17d1c3ca)

Calculating Confidence: for product2
![image](https://github.com/user-attachments/assets/b1969425-7a00-45b8-bfcb-472a46b45832)

Calculating Lift:
![image](https://github.com/user-attachments/assets/d2938bc5-13f4-474c-8ace-112b36e9e291)

Creating Basket:
![image](https://github.com/user-attachments/assets/1004a299-5e19-4566-a2d8-101af8f95d05)


Power BI Report on Basket Analysis Snapshot:

![image](https://github.com/user-attachments/assets/041b0276-646f-495b-bb6d-fd5f0dd990e5)

Visualisation used in Power bi report:
-Two cards to view Total Transactions and Total Products
-Advance network visual to visualize product 1 and product2 in the nodes and in measure we will use Sum of lifts.
.Add some filters based on lift value . Sum of lift choose is greater than [2.2]
.Add Support Basket in the filter section and select option is greater than .6%

- Scatter plot
Add Basket in values, X-axis will be Sum of lift, Y-axis will be Sum of Support Basket.
.Add filter , sum of lift - select option: is greater than 2.2 and  Sum of Support Basket- select option- is greater than .6% and Format the scatter plot label on.

-Matrix visual
Add Basket in rows and in the values:Sum of Support basket,sum of confidence of product1,sum of confidence of product 2,sum of lift
.Add filter 
Sum of lift -  select is greater than option - 2.2
Sum of Support Basket - select is greater than option- 0.6%







            

 

                          

    
|  
