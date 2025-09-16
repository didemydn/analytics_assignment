# analytics_assignment

**How to start this project**

I began by creating an account to use BigQuery, Google Cloud Console (GCC) Shell, and dbt.
Then I created a project on Google Cloud Console.
As mentioned in the assignment document:
I found a free CSV file on GCC.
I created a Cloud Storage bucket.
I uploaded the dataset there and used it to start Task 1.

**Task 1 Load & Transform Data**

- Created Cloud Storage bucket and uploaded the CSV file.
- Created a dataset analytics_assignment in BigQuery.
- Loaded the CSV into a RAW table (schema autodetected).
- Created a FINAL table:
Converted event_date to DATE.
- Partitioned by event_date.
- Clustered by event_name.
- Verified data with a query for January 2021, which showed the most frequent events.

**Task 2 – dbt Setup & Staging Models**

- Installed dbt in Google Cloud Shell.
- Initialized a new dbt project ga4_assignment.
- Configured profiles.yml to connect dbt to BigQuery.
- Created staging models (stg_ga4_events) to:
Clean raw GA4 events.
- Convert types (DATE, STRING, FLOAT).
- Standardize naming.
- Added schema tests to validate fields (not_null, accepted_values).
- Successfully ran dbt models and validated results in BigQuery.

**Task 3 – Metrics & Final Models**

- Built final models (fct + views) in dbt.
- Created metrics such as:
events_per_month.
- Aggregated event counts.
- Validated metrics in BigQuery by running SQL queries.

**What I Learned
As a software developer, I learned how to:**

* Use Google Cloud Storage + BigQuery together for data pipelines.
* Configure and run dbt inside Google Cloud Shell.
* Design staging and final models with transformations and tests.
* Understand the importance of schema design (partitioning, clustering).
* Work step by step on a real-world analytics engineering workflow.
* This assignment helped me strengthen my SQL, dbt, and cloud data engineering skills.

**How AI Helped Me as a Trainee**
Since this was my first experience with **BigQuery + dbt + Google Cloud Shell**, I faced challenges at almost every step.
- **Breaking down complex tasks** → When the assignment instructions were high-level, AI explained them step by step (e.g., how to create buckets, how to initialize dbt, why we partition/cluster).
- **Debugging errors**→ Whenever I got stuck (for example, dbt profile connection errors or missing dataset references), AI guided me through debugging.
- Improve SQL queries, dbt models, and even schema.yml test definitions.

