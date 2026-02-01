# DE Zoomcamp-HW1

**Question 1:** 25.3
<img width="1729" height="95" alt="image" src="https://github.com/user-attachments/assets/b59783ce-6e12-437e-b31f-c00db01bf252" />

**Question 2:** 
Host: postgres (the container name)
Port: 5432
Username: postgres
Password: postgres

<img width="1238" height="894" alt="image" src="https://github.com/user-attachments/assets/a8b83dd1-7eb4-4e3e-ae16-23190e18f16c" />

**Question 3:** 
```sql
SELECT COUNT(*)
FROM ny_taxi_data
WHERE trip_distance <= 1
AND lpep_pickup_datetime >= '2025-11-01'
AND lpep_pickup_datetime <  '2025-12-02';
```

<img width="762" height="312" alt="image" src="https://github.com/user-attachments/assets/d7da1763-114a-439d-aedf-8fbde0e83c83" />

**Question 4:** 
```sql
SELECT lpep_pickup_datetime, trip_distance
FROM ny_taxi_data
WHERE trip_distance < 100
ORDER BY trip_distance DESC
LIMIT 1;
```

<img width="873" height="319" alt="image" src="https://github.com/user-attachments/assets/fda9f67b-fd64-45c9-9830-5737681cc994" />

**Question 5:** 
```sql
SELECT
	zpu."Zone" AS "pickup_loc",
    SUM(t.total_amount) AS total_amount
FROM
    ny_taxi_data t
JOIN
    ny_taxi_zone zpu ON t."PULocationID" = zpu."LocationID"
WHERE lpep_pickup_datetime >= '2025-11-18' AND lpep_pickup_datetime < '2025-11-19'
GROUP BY pickup_loc
ORDER BY total_amount DESC
LIMIT 1;
```

<img width="814" height="268" alt="image" src="https://github.com/user-attachments/assets/ed75a7b7-cedf-417c-b366-b61a5e760300" />

**Question 6:**
```sql
SELECT 
    zdo."Zone" AS dropoff_zone,
    MAX(d.tip_amount) AS largest_tip
FROM ny_taxi_data d
JOIN ny_taxi_zone zpu 
    ON d."PULocationID" = zpu."LocationID"
JOIN ny_taxi_zone zdo 
    ON d."DOLocationID" = zdo."LocationID"
WHERE 
    zpu."Zone" = 'East Harlem North'
    AND d.lpep_pickup_datetime >= '2025-11-01'
    AND d.lpep_pickup_datetime < '2025-12-01'
GROUP BY zdo."Zone"
ORDER BY largest_tip DESC
LIMIT 1;
```

<img width="645" height="249" alt="image" src="https://github.com/user-attachments/assets/f09e95a0-3234-4d2f-a7f2-752d8949441b" />

**Question 7:** terraform init, terraform apply -auto-approve, terraform destroy
