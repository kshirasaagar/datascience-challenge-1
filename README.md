# Data Scientist Challenge - No. 1

## Background

Most e-commerce companies while signing up new customers - in the name of frictionless onboarding - do not ask for a lot of details about the customers or their personal information. So customers typically only provide the bare minimum of information needed when signing up as a new user or making a transaction on the site (i.e credit card details, delivery address etc). Most important information left out coule be their age, gender or any other personal details. This is further amplified by "Shop As A Guest Option".

Respecting customer privacy is of the utmost important to all these e-commerce ventures and we understand why some shoppers are hesitant to provide personal information too, in this age of social media baiting. 

However, to be able to better tailor the site, branding strategy, marketing, product and most importantly merchandising, the retail companies need to have a better handle on the profile of their shoppers and understand the things that are more relevant to them. How else would you design your site or your marketing if you didn't know what % of your shoppers are men, women or other genders?

## Solution

In comes the rich treasure trove of behavioural data, that are exhibited by the users while shopping on site or on their apps, which layered on top with the appropriate Machine Learning techniques can fairly accurately delineate the three different gender groups - male, female and others - based on their "expressed behaviour" and "how they shop".

Remember, just because someone buys only male clothes - they are not men. It could be partners, spouses, mums, friends buying for someone else. So just what people buy is not a moniker of who they are. An 80-year young grandma can buy and dress like a 20-year old millenial - age is a number and gender is but an ordinal variable.

## The Challenge

**What we have in this data science challenge here is an opportunity to ‘infer’ a customer’s gender based on the amazingly rich user behavioural data, which will allow us to better tailor the retailer's site and offerings to their needs.**

This way, the customer will be able to control their privacy and while still allowing us to tailor our offerings more suitably to our customer's needs.

There are two main ways to gauge customer behaviour:

- *Purchase Behaviour*: Identify what they purchase, how do they purchase it, frequency, what price points, what discount types resonate etc.
- *Visit Behaviour*: This includes behaviour on site, the way shoppers browse, the types of interactions respond to etc. 

Here are a host of such features that can be engineered, but for now, this should suffice. Using the dataset given, can you predict an "inferred" gender for our customers? 

## The Evaluation
In other words, this is an "unlabelled dataset challenge" - there is no obvious gender variable to learn more, and you have to write an algorithm that can split the groups. Your results [read the section on these things needed from you] will be compared to the benchmark results of the retailer, who has a 95% confidence in their dataset and labels, to identify your algorithm's effective smartness.

## Task

There are four stages to this task:

**Stage 1** : *CLEAN* - Unhash the data (`test_data.zip`) using the secret key provided by us, extract it, most importantly clean it and put it in a form you can use - all programatically of course. We have also "intentionally" corrupted two columns in this file - two columns that might look correct but are not correct. They need "some correction" to be useful.

**Stage 2** : *BUILD* - Build a deep learning model (preferably) or any other model that suitably answers this question and predict the inferred gender using the features provided and deriving more featueres at your end. Remember, there is no gender flag, so you are flying blind here.

**Stage 3** : *DELIVER* - Package all your process, findings and code into a reproducible document that can be understood by a business user. A repo of the code branch would be a great thing to have! This **reproducible report** must answer the following questions:

1. How did you clean the data and what was wrong with it? Close to 90% of a Data Scientist's job is in cleaning data
2. What are the features you used as-is and which one did you engineer using the given ones? What do they mean in the real world?
3. What does the output look like - how close is the accuracy of the prediction in light of data with labelled flags?
4. What other features and variables can you think of, that can make this process more robust? Can you make a recommendation of top 5 features you'd seek to find apart from the ones given here
5. Summarize your findings in an *executive summary*

## Evaluation Criteria

**Given dependencies and other instructions, we should be able to re-run your source code with the dataset in the same directory and obtain the same results and figures. Popular formats for this include RMarkdown and Jupyter Notebook (formerly IPython)**

Also, we have a larger sample set on our end on which we can run your source code and check out the accuracy of your predictions. Think Kaggle :)

**We are looking to find these three things from you:**

1. Your R or Python code \n
2. Your output file for all the customers along with a gender flag - two fields - customer_id, female_flag (1 if female, 0 if male) \n
3. A markdown document that contains your code or independent of the code that explains your logic \n

## Data

We have provided one zipped file - `test_data.zip` which contains the data in json format. Opening this using our hashed passcode is the ZEROTH challenge. The passcode is right, you don't have to check if we did something wrong :)

The file (`test_data.zip`) has been super encrypted - the password to the file is "an unserialized lowercase SHA-256 hash" of the keyword you received. Reminder the password to the file is not the password shared with you but the unserialized SHA-256 hash of the password.

This dataset is purely synthetic and modelled on top of a few actual retailer's open datasets. Users are randomly sampled to and anonymised, along with programatically shifting all their behavioural metrics by set deviations.

TL;DR - Don't worry, consider this dataset to be as close to reality as possible.

The dataset is currently been put in a JSON format, hashed and then compressed - so all the best! 

**The way to open the files is by working on the passcode that you received from us to get the right password!**

| Column                   | Value   | Description                                                              | 
|--------------------------|---------|--------------------------------------------------------------------------| 
| days_since_first_order   | integer | Days since the first order was made                                      | 
| days_since_last_order    | integer | Days since the last order was made                                       | 
| is_newsletter_subscriber | string  | Flag for a newsletter subscriber                                         | 
| orders                   | integer | Number of orders                                                         | 
| items                    | integer | Number of items                                                          | 
| returns                  | integer | Number of returned orders                                                | 
| different_addresses      | integer | Number of times a different billing and shipping address was used        | 
| shipping_addresses       | integer | Number of different shipping addresses used                              | 
| devices                  | integer | Number of unique devices used                                            | 
| vouchers                 | integer | Number of times a voucher was applied                                    | 
| cc_payments              | integer | Number of times a credit card was used for payment                       | 
| paypal_payments          | integer | Number of times PayPal was used for payment                              | 
| afterpay_payments        | integer | Number of times AfterPay was used for payment                            | 
| female_items             | integer | Number of female items purchased                                         | 
| male_items               | integer | Number of male items purchased                                           | 
| unisex_items             | integer | Number of unisex items purchased                                         | 
| wapp_items               | integer | Number of Women Apparel items purchased                                  | 
| wftw_items               | integer | Number of Women Footwear items purchased                                 | 
| mapp_items               | integer | Number of Men Apparel items purchased                                    | 
| wacc_items               | integer | Number of Women Accessories items purchased                              | 
| macc_items               | integer | Number of Men Accessories items purchased                                | 
| mftw_items               | integer | Number of Men Footwear items purchased                                   | 
| sprt_items               | integer | Number of Sport items purchased                                          | 
| msite_orders             | integer | Number of Mobile Site orders                                             | 
| desktop_orders           | integer | Number of Desktop orders                                                 | 
| android_orders           | integer | Number of Android app orders                                             | 
| ios_orders               | integer | Number of iOS app orders                                                 | 
| work_orders              | integer | Number of orders shipped to work                                         | 
| home_orders              | integer | Number of orders shipped to home                                         | 
| parcelpoint_orders       | integer | Number of orders shipped to a parcelpoint                                |
| coupon_discount_applied  | float   | Average discount rate applied via coupon based discount e.g. SAVE15      | 
| revenue                  | float   | $ Dollar spent overall per person                                        |
| customer_id              | string  | ID of the customer - super duper hashed                                  | 

All the best! Blow us away with your findings and accuracy!
