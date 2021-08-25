# MySQL-and-php-code-Job

## MySQL
Question 1

We first select the plan type name. Then we use the JOIN to join the plan, users and company together, using foreign keys between tables. Lastly we use the WHERE clause to find plan types with "Funeral Directors".

- SELECT plan.plan_type
- FROM Plan
- JOIN Users
- ON Plan.plan_lead_gen = Users.id
- JOIN Company
- ON Users.user_company = Company.company_id
- WHERE company_name = "Funeral Directors"

Question 2

We Select the company name, but we also count the number of rows. Next we connect our foreign keys to connect Plan, Users and Company together. We then use a WHERE clause to check which plan statuses are 'Pending Review' or 'Plan Active'. Finally we group by company name. We use the GROUP BY to ensure we get the number of claims per company. Together using the COUNT and GROUP BY functions we are getting the number of claims per company.

- SELECT company.company_name, COUNT(*)
- FROM Plan JOIN Users
- ON plan.plan_lead_gen = users.user_id
- JOIN Company
- ON users.user_company = company.company_id
- WHERE plan_status = "Plan Active" OR plan_status = "Pending Review"
- GROUP BY company_name

Question 3

Here I have documented how i have used PHP Code to construct a connection to form a MySQL Query to output the following:

Here I selected the plan_type, plan_lead_generator, the company_name and the pc_firstname and lastname. I joined the Company, Users, Plan, Plan_client & Payment tables together using their foreign keys.
I assumed the pc_plan_id from the PC Client table was a link to the plan table, therefore I linked them together and gathered the name of the clients who owned the insurance plan.

- I have documented the answer in my index.html file.

