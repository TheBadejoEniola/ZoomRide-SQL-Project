# ZoomRide-SQL-Project

## Overview
ZoomRide is a ride-hailing company operating in 6 cities: Lagos, Abuja, Port Harcourt, Nairobi, Accra and Kampala. The manager wanted to know which city earns the most, which month is busiest, and which vehicle type earns the most. The data was messy, so I cleaned it first and then analysed it with SQL (MySQL on OneCompiler).

## My Process
1. **Looked at the data:** checked the trips table (300 rows).
2. **Found the problems:**
   - City names were spelled wrongly or had extra spaces (PH, Port-Harcourt, Nairobbi, Kampla, ' Lagos', ' Accra'), giving 12 city names instead of 6.
   - 2 trips were saved twice (trips 82 and 299, trips 253 and 300).
   - 9 completed trips have no fare recorded.
3. **Cleaned the data:** trimmed spaces, fixed the city spellings, and deleted the duplicate rows (299 and 300). That left 6 cities and 298 rows. I did not fill in the 9 missing fares. They stay empty (NULL).
4. **Analysed the clean data** using completed trips only, since cancelled trips earn nothing.

## Answers to the Manager's Questions

**1. Which city earns the most money?**
Lagos, with ₦218,890 from 93 completed trips. Accra is second with ₦92,640.

| City | Trips | Revenue (₦) | Avg fare (₦) |
|---|---|---|---|
| Lagos | 93 | 218,890 | 2,405.38 |
| Accra | 37 | 92,640 | 2,807.27 |
| Abuja | 36 | 88,720 | 2,464.44 |
| Port Harcourt | 31 | 71,240 | 2,374.67 |
| Nairobi | 32 | 58,960 | 1,901.94 |
| Kampala | 19 | 38,020 | 2,112.22 |

**2. Which month do people ride the most?**
December 2025, with 31 trips and ₦66,980. May 2026 was second in revenue (₦64,140).

**3. Which type of vehicle earns the most money?**

| Vehicle type | Trips | Revenue (₦) |
|---|---|---|
| Economy | 121 | 262,550 |
| Comfort | 76 | 239,050 |
| Bike | 51 | 66,870 |

Economy earns the most.

## Bonus
- **Customers who never booked a trip:** Bisi Ogunleye, Wanjiru Kamau, Akinyi Ouma, Nakato Namutebi.
- **Top 3 customers by spend:** Chioma Nwosu (₦38,950, 21 trips), Tunde Bakare (₦37,610, 13 trips), Zainab Garba (₦35,380, 15 trips).

## Message to the Manager
I recommend that ZoomRide invests in Lagos, which made ₦218,890 from 93 completed trips, more than twice Accra’s ₦92,640. I found two data issues: some city names were written differently, and two trips were duplicated. Without cleaning the data, the results would have been inaccurate. Some completed trips also have no fare recorded, so the actual revenue may be slightly higher. 


## Data Note
Some completed trips have no fare recorded, so the revenue is slightly understated.

## Files
- (zoomride_eniola.sql)[setup script and all my queries (Q1 to Q10), in order]
- README.md
