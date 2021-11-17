# data_cleaning

Starbucks processing

range: 
US No. 7435 to No. 11238
FR No. 17644 to No. 17737 
       
1. read starbucks.csv
2. split to 2 dataframe, 'us_df' and 'fr_df'
3. str_to_json function to work on ['schedule] column, replace with ', True, False, None value and split to different days
4. concat two dataframes 
5. set new column names
6. separate day hours with .str.split(' to ', expand=True) to new columns day_open, day_close 
7. convert AM, PM to 24hr clock, use pd.to_datetime().dt.strftime('%H:%M')
8. split df['olsonTimeZoneId'] to df['GMT'] and  df['GMT_region']
9. city lowercase
10. combine address1,2,3 with '|' in df['address'] then delete streetAddressLine1,2,3 
11. reorder columns
