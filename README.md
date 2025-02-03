# Timeseries Forecasting E-commerce Sales
## Forecast sales using store, promotion, and competitor data
### Dataset Description
You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set.
Note that some stores in the dataset were temporarily closed for refurbishment.
### Files
- train.csv - historical data including Sales
- test.csv - historical data excluding Sales
- sample_submission.csv - a sample submission file in the correct format
- store.csv - supplemental information about the stores
- (Could be downloaded from Kaggle: https://www.kaggle.com/competitions/rossmann-store-sales)
### Data fields
- Id - an Id that represents a (Store, Date) duple within the test set
- Store - a unique Id for each store
- Sales - the turnover for any given day (this is what you are predicting)
- Customers - the number of customers on a given day
- Open - an indicator for whether the store was open: 0 = closed, 1 = open
- StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and
                 weekends a = public holiday, b = Easter holiday, c = Christmas, 0 = None
- SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools
- StoreType - differentiates between 4 different store models: a, b, c, d
- Assortment - describes an assortment level: a = basic, b = extra, c = extended
- CompetitionDistance - distance in meters to the nearest competitor store
- CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened
- Promo - indicates whether a store is running a promo on that day
- Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
- Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2
- PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in
                  February, May, August, November of any given year for that store
## Assumptions
### Based on Promotion, Competition and Holiday information given, right of the bat, these are the assumptions that one can come up with
- Stores with a larger product assortment should sell more.
- Stores with closer competitors should sell less.
- Stores with competitors that have been around for longer should sell more.
- Stores with promotions running for longer should sell more.
- Stores with more days of promotions should sell more.
- Stores with more consecutive promotions should sell more.
- Stores that open during the Christmas holidays should sell more.
- Stores should sell less on weekends.
- Stores should sell more over the years.
- Stores should sell more in the second half of the year.
- Stores should sell more after the 10th of each month.
- Stores should sell less during school holidays.

## Observations and Methodology
- The assumptions or in other words hypothesis are tested with the data presented and determined if they are true or false
- Then manually select features, based on the above observation that are useful for our prediction.
- Compare the performance of by fitting the data in various ML models and cross validation
<img width="557" alt="Screenshot 2025-02-01 at 10 43 30 PM" src="https://github.com/user-attachments/assets/3f6fcd41-5f60-4b10-9c72-db8ee1d0ef30" />


## Results
<img width="263" alt="Screenshot 2025-02-01 at 10 34 53 PM" src="https://github.com/user-attachments/assets/b642c747-c9f7-453b-b5f7-100a0c86cd0f" />





