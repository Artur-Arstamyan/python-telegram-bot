**python-telegram-bot library**  
[Documentation](https://docs.python-telegram-bot.org/en/v21.5/)  
[Examples](https://docs.python-telegram-bot.org/en/v21.5/examples.html)  
# My bots
**1. @armenian_robot** - [Link](https://t.me/armenian_robot)  
Bot uses **Anthropic's** `claude-3-7-sonnet-20250219` model  

Use /start command to
- correct any texts
- translate any texts into any language
- 
Use /power_cuts command to
- get information about power cuts
- subscribe to get messages whenever bot notices power cuts at your address

The bot scrapes data from [the Electric Networks of Armenia webpage](https://www.ena.am/Info.aspx?id=5&lang=1) at a specified interval (12 hours). Using RegEx, the extracted data is converted into a Pandas DataFrame with the following columns: Date, Region, Time, and Addresses. The bot then iterates over each row of the DataFrame and sends a message to subscribers whose address appears in that row's Addresses column. To prevent duplicate notifications, it ensures that each subscriber receives a message only if the Date and Time pair in that row is new to them.

Along with other commands, Bot has a command `/geography` which gives a lot of information about geography in a very fun way
