# AWS & ASK CLI Setup Guide
[AWS Account](new-aws-account.md) | [AWS CLI](aws-cli-setup-intro.md) | [AWS CLI Profile](aws-cli-setup-profile.md) | [Amazon Developer Account](dev-portal-intro.md) | **[ASK CLI](ask-cli-setup-intro.md)** | [ASK CLI Profile](ask-cli-setup-profile.md) | [Deploy a Skill](deploy-sample-skill.md)




## ASK Command Line Interface (CLI)

The Alexa Skills Kit Command Line Interface (ASK CLI) is a tool that lets developers manage their Alexa skills and related resources such as interaction models and account linking details from the command line. It performs skill management actions by calling the Alexa Skill Management API (SMAPI) under the hood. ASK CLI can be used to create, read, update, and test Alexa skills and connected AWS Lambda functions, as well as to submit skills for certification or withdraw them.



The ASK CLI requires an Amazon Developer Portal account. Make sure to [create an account](new-dev-portal-account.md) first.



#### Do you have the ASK CLI Installed?

To check whether you have the ASK CLI installed, open a terminal (command prompt on Windows) and type the following command:

```bash
ask --version
```

If the CLI is installed correctly then you should see an output like this:

```bash
ask --version
1.1.2
```

In this case, you can continue to the next step which is to [Setup an ASK CLI Profile](ask-cli-setup-profile.md).



If the CLI is not installed, then you will get an error back stating that `ask` is not a recognized command. In that case you should continue to follow the guide to [Install the ASK CLI](ask-cli-setup-install.md)



## Next steps: [Install the ASK CLI](ask-cli-setup-install.md) | [Setup an ASK CLI Profile](ask-cli-setup-profile.md)
