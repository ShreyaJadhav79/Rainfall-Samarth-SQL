-- 🌧️ Project Samarth – Rainfall Q&A System (SQL Prototype)
-- Fellowship: Build for Bharat (Data Science Track)
-- Created by: Shreya Jadhav
-- Goal: Compare rainfall trends between Indian states using open data from data.gov.in

-- Step 1: Create rainfall table
CREATE TABLE rainfall_data (
    State VARCHAR(50),
    Year INT,
    Month VARCHAR(20),
    Rainfall_mm FLOAT
);

-- Step 2: Insert sample rainfall data (based on IMD rainfall dataset format)
INSERT INTO rainfall_data (State, Year, Month, Rainfall_mm) VALUES
('Maharashtra', 2018, 'June', 215.6),
('Maharashtra', 2018, 'July', 450.3),
('Maharashtra', 2019, 'June', 198.2),
('Maharashtra', 2019, 'July', 422.6),
('Gujarat', 2018, 'June', 180.4),
('Gujarat', 2018, 'July', 375.8),
('Gujarat', 2019, 'June', 165.9),
('Gujarat', 2019, 'July', 358.1),
('Karnataka', 2018, 'June', 230.2),
('Karnataka', 2018, 'July', 460.8),
('Karnataka', 2019, 'June', 205.4),
('Karnataka', 2019, 'July', 440.1);

-- Step 3: Compare average rainfall between states (2018–2019)
SELECT 
    State,
    ROUND(AVG(Rainfall_mm), 2) AS Average_Rainfall
FROM rainfall_data
WHERE Year BETWEEN 2018 AND 2019
GROUP BY State
ORDER BY Average_Rainfall DESC;

-- Step 4: Find the month with highest rainfall in a state
SELECT 
    Year, 
    Month, 
    Rainfall_mm
FROM rainfall_data
WHERE State = 'Maharashtra'
ORDER BY Rainfall_mm DESC
LIMIT 1;

-- Step 5: Show rainfall trend by year for a state
SELECT 
    Year,
    ROUND(AVG(Rainfall_mm), 2) AS Avg_Rainfall
FROM rainfall_data
WHERE State = 'Gujarat'
GROUP BY Year
ORDER BY Year ASC;
