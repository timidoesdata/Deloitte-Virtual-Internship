# Deloitte-Virtual-Internship
I answered key questions using telemetry data from a manufacturing company, and created an interactive dashboard to visualize problem areas. This is my input for the Forage X Deloitte Virtual Analytics internship. 

## Introduction
Every minute of downtime in manufacturing leads to revenue loss, delayed production, and inefficiencies. One of Deloitte Australia’s clients, Daikibo, has been facing frequent interruptions on their assembly lines, and they need answers. They provided telemetry data collected from four of their branches in Tokyo, Osaka, Berlin, and Shenzhen and I was to uncover the root causes of the frequent breakdowns.<br> 

The [dataset](https://cdn.theforage.com/vinternships/companyassets/9PBTqmSxAf6zZTseP/daikibo-telemetry-data.json.zip) consists of machine logs from nine different machine types, recorded every ten minutes throughout May 2021. Using this data, I was able to answer key questions such as;<br>
- Which factory experienced the most machine breakdowns?
- Which machines were most frequently affected in that factory?<br>

**Tools used:**
To achieve this, I used only Tableau to visualize patterns, create calculated fields, and design an interactive dashboard for stakeholders to easily identify problem areas.

# TASK ONE

## Step one:
I opened Tableau and connected to a file, selecting 'JSON' because the dataset was provided in a .json file. I loaded the telemetry data, and then extracted the relevant columns. 

## Step two:
Next, I created the 'unhealthy' calculated field, which assigns 10 minutes of downtime for every unhealthy status inputted, using the formula below:
```
IF [status] = "unhealthy" THEN 10 ELSE 0 
```

## Step three:
I then created the ***'Downtime Per Factory'*** chart, showing that the **Seiko** factory experienced the most downtime, and the Berlin factory the least. 

![image](https://github.com/user-attachments/assets/0a6bdaf2-66cb-429f-9f3c-07b4b96942b6)

## Step four: 
I created a new sheet to visualize ***'Downtime Per Device Type'***, and it shows that the **Laser Welder** broke down the most, while the CNC, Conveyor Belt, and Spot Welder broke down the least, however, the Air Wrench and Metal Press did not record any issues. 

![image](https://github.com/user-attachments/assets/2861b966-a078-4669-908e-49c53ca72101)

## Step five:
I created a new dashboard and added both charts to it, setting the ***'Downtime Per Factory'*** one as filter to help see the machines performance for any factory I select. As instructed, I selected the factory with the highest downtime, Seiko,  to see the most affected machine which was the **Laser Welder.**

![image](https://github.com/user-attachments/assets/91176738-2e1d-4dd9-9d8f-1ff110147183)

## Conclusion:
By following this process, I was able to show the factories and their machine failures levels and identify the most problematic machines across these locations. 

# TASK TWO 

Daikibo has received internal complaints about gender pay inequality across various job roles and locations, and to address this, the Forensic Tech team developed an algorithm that quantifies gender pay equality using an Equality Score. My task is to analyze the Equality Table, classify job roles based on fairness, and document my findings.

The [dataset](https://cdn.theforage.com/vinternships/companyassets/9PBTqmSxAf6zZTseP/Task%205%20Equality%20Table.xlsx) includes the following columns:
- Factory 
- Job Role 
- Equality Score ranging from -100 to +100, with 0 as the ideal score.
  
The task is to create a fourth column separating job roles according to the ratings below:
- Fair (-10 to +10)
- Unfair (<-10 AND >10)
- Highly Discriminative (<-20 AND >20)

**Tools used:**
I used Microsoft Excel for this task. 

## Step one:
I loaded the dataset into Excel and applied filters to check for blanks, spelling error repititions of which there were none. I also auto-fitted column with for a better look and boldened the column titles. I correctly formatted the data type for each column. 

## Step two:
I created the fourth column titled ***Equality class***, and applied the *IF* function formula below to the first cell D2:
```
=IF(AND(C2>=-10,C2<=10),"Fair",IF(OR(C2<-20,C2>20),"Highly Discriminative","Unfair"))
```

![image](https://github.com/user-attachments/assets/2b8bbd40-06f8-4b45-9fb2-e5f2dadeab11)

## Conclusion
By completing this process, I have classified job roles based on gender pay equality to help Daikibo Industrials to identify job roles and factories where inequality exists so that leadership can take necessary corrective measures.





  










