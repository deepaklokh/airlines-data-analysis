# Airline Flight Occupancy Analysis

## Project Description

This project analyzes an airline's flight, booking, and ticketing data to identify opportunities for increasing seat occupancy on low-performing flights. By exploring patterns in revenue, booking trends, and aircraft utilization, the goal is to provide actionable insights to improve profitability.

## Dataset Overview

The analysis uses the `travel.sqlite` database containing tables such as:

- `flights`: Flight schedules and aircraft info  
- `bookings` & `tickets`: Booking and ticket details  
- `aircrafts_data` & `seats`: Aircraft specifications and seat layouts  
- Additional tables for airports, boarding passes, and fare conditions

## Technologies & Tools

- SQLite (SQL queries for data extraction)  
- Python (data cleaning and analysis)  
- Pandas (data manipulation)  
- Matplotlib & Seaborn (visualizations)  

## Key Features & Analysis Highlights

- Connected to and explored the airline database  
- Cleaned and validated data integrity  
- Analyzed aircraft seat capacities and occupancy rates  
- Visualized booking trends and revenue patterns over time  
- Examined fare conditions’ impact on ticket prices and occupancy  

## How to Run

1. Clone/download the repository  
2. Ensure Python 3.x and libraries (`pandas`, `matplotlib`, `seaborn`, `sqlite3`) are installed  
3. Place `travel.sqlite` database in the project folder  
4. Run the Jupyter Notebook to see analysis, visualizations, and insights  

## Sample SQL Queries

```sql
-- Find aircraft with more than 100 seats
SELECT aircraft_code, COUNT(*) as num_seats 
FROM seats 
GROUP BY aircraft_code 
HAVING num_seats > 100;

-- Average ticket price by aircraft and fare condition
SELECT fare_conditions, aircraft_code, AVG(amount) AS avg_amount 
FROM ticket_flights
JOIN flights ON ticket_flights.flight_id = flights.flight_id
GROUP BY aircraft_code, fare_conditions;

```

## Results & Conclusion

The analysis reveals that certain aircraft models consistently have low occupancy rates
indicating opportunities for targeted marketing or dynamic pricing.
Booking trends also suggest seasonality effects, which can inform scheduling and promotions.

---

## Author

**Deepak Anand Lokhande**  
  Data Analyst  

> - [LinkedIn](https://www.linkedin.com/in/deepak-lokhande-82a887342/)
> - [GitHub](https://github.com/yourgithub)  
> - deepak50384297@gmail.com
