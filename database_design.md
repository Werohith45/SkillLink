# SkillLink Database Design

## Table 1: Workers

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| worker_id | INT | Unique worker ID |
| name | VARCHAR(100) | Worker name |
| phone | VARCHAR(15) | Phone number |
| email | VARCHAR(100) | Email address |
| skill | VARCHAR(100) | Worker skill |
| location | VARCHAR(100) | City/Area |
| experience | INT | Years of experience |
| rating | FLOAT | Average rating |
| availability | VARCHAR(50) | Available/Busy |

## Table 2: Businesses

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| business_id | INT | Unique business ID |
| business_name | VARCHAR(100) | Business name |
| owner_name | VARCHAR(100) | Owner name |
| phone | VARCHAR(15) | Contact number |
| email | VARCHAR(100) | Email address |
| location | VARCHAR(100) | Business location |
| rating | FLOAT | Average rating |

## Table 3: Jobs

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| job_id | INT | Unique job ID |
| business_id | INT | Business posting the job |
| skill_required | VARCHAR(100) | Required skill |
| salary | DECIMAL(10,2) | Salary offered |
| location | VARCHAR(100) | Job location |
| job_date | DATE | Work date |
| work_hours | INT | Number of hours |
| description | TEXT | Job description |
| status | VARCHAR(50) | Open/Closed |

## Table 4: Applications

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| application_id | INT | Unique application ID |
| worker_id | INT | Applicant worker |
| job_id | INT | Applied job |
| application_date | DATE | Date applied |
| status | VARCHAR(50) | Pending/Accepted/Rejected |

## Table 5: Ratings

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| rating_id | INT | Unique rating ID |
| worker_id | INT | Rated worker |
| business_id | INT | Rating business |
| rating_value | INT | Rating (1-5) |
| comment | TEXT | Review comment |

## Relationships

- One Business can post many Jobs.
- One Worker can apply to many Jobs.
- One Job can receive many Applications.
- Workers and Businesses can rate each other after completion.
