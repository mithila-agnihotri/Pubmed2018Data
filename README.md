# Pubmed2018Data
Analysis  of research articles from Jan 2018 to March 2018 as obtained from Pubmed

## Data Files
For this analysis, I obtained the data by querying the PubMed database for research articles published between Jan and March 2018. I downloaded the results in the .xml format. It was a relatively large dataset (size: ~ 4 GB).

I also used University ranking data obtained as a file from Kaggle: https://www.kaggle.com/mylesoneill/world-university-rankings/data. This file contains a list of Universities in the world sorted by their rank. 

## Analysis
In order to parse the xml file, I used the xml.etree.cElementTree module. From this module I used the iterparse method. The advantage of this method is that it does not generate and store the entire xml data tree in the beginning itself. Instead it iteratively reads each node in the tree which allows us to delete nodes which we do not require while reading the file. This is advantageous as we can now read this large file in a memory efficient way by only storing the information that is of interest to us.

First, I read the file as described above and for each publication record, stored its Authors list, Grant ID list, Keywords list and Author affiliations.   

## Results
Using this information, I first looked at the percentage of total publications that come from top 10 Universities in different countries – 3% in US, 3.5% in China, 0.3% from India and 2.6 % from Japan.

Next I looked at the number of publications from US Universities. Among the top 10, John Hopkins had the highest with 2427 publications in 3 months while Cal Tech was the least with 222 publications. 

I also looked at which research fields are being investigated more heavily than others. Among the following research fields -  cancer,alzheimer,hiv,diabetes,autism,machine learning,neural networks,deep learning – cancer is the most heavily researched field with over 15,000 publications in just three months.

Lastly, I investigated which Universities and research scientists are top publishers in the above mentioned research fields.  
