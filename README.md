# ADS-2
**AIM:**
    
    To Perform Data Collection through web scraping using python.

**ALGORITHM:**
	Step 1: Include the Necessary python libraries.
 
	Step 2: Use the requests library to send HTTP requests to a web page.
 
	Step 3: Retrieve the HTML content and use BeautifulSoup to parse it.
 
	Step 4: Navigate and extract the necessary data.
 
	Step 5: Handle the Java script content and retrieve the data using the html tags.
 
	Step 6: Check with the website permission and scrap the content.

**CODING & OUTPUT:**
```
pip install beautifulsoup4 requests
import requests
from bs4 import BeautifulSoup
import pandas as pd
url = 'https://www.w3schools.com/html/html_tables.asp'
response = requests.get(url)
```
![image](https://github.com/user-attachments/assets/d1e875bb-c1de-4bce-afe3-a4204002432d)

```
response
soup = BeautifulSoup(response.content, 'html.parser')
headings = soup.find_all('h2')
for heading in headings:
  print(heading.text)
```

![image](https://github.com/user-attachments/assets/bc5f073b-0a10-4fa8-8942-89caa7a475e1)

```
data = []
for heading in headings:
  data.append(heading.text)
df=pd.DataFrame(data)
df.to_csv('newdata.csv', index=False)
df.head()
```
![image](https://github.com/user-attachments/assets/89f4a4ed-22e2-47d8-b2a3-879fe4cd1779)

**RESULT:**
Thus ,the program To Perform Data Collection through web scraping using python is successfully implemented.
