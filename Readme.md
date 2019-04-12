google-auth


This command-line tool allows you to acquire AWS temporary (STS) credentials using Google Apps as a federated (Single Sign-On, or SSO) provider.

Setup
You'll first have to set up Google Apps as a SAML identity provider (IdP) for AWS. There are tasks to be performed on both the Google Apps and the Amazon sides.

Installation
You can install quite easily via pip, if you want to have it on your local system:

# For basic installation
localhost$ sudo pip install -r requirement.txt

# Run the below command from your local machine

python __init__.py -u username [-I IDP_ID] [-S SP_ID] [-R REGION]

it will prompt you to provide email details and password.

