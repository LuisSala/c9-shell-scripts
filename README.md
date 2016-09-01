1. Create a Cloud9 account:
https://c9.io

2. Launch an empty Workspace

3. Clone Zombie Repo
git clone https://github.com/LuisSala/aws-lambda-zombie-workshop .

4. Clone the Tools Repo
git clone https://github.com/LuisSala/c9-shell-scripts ./tools


5. Install AWS CLI

` sudo pip install awscli

6. Configure CLI with **aws configure**
```
$ aws configure
AWS Access Key ID [None]: AKISAMPLEACCESSKEY
AWS Secret Access Key [None]: CHANGEME/t00m@any$3cret$E
Default region name [None]: us-east-1
Default output format [None]: json
```

7. Launch Stack from github repo

8. Begin to follow intros. At "Setup..." step 19:
`$ tools/pull-site

9. Make the necessary changes to constants.js
`$ tools/push-site

10. Generating keys
```bash
$ openssl genrsa -aes256 -out private_key.pem 2048
Generating RSA private key, 2048 bit long modulus
.........................................................................................................+++
........................+++
e is 65537 (0x10001)
Enter pass phrase for private_key.pem:
Verifying - Enter pass phrase for private_key.pem:

$ openssl rsa -in private_key.pem -out private_key_no_password.pem
Enter pass phrase for private_key.pem:
writing RSA key

$ openssl rsa -pubout -in private_key_no_password.pem -out public_key.pem
writing RSA key
```

Config:
Cognito Pool ID: CHANGEME
App Client ID: CHANGEME