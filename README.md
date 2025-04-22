## Overview
The dataset provides comprehensive details on simulated train ticket sales for National Rail in the United Kingdom, covering the period from January to April 2024. It includes various essential attributes such as the type of ticket purchased, the exact date and time of each journey, the departure and arrival stations, and the ticket price. Additionally, the dataset may encompass other relevant aspects for analysis, including different fare categories, applied discounts, service classes available, and price variations based on demand, travel periods, and specific routes. This information offers valuable insights into ticketing trends, passenger preferences, and potential fluctuations in rail travel patterns during the given timeframe.
## Objectives
The dataset aims to:
-	Provide delay time for the journey.
-	Explore data and time for purchase ticket and his price.
-	The reason for cancelled trips and minimize cancelled trips.
-	Understand reason for delayed trips and provide refund request.
-	improve stations that departure station and arrival station.
-	The peak of purchase ticket per hour and optimize purchasing. 
## Data Source and Description
The dataset originates from UK Train Rides a railway in UK that the passenger in UK use it to travel between stations. It encompasses information on approximately 31653 ticket purchase from January to April 2024. The data include various aspects of the railway and trips, including:
-	**Railway table**: Information on each transaction ID, purchase details, ticket details, railcard and if have railcard or not and payment method.
-	**Trips table**: trips ID, departure and arrival station, details for delay, details of journey and departure and Arrival Coordinates
-	**Dim Journey Date table**: date, time and week day typer
-	Station:  the station name and coordinates

-	**Ticket details**: ticket price, type and class.
-	**Purchase information**: date and time, type, payment method, Days Between Purchase a journey and Purchase Hour.
-	**Journey details**: trip ID, date, day of journey, departure and arrival time, actual arrival time, status, delay time, reason for delay.
-	**Station information**: coordinates, departure and arrival. 
## Key Columns
| Column    | Description |
| -------- | ------- |
| Transaction ID| Unique identifier for each ticket purchase transaction.|
| Date of Purchase|  The date on which the ticket was purchased. | 
| Time of Purchase |The time on which the ticket was purchased. |
| Purchase Type | Where the ticket was purchased: Online or at the Station. |
| Payment Method| Payment method used to purchase the ticket (Contactless, Credit Card, or Debit Card).|
| Railcard | Whether the passenger is a National Railcard holder (Adult, Senior, or Disabled) or not (None). Railcard holders get 1/3 off their ticket purchases.|
| Ticket Class | Seat class for the ticket (Standard or First). |
| Ticket Type | When you bought or can use the ticket. Advance tickets are 1/2 off and must be purchased at least a day prior to departure. Off-Peak tickets are 1/4 off and must be used outside of peak hours (weekdays between 6-8am and 4-6pm). Anytime tickets are full price and can be bought and used at any time during the day.|
| Ticket Price | Price of the individual ticket. |
| Departure Station | The station from which the train journey begins. |
|Arrival Destination| The station where the train journey ends. |
|Journey Date| The date of the actual train journey. |
|Departure Time| Time the train departed. |
|Arrival Time| Time the train was scheduled to arrive at its destination (can be on the day after departure).|
|Actual Arrival Time| Time the train arrived at its destination (can be on the day after departure).|
|Journey Status| Whether the train was on time, delayed, or cancelled. |
|Reason for Delay| Reason for the delay or cancellation. |
|Refund Request| Whether the passenger requested a refund after a delay or cancellation.|

**Additional Custom Columns Created:**
-	Origin-destination: merged to column departure station and arrival destination.
-	Delay time(minutes): the difference between arrival time and actual arrival time.
-	Merged column: merge origin-destination, date of journey and departure time. 
-	Purchase Hour: extracted hour from Purchase Time column.
Data Analysis questions:
**Performance Analysis**
1-	What percentage of total trips were cancelled or delayed?
2-	Which routes experience the highest number of delays or cancellations?
3-	Is there a relationship between the number of trips on a route and the delay/cancellation rate?
**Revenue Analysis**
4-	Which routes generate the most revenue, and how does that correlate with trip volume or punctuality?
5-	What is the revenue loss due to cancelled or delayed trips?
6-	Is there a seasonal or monthly trend in revenue, delays, or cancellations?
**Route Optimization**
7-	Which routes have the lowest performance (e.g., highest cancellations) and lowest revenue — candidates for reevaluation or discontinuation?
8-	Which underperforming routes still bring in high revenue, possibly indicating essential services despite inefficiency?
**Operational Efficiency**
9-	Are certain time periods (days of the week, months) more prone to delays or cancellations?
10-	What are the average delay durations per route or trip type?
**Comparative Questions**
11-	How do high-performing routes differ from low-performing ones in terms of trips, revenue, and delays?
12-	what is the trend of trip volume and performance over time — is it improving or declining?
