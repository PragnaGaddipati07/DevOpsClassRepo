Case -1 
env file looks like below
APP_PORT =hello
DEBUG=true
DB_HOST =

PS C:\Users\pragnag\DevOpsClassRepo> py validator.py bad-port.env.example
>> $LASTEXITCODE
APP_PORT must be an integer in 1024..65535
DEBUG must be false
DB_HOST must be nonempty
1

Case -2
It is a successful case
PS C:\Users\pragnag\DevOpsClassRepo> py validator.py valid.env.example
>> $LASTEXITCODE
Configuration accepted
0

Case -3
APP_PORT contains value "hello"
PS C:\Users\pragnag\DevOpsClassRepo> py validator.py messy.env
>> $LASTEXITCODE
APP_PORT must be an integer
DEBUG must be false
DB_PASSWORD must be nonempty
1

Case -4
Here one of the variable is in lowercase.It should be in snake_case.
app_port=80
DB_PASSWORD=example-only-placeholder

PS C:\Users\pragnag\DevOpsClassRepo> py validator.py bad-port.env.example
>> $LASTEXITCODE
APP_PORT must be an integer in 1024..65535
DEBUG must be false
DB_HOST must be nonempty
app_port must be uppercase (did you mean APP_PORT?)
1