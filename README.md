1. Clone Zombie Repo

2. Clone Box Repo

TODO: Combine into a single project

3. Install AWS CLI

` sudo pip install awscli

4. Configure CLI with:
`aws configure
```
c9ideuser:~/workspace (master) $ aws configure
AWS Access Key ID [None]: AKISAMPLEACCESSKEY
AWS Secret Access Key [None]: jt00m@any$3cret$Ev
Default region name [None]: us-east-1
Default output format [None]: json
```
5. Launch Stack from github repo

6. Begin to follow intros. At "Setup..." step 19:
`$ ./pull-site
Make the necessary changes to constants.js
`$ ./push-site

7. Generating keys
```
c9ideuser:~/workspace (master) $ openssl genrsa -aes256 -out private_key.pem 2048
Generating RSA private key, 2048 bit long modulus
.........................................................................................................+++
........................+++
e is 65537 (0x10001)
Enter pass phrase for private_key.pem:
Verifying - Enter pass phrase for private_key.pem:

c9ideuser:~/workspace (master) $ openssl rsa -in private_key.pem -out private_key_no_password.pem
Enter pass phrase for private_key.pem:
writing RSA key

c9ideuser:~/workspace (master) $ openssl rsa -pubout -in private_key_no_password.pem -out public_key.pem
writing RSA key
c9ideuser:~/workspace (master) $ 
```

Config:
Cognito Pool ID: CHANGEME
App Client ID: CHANGEME