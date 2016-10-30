#Dengue Alert Apps

This android application developed during “48 Jam Hackathon Data Terbuka Sektor Awam 2016” organized by MAMPU. The hackathon start by 10.30 am, 25 Oct 2016 and en by 10.30 am, 27 Oct 2016.

##Introduction

What is Dengue Alert?

Dengue Alert is an application that is developed to help the user to visualized and understand the threat of Dengue Fever. 

The application will visualized the number of cases and the rate of mortality.

This application will also forecast the number of cases for the following year.

##Dataset

###[data.gov.my](http://www.data.gov.my/)

- http://www.data.gov.my/data/ms_MY/dataset/senarai-lokaliti-hotspot-wabak-denggi-di-malaysia

- http://www.data.gov.my/data/ms_MY/dataset/jumlah-kes-keseluruhan-wabak-denggi-yang-telah-dilaporkan-di-malaysia

- http://www.data.gov.my/data/ms_MY/dataset/jumlah-kes-kematian-akibat-wabak-denggi-yang-telah-dilaporkan-di-malaysia

- http://data.gov.my/data/ms_MY/dataset/population-and-demographic-statistics-malaysia

###[google.com/trends](https://google.com/trends)

- "Denggi" keywords from 2010 to 2015

##Data Pre-Processing

##Data Visualization


The features in Dengue Alert are more to data visualization where the data will be display in a form of graph, heatmap and table. Below is the screenshot of our main page in the application.

###Current Cases

<p align="center">
<img src="https://i.imgur.com/hG6IbPV.jpg" alt="Screenshot"  width="320"/>
</p>

In this section, it shows statistic from 2016, the number of current cases for one day and the total number of cases for the current year. This is a real time data where we get it from http://idengue.remotesensing.gov.my/. From this statistic it is obvious that Selangor lead the total number of cases by 45,827 cases, followed by Johor with 9,776 cases. State with minimum cases goes to WP Labuan, maybe because of the population which is less than other states. Below the 2016 statistic is the number of cases and death of dengue from 2010 to 2015. Total number of cases is 245,570, and total number of death is 548. 


###Total Cases and Death of Dengue

Then go to the Total Cases section where it display the statistic of total cases and death between 2010 until 2015.

<p align="center">
<img src="http://i.imgur.com/UQrX9LP.jpg" alt="Screenshot"  width="320"/>
</p>

The total cases increase every year except for 2010 to 2011 where the cases decreased. From 2013 to 2014 the cases drastically increasing from 40,831 to 87,503 cases which is 143% increment. From 2014 to 2015 also increase by 21% which is 109,027 cases. This conclude that every year dengue cases will increasing.

<p align="center">
<img src="http://i.imgur.com/YLtOpli.jpg" alt="Screenshot"  width="320"/>
</p>

This graph show total death of dengue cases from 2010 to 2015. Same goes to the graph of dengue cases above, this graph also show increasing in number of death, which in 2015 is the highest total death, 293 cases. The lowest case is in year 2011 with 33 cases. Average death from 2010 to 2015 is 121.8 death because of dengue.


###Cases Comparison

Below is the graph for Cases Comparison section, where the total number of cases is visualized in radar. From the graph here we group some states except Selangor and Wilayah Persekutuan. 

<p align="center">
<img src="http://i.imgur.com/zqFTDCM.jpg" alt="Screenshot"  width="320"/>
</p>

<table>
  <tr>
  <th>Label Name</th>
  <th>States</th>
  </tr>
  <tr>
  <td>Northern</td>
  <td>Perlis, Kedah, Perak and Pulau Pinang</td>
  </tr>
  <tr>
  <td>Southern</td>
  <td>Melaka, Negeri Sembilan, Johor</td>
  </tr>
  <tr>
  <td>Eastern</td>
  <td>Pahang, Terengganu, Kelantan</td>
  </tr>
  <tr>
  <td>SS</td>
  <td>Sabah, Serawak</td>
  </tr>
 </table>
	
The reason why the states being group is because the total cases is too small compared to Selangor, when the graph is displayed for the first time (separate all the states), only Selangor can be seen in the graph. The other states is hidden from there because of small number in total of cases.

###Google Trends x Total Number of Cases/Week (2010-2015)

TO-DO

##Prediction

<p align="center">
<img src="http://i.imgur.com/pjmHl9H.jpg" alt="Screenshot"  width="320"/>
</p>

The above graph is for forecasting. Linear Regression technique is used to forecast where total population and increment of population are independent variable, while total number of dengue cases per week as dependent variable. In this graph, x-axis is Year, y-axis are total population, total number of dengue cases and total number of dengue cases predicted.

<p align="center">
<img src="http://i.imgur.com/RYEgf1w.png" alt="Screenshot"  width="640"/>
</p>

Below is the equation generated for Linear Regression technique:

Calculate Average Cases Per Week: 

> Average= (Sum(Week 1 :Week 52))/52

Calculate Increment of Population:

> Increment = (Year -Previous Year)/Previous Year * 100

> Predicted Population = Population * Increment

Linear Regression Equation:

> Predicted Average Cases/Week = -2548.1042 + (9.2441 * Predicted Population) + (-71.6842 * Increment)

The equation explain that if predicted population increase one unit then the number cases will increase by 9.2441 unit. While increment population is increase, the number of cases will decrease by 71.6842 unit. 

The reason why we choose total population and increment population is shown in the graph below where it have the relationship with total number of cases per week. 

<p align="center">
<img src="http://i.imgur.com/chDlRXg.png" alt="Screenshot"  width="320"/>
</p>

<p align="center">
<img src="http://i.imgur.com/Fn5zs1r.png" alt="Screenshot"  width="320"/>
</p>


##Conclusion

In conclusion, increase awareness of dengue among Malaysian is a must. By using this application, hope it may alert the user to be more aware of their surrounding and take an action to prevent dengue mosquito from breeding such as frequently checking and removing stagnant water in their premises.
