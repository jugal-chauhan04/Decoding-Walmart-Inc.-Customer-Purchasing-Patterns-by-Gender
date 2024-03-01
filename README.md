# Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender
This project showcases the application of data visualization techniques to perform Exploratory Data Analysis to unravel gender disparities, with Walmart Inc. serving as a case study.

## Problem Description  

Our aim is to analyze customer purchase behavior, specifically the purchase amount, in
relation to customer gender and various other relevant factors. The key objective is to
understand whether there are differences in spending habits between male and female
customers. This analysis will provide valuable insights for the business to make
data-driven decisions, optimize marketing strategies, and allocate resources effectively,
ultimately enhancing revenue and customer satisfaction.  

## Dataset Description  

The data is obtained from kaggle dataset ‘Walmart_data:Transactional Data of
customers who purchased products in Black Friday’ (Bagale, 2022)  

The dataset comprises Walmart purchase data with the following columns:  

1. User_ID: Identifier for the user making the purchase.  
2. Product_ID: Identifier for the purchased product.
3. Gender: Gender of the customer (e.g., Male or Female).
4. Age: Age group of the customer.
5. Occupation: Occupation of the customer.
6. City_Category: The category of the city where the purchase was made.
7. Stay_In_Current_City_Years: The number of years the customer has been
residing in the current city.
8. Marital_Status: Marital status of the customer.
9. Product_Category: The category of the purchased product.
10. Purchase: The purchase amount made by the customer.

The programming language used here is Python, and the environment is Jupyter.
The following libraries will be employed for data visualization and analysis in this
project: Matplotlib, Seaborn, Pandas, ggplot, and Numpy, among others.  

## Univariate Analysis  

To better understand the distribution of features in the data we start by exploring single variables. Here we are looking at the composition of male and female customers, the age distribution of customers, and finding out which products are popular among both the genders and different age groups. The main objective of performing univariate analysis is to try and visualize the data in order to find any patterns.  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/061bf83c-4567-4b58-b5f4-2a759017d742)

On conducting a univariate analysis on the data to examine the gender distribution. The results indicate that the majority of customers, approximately 75%, are men, while the remaining 25% are women. This distribution is visually represented in a bar plot, where the count for women is 135,809 and for men is 414,259.  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/392523f1-f8e2-4f09-9c8f-94d8b314c3d3)

The age distribution of all customers was categorized into seven sections: [0-17], [18-25], [26-35], [36-45], [46-50], [51-55], and [55+]. The bar plot reveals that the majority of customers fall into the age group of 26-35 years old, while the least number of people are in the 0-17 age bracket.   

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/a097275e-98e2-49ce-a05c-bed60a94a4dd)

This plot illustrates the marital status of customers. It reveals that nearly 41% of customers are married, while the remaining 59% are unmarried.  

## Bivariate Analysis  

The aim of conducting bivariate analysis is to explore how the distribution of age groups varies between male and female customers and based on the marital status of customers. Analyzing age, gender, and marital status together helps find points where they all affect customers' behavior. This overall understanding will help stores make shopping more personal, manage products better, and improve ads to meet the different needs of customers on Black Friday. Furthermore, a correlation analysis was considered to see what attributes impact purchase behavior, however, with the dataset predominantly having categorical values, the correlation analysis seemed fruitless as it could not generate any insight related to gender, age or marital status affecting the purchase.  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/6c86da7b-3d50-4415-a37a-0c2493facbaa)
 
We observe a consistent pattern where unmarried individuals tend to spend more than their married counterparts across all age groups. Notably, the age group [50-55] emerges as the highest spending group, regardless of marital status. Conversely, the least spending is observed in the [0-17] and [46-50] age groups, particularly among those who are not married.  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/8748c76c-06a6-4d41-ad05-ecfc270d7d1f)

A consistent trend emerges as we observe that males consistently exhibit higher spending compared to females across all age groups. Notably, the age group [50-55] stands out as the highest spending bracket for men, while for women, it is [50+]. Conversely, the lowest spending among women is observed in the [0-17] and [18-25] age groups around $8300 and for men the lowest spending is around $9200.  

## Central Limit Theorem - Gender Analysis

