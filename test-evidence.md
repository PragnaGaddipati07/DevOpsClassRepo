Case -1 
PS C:\Users\pragnag\DevOpsClassRepo> py validator.py bad-port.env.example
>> $LASTEXITCODE
APP_PORT must be an integer in 1024..65535
DEBUG must be false
DB_HOST must be nonempty
1

Case -2
PS C:\Users\pragnag\DevOpsClassRepo> py validator.py valid.env.example
>> $LASTEXITCODE
Configuration accepted
0

Case -3
PS C:\Users\pragnag\DevOpsClassRepo> py validator.py messy.env
>> $LASTEXITCODE
APP_PORT must be an integer
DEBUG must be false
DB_PASSWORD must be nonempty
1