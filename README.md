# DA-462-Project

Constructed an independent data analysis for a project.

## Table of Contents

- [DA-462-Project](#da-462-project)
  - [Table of Contents](#table-of-contents)
  - [Project Description](#project-description)
  - [Dataset](#dataset)
  - [Data Dictionary](#data-dictionary)
  - [Research Questions](#research-questions)
  - [Methods](#methods)
  - [Results](#results)
  - [Contact](#contact)

## Project Description

This project is designed to simulate a real-world analytics task, where you must define the problem, determine the approach, and clearly explain the results.

## Dataset

- **Source:** https://github.com/rfordatascience/tidytuesday/tree/main/data/2020/2020-02-11
- **Description:** The data comes from an open hotel booking demand dataset from Antonio, Almeida and Nunes, 2019.

## Data Dictionary

| variable                       | class     | description                                                                                                                                                                                                                                                                 |
| :----------------------------- | :-------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| hotel                          | character | Hotel (H1 = Resort Hotel or H2 = City Hotel)                                                                                                                                                                                                                                |
| is_canceled                    | double    | Value indicating if the booking was canceled (1) or not (0)                                                                                                                                                                                                                 |
| lead_time                      | double    | Number of days that elapsed between the entering date of the booking into the PMS and the arrival date                                                                                                                                                                      |
| arrival_date_year              | double    | Year of arrival date                                                                                                                                                                                                                                                        |
| arrival_date_month             | character | Month of arrival date                                                                                                                                                                                                                                                       |
| arrival_date_week_number       | double    | Week number of year for arrival date                                                                                                                                                                                                                                        |
| arrival_date_day_of_month      | double    | Day of arrival date                                                                                                                                                                                                                                                         |
| stays_in_weekend_nights        | double    | Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel                                                                                                                                                                               |
| stays_in_week_nights           | double    | Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel                                                                                                                                                                                    |
| adults                         | double    | Number of adults                                                                                                                                                                                                                                                            |
| children                       | double    | Number of children                                                                                                                                                                                                                                                          |
| babies                         | double    | Number of babies                                                                                                                                                                                                                                                            |
| meal                           | character | Type of meal booked. Categories are presented in standard hospitality meal packages: <br> Undefined/SC – no meal package;<br>BB – Bed & Breakfast; <br> HB – Half board (breakfast and one other meal – usually dinner); <br> FB – Full board (breakfast, lunch and dinner) |
| country                        | character | Country of origin. Categories are represented in the ISO 3155–3:2013 format                                                                                                                                                                                                 |
| market_segment                 | character | Market segment designation. In categories, the term "TA" means "Travel Agents" and "TO" means "Tour Operators"                                                                                                                                                              |
| distribution_channel           | character | Booking distribution channel. The term "TA" means "Travel Agents" and "TO" means "Tour Operators"                                                                                                                                                                           |
| is_repeated_guest              | double    | Value indicating if the booking name was from a repeated guest (1) or not (0)                                                                                                                                                                                               |
| previous_cancellations         | double    | Number of previous bookings that were cancelled by the customer prior to the current booking                                                                                                                                                                                |
| previous_bookings_not_canceled | double    | Number of previous bookings not cancelled by the customer prior to the current booking                                                                                                                                                                                      |
| reserved_room_type             | character | Code of room type reserved. Code is presented instead of designation for anonymity reasons                                                                                                                                                                                  |
| assigned_room_type             | character | Code for the type of room assigned to the booking. Sometimes the assigned room type differs from the reserved room type due to hotel operation reasons (e.g. overbooking) or by customer request. Code is presented instead of designation for anonymity reasons            |

## Research Questions

1.  Do city hotels or resort hotels have more children per booking?

2.  Which combinations of characteristics affect adr the most?

3.  Do repeated guest stay longer than first time guest?

4.  Is average daily rate lower for longer stays?

## Methods

This project was done in R using the hotel booking dataset from TidyTuesday. I looked at patterns in hotel bookings and tested how different booking characteristics were related to average daily rate (ADR).

- Loaded the hotel booking data from the source.
- Split the data into groups like city hotels vs. resort hotels and first-time guests vs. repeated guests.
- Created a `total_days_stayed` variable by adding weekday nights and weekend nights together.
- Used t-tests to compare average values between groups.
- Used linear regression and multiple regression to see which variables were related to ADR.
- Compared different regression models and kept the ones with the best adjusted $R^2$.

The main variables used in this project were hotel type, number of children, guest type, length of stay, lead time, and ADR.

## Results

The results showed a few clear patterns in the hotel booking data.

- Resort hotels had a little more children per booking than city hotels.
- Children, adults, babies, lead time, and weeknight stays were all useful for predicting ADR.
- Out of the variables tested, children had the biggest positive effect on ADR.
- First-time guests stayed longer on average than repeated guests.
- Longer stays were linked to a slightly higher ADR, but the effect was pretty small.

Overall, the results show that the type of booking and how long someone stays can help explain ADR, even though some of the differences were small in a practical sense.

## Contact

Made by Alex Copeland,
alexcopeland2020@gmail.com