To obtain robust conclusions regarding the spending behavior among gender, age groups and marital status, it is beneficial to implement a statistical method that allows us to make more reliable inferences about spending patterns. In this case, we implement the Central Limit Theorem and calculate Confidence Intervals. The Central Limit Theorem states that the distribution of sample means approaches a normal distribution, even if the original population distribution is not normal, given a sufficiently large sample size. By calculating sample means for spending patterns within different gender, age, and marital status categories, we can rely on the CLT to assume normality. This allows for the construction of confidence intervals around the sample means, providing a range within which the true population mean is likely to fall. Thus, we can estimate the spending differences among gender, age group and marital status which will provide valuable insights for data driven decision making at Walmart.  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/85bf43b2-1f8e-4758-843f-07c0d580d61f)


![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/b520c683-bedf-4d3c-84b9-9dcb28a6b54e)


![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/70741beb-174b-4d68-8903-a7d6c2700235)


![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/1a97648a-4b3e-4156-aba5-b1f8e6cf0963)
  

We can see from the figures that as the sample size increases the difference between both the gender becomes more pronounced. The 95% confidence interval for the population mean of male spending is relatively narrow, ranging from $9,406.68 to $9,468.58. However, the 95% confidence interval for the population mean of female spending is narrow, spanning from $8,704.83 to $8,764.09.

Thus, we can conclude that male spend relatively higher compared to women.  

## Central Limit Theorem - Marital Status Analysis  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/2e16d72f-8be1-400d-a368-57718d23c0ab)

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/34f2bef1-c6de-4d13-aae9-31fbd73b3fb9)


![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/43bef04c-d287-4aa1-8482-996da17d1de3)

  
![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/d33b42bf-db06-4b53-b043-eb462b61c1f4)  


Here, using CLT we can see that increasing the sample size does not result into strong difference between the values of married and unmarried groups. Unmarried group tends to spend 9267.97$ and the married ones spend 9249.48$. Thus we can see that the difference between them is not significant.  

## Central Limit Theorem - Age Analysis  

![image](https://github.com/jugal-chauhan04/Decoding-Walmart-Inc.-Customer-Purchasing-Patterns-by-Gender/assets/111266884/66580ff2-e83b-4a16-8231-9d846bf6be3d)

Based on the analysis of the Age group which was divided into 7 groups. We can conclude that customers in the age group of 0-17 spent the lowest compared to the age group of 51-55 which spent the highest. The other age groups has almost similar spending.  

## Key Findings:

1. Univariate analysis highlighted:
   * Men tend to spend more than women.
   * Highest spenders are 50+ and unmarried.
2. Bivariate analysis revealed:
   * Unmarried individuals consistently exhibit higher spending.
   * Males spend more than females, especially in [50-55] bracket.

3. Central Limit Theorem analysis:
   * Confirmed increasing sample size accentuates spending difference between genders.
   * Emphasized that males generally spend more than females.

4. Additional Insights:
   * Marital status has a relatively minor impact on spending.
   * In the age category, customers aged 51-55 are the highest spenders, while those aged 0-17 spend the least.

## References  

1. Tengli A, Srinivasan SH. An Exploratory Study to 
Identify the Gender-Based Purchase Behavior of 
Consumers of Natural Cosmetics. Cosmetics. 2022; 
9(5):101. 
https://doi.org/10.3390/cosmetics9050101

2. Pakasi, A., & Tumiwa, J. (2016). Comparison 
analysis between male and female of consumer 
purchase behavior of Yamaha Mio. Jurnal EMBA: 
Jurnal Riset Ekonomi, Manajemen, Bisnis dan 
Akuntansi, 4(1).
4. Ronaghi, M., Danae, H., & Haghtalab, H. (2013). 
Survey of effects of gender on consumer behavior; 
case study on mobile phone. International Journal 
of Advanced Studies in Humanities and Social 
Science, 1(8), 1024-1033.
5. Abir Smiti, A critical overview of outlier detection 
methods, Computer Science Review, Volume 
38,2020, 100306, ISSN 1574-0137,
https://doi.org/10.1016/j.cosrev.2020.100306.
(https://www.sciencedirect.com/science/article/pii/
S1574013720304068)


















