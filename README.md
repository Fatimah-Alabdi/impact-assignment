- Impact.com – iHerb Feed Integration

This project is part of a technical assignment to integrate with the Impact.com API feed for the iHerb store.  
It retrieves daily performance data and appends it to a Google Sheet automatically.


- Features

- Fetches data from a feed URL (Impact.com CSV)
- Extracts `revenue` and `orders` (actions)
- Appends data to Google Sheets (date, revenue, total orders)
- Scheduled to run daily at **9:00 AM** via a **cron job**
- Writes logs to a local file `log.txt`


File               	Description   
impact_script.py	Main Python script to automate data flow         
log.txt	          Records each execution and posted data           
README.md	        This documentation                              
credentials.json	|  Not included — required for Google Sheets API




-  Cron Job

The script is scheduled to run daily at 9:00 AM using this crontab entry:

bash
0 9 * * * /Users/fatimahabdullah/anaconda3/bin/python /Users/fatimahabdullah/impact_project/impact_script.py >> /Users/fatimahabdullah/impact_project/log.txt 2
