1. Which entry has an invalid data type?
 APP_PORT. It has string but it should be integer.
2. Which entry violates the deployment debug policy?
 DEBUG = true, because it shows all the details and errors to users.
3. Which required setting is empty?
 DB_PASSWORD
4. Which two names appear to represent the same concept, and which spelling does the contract require?
dbhost and DB_HOST appear to reprsent the hostname but all the name sin .env should be in Snake case.So DB_HOST is valid one.

Rules:
1. `APP_PORT`: required integer between 1024 and 65535, inclusive.
2. `DEBUG`: required literal `false`, with exact case.
3. `DB_HOST`: required and nonempty; `dbhost` is not an alias.
4. `DB_PASSWORD`: required and nonempty; never display its value.
5. All variables should be in snake_case