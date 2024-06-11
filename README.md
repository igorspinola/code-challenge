# Indicium Tech Code Challenge

Code challenge for Software Developer with focus in data projects.


## Context

My solution steps are provided on folders solution/first_step and solution/second_step. Both are scheduled using airflow with the @daily directive on their respective meltano.yml configuration files.

The first step consists of executing the command "meltano run tap-postgres target-csv" on the solution/first_step directory in an UNIX-like terminal or WSL2. It runs the pipeline taking the data from northwind PostgreSQL database, transforming it to CSV format and outputs it in the solution/first_step/csv_first_output/postgres directory. On solution/first_step/csv_first_output/csv, there is the csv order_details file originally provided for the challenge. 

The second step is executing "meltano run tap-csv target-postgres" on the solution/second_step directory, which transforms back the CSV collected data to a new PostgreSQL database, this time with order_details included.
