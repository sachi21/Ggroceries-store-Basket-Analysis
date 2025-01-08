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
- So SUPPORT indicates the frequency of the products being bought together. So in our example of berries and whipped cream 30% of the transaction contain these two items together.

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

  NOTE: Lift is not calculated in % , calculated in decimal format.

  Summary: --Lift ~1: No important relationship.
          --Lift > 1:Two products bought together.
          --Lift < 1:Two products not bought frequently.
        
            

 

                          

    
|  
