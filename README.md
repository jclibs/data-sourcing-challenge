# data-sourcing-challenge

In this challenge I utilized the NASA API to find information on GST activity and CME activity.
From both the CME data and the GST I created a url, read the data to a json, and used the json to generate a dataframe. 
For each dataframe I isolated the relevent columns, broke the linkedEvents column down for each event to have its own row, and changed the dtypes of the columns to suit my needs.
I then created columns for the cmeID and GST_ActivityID in the expanded_cme_df, and gstID and CME_ActivityID in the gst_df.
I merged the two df's on gstID and CME_ActivityID for gst_df and GST_ActivityID and cmeID for expanded_cme_df.
With the merged data frame I calculated the time difference between GST and CME activities, and then used the describe() funcion to find the median and mode for the time difference.
Lastly I exported my merged data frame and the results of my describe() to csv files.
