The procedure for this assignment is as follows:
1. I imported Numpy Pandas Matplotlib,Seaborn, Request and json libraries
2. I created a function in which i used get() method which passed a request and get some response from the api link. If the response was 200, I stored it in json by json() method and returned it otherwise returned None as no data was retrieved from the API.
3. I called this function for FINNIFTY, NIFTY, SENSEX and BANKEX for 0edt-4edt.From the json I extracted result and stored it in the form of dataframe.
4. I combined all the dataframes to form a single training dataframe
5. I used Datetime class to handle date and time columns and extract year month and date out of them
6. I converted all the numeric string columns as float and labelencoded type of share in order to get all the integers in the dataframe
7. I dropped high,low,close and open column for X and stored close,open,high and low in Y1,Y2,Y3 and Y4 respectively
8. I initialized 4 linear regression models for predictions of close,open,high and low.
9. In respective model, I fit input X and targetted Y. I got 91-93% score in all my models.
10. I then assuming the previous expiry data as the next expiry data predicted tomorrow's close, open, high and low using the trained models.
