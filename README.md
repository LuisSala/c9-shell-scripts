1. Create anm AWS account if you don't already have one. Make sure you copy your AWS ACCESS KEY and SECRET ACCESS KEY. You'll need this later.

2. Create a Cloud9 account:
https://c9.io

3. Visit the "awshackers" team workspace: https://c9.io/awshackers

4. Clone the "awshackers/hackathon" workspace. Ensure you uniquely name the workspace.

5. Open your newly-cloned workspace.

6. Configure CLI with **aws configure**
```
$ aws configure
AWS Access Key ID [None]: AKISAMPLEACCESSKEY
AWS Secret Access Key [None]: CHANGEME/t00m@any$3cret$E
Default region name [None]: us-east-1
Default output format [None]: json
```

7. ![Click Here](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=zombiestack&templateURL=https://s3.amazonaws.com/aws-zombie-workshop-us-east-1/CreateZombieWorkshop.json) to launch your stack:
 

8. Begin to follow intros. At "Setup..." step 19:
```
$ pull-constants
```

9. Make the necessary changes to constants.js
```
$ push-site
```

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