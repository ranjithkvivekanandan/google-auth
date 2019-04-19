# google-auth


This command-line tool allows you to acquire AWS temporary (STS) credentials using Google Apps as a federated (Single Sign-On, or SSO) provider.

Setup
You'll first have to set up Google Apps as a SAML identity provider (IdP) for AWS. There are tasks to be performed on both the Google Apps and the Amazon sides.

# For basic installation
You can install quite easily via python, pip, if you want to have it on your local system:


To get AWS STS token using gsuite credential we have execute the script. to execute the python script we have ensure python and required 
library. the below step will help you install the application.

the below command are used in ubuntu OS.

localhost$ sudo apt install python

localhost$ sudo pip install -r requirement.txt

# Run the below command from your local machine

Once you installed above application, clone the repositroy.

go to cloned repository 

localhost$ cd /google-auth

Execute the __init__.py file as mentioned below.

localhost$ python __init__.py -u username 

it will prompt you to provide email details and password.

usage: python __init__.py -u username  [-h] [-u USERNAME] [-I IDP_ID] [-S SP_ID] [-R REGION]


                       [-d DURATION] [-p PROFILE] [-D] [-q] [--no-cache]
                       
                       [--print-creds] [--resolve-aliases]
                       
                       [--save-failure-html] [-a | -r ROLE_ARN] [-k] [-V]


Acquire temporary AWS credentials via Google SSO

optional arguments:
  -h, --help            show this help message and exit
  
  -u USERNAME, --username USERNAME
                        Google Apps username ($GOOGLE_USERNAME)
  
  -I IDP_ID, --idp-id IDP_ID
                        Google SSO IDP identifier ($GOOGLE_IDP_ID)
  
  -S SP_ID, --sp-id SP_ID
                        Google SSO SP identifier ($GOOGLE_SP_ID)
  
  -R REGION, --region REGION
                        AWS region endpoint ($AWS_DEFAULT_REGION)
  
  -d DURATION, --duration DURATION
                        Credential duration ($DURATION)
  
  -p PROFILE, --profile PROFILE
                        AWS profile (defaults to value of $AWS_PROFILE, then
                        falls back to 'sts')
  
  -D, --disable-u2f     Disable U2F functionality.
  
  -q, --quiet           Quiet output
  
  --no-cache            Do not cache the SAML Assertion.
  
  --print-creds         Print Credentials.
  
  --resolve-aliases     Resolve AWS account aliases.
  
  --save-failure-html   Write HTML failure responses to file for
                        troubleshooting.
  
  -a, --ask-role        Set true to always pick the role
  
  -r ROLE_ARN, --role-arn ROLE_ARN
                        The ARN of the role to assume
  
  -k, --keyring         Use keyring for storing the password.
  
  -V, --version         show program's version number and exit



