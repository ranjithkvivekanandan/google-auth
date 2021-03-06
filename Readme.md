# Google-auth


This command-line tool allows you to acquire AWS temporary (STS) credentials using Google Apps as a federated (Single Sign-On, or SSO) provider.


You'll first have to set up Google Apps as a SAML identity provider (IdP) for AWS. There are tasks to be performed on both the Google Apps and the Amazon sides.

# For basic installation

To get AWS STS token using gsuite credential we have execute the python script. to execute the python script we have ensure python and required library are installed in your local host. the below step will help us to install the application.



the below command are used in ubuntu OS:

localhost$ sudo apt install python

localhost$ sudo apt install python-pip

localhost$ sudo pip install -r requirement.txt

# Run the below command from your local machine to get temporary token from AWS

Once we installed the above application, clone the repositroy.

localhost$ get clone <repo url>
  
Go to cloned repository 

localhost$ cd /google-auth

Execute the __init__.py file as mentioned below.

localhost$ python __init__.py -u username 

it will prompt you to provide gsuite password.

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


Note: for detailed instruction refer the below link step 7:

https://life360.atlassian.net/wiki/spaces/INFENG/pages/653066245/Federated+Single+Sign-on+design+document+-+draft

