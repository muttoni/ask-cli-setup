# AWS & ASK CLI Setup Guide
[AWS Account](new-aws-account.md) | **[AWS CLI](aws-cli-setup-intro.html)** | [AWS CLI Profile](aws-cli-setup-profile.html) | [Amazon Developer Account](dev-portal-intro.html) | [ASK CLI](ask-cli-setup-intro.html) | [ASK CLI Profile](ask-cli-setup-profile.md) | [Deploy a Skill](deploy-sample-skill.html)



## AWS Command Line Interface (CLI)

The AWS Command Line Interface (CLI) is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.

When developing Alexa Skills, AWS Lambda is a great runtime choice for hosting and executing your skill code. The AWS CLI provides easy access to create and update Lambda functions.     

If you don't already have an AWS account, make sure to [create an account](new-aws-account.md) first.



#### Do you have the AWS CLI Installed?

To check whether you have the AWS CLI installed, open a terminal (command prompt on Windows) and type the following command:

```bash
aws --version
```

If the CLI is installed correctly then you should see an output like this:

```
aws-cli/1.11.84 Python/3.6.2 Linux/4.4.0-59-generic botocore/1.5.47
```

In this case, you can continue to the next step which is to [Setup an AWS CLI Profile](aws-cli-setup-profile.md).



If the CLI is not installed, then you will get an error back stating that `aws` is not a recognized command. In that case you should continue to follow the guide to [Install the AWS CLI](aws-cli-setup-install.md)



Next steps:

## [Setup an AWS CLI Profile](aws-cli-setup-profile.md) | [Install the AWS CLI](aws-cli-setup-install.html).
