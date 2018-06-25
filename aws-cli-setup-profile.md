# AWS & ASK CLI Setup Guide
[AWS Account](new-aws-account.md) | [AWS CLI](aws-cli-setup-intro.md) | **[AWS CLI Profile](aws-cli-setup-profile.md)** | [Amazon Developer Account](dev-portal-intro.md) | [ASK CLI](ask-cli-setup-intro.md) | [ASK CLI Profile](ask-cli-setup-profile.md) | [Deploy a Skill](deploy-sample-skill.md)


# AWS CLI Setup - Profiles

If you are here it means that you have:

✓ **An AWS Account** (if you don't, follow the [guide to Create a new AWS Account](new-aws-account.md))

✓ **The AWS CLI Installed** (if you don't, follow the [guide to install AWS CLI](aws-cli-setup-install.md))



In this step, we will create a **new AWS Identity and Access Management (IAM) User** in your AWS account and a **new AWS CLI Profile** mapped to this IAM user. 

![](iam_icon.png)

IAM enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. 

IAM users enable programmatic access to your AWS Account so that tools such as the AWS CLI can access your account on your behalf, without requiring a username and password. Programmatic access to your account is controlled through an Access Key and an Access Secret Key.



### Create a New IAM User

##### 1 - Log on to your AWS Account

Using your browser, navigate to: http://aws.amazon.com and log in to your account.  

**Note** If you have already created IAM users in the past, make sure to log into your account with an IAM user that has sufficient privileges to create IAM users. Otherwise, if you are following along or have just created your AWS Account, use the email address and root account password associated with your AWS account, which has Administrator privileges to the account. 



##### 2 - In your AWS Account, navigate to the IAM Console

After you log on to the account, on the front page, type `IAM` in the AWS services search box and select `IAM`   from the drop-down that appears.

![](aws-console-iam-searchbox.png)



##### 3 - Open the Users Panel and `Add user` to create a new IAM User

From the menu on the left-hand side, click `Users` and then, from the Users list view, click the `Add user` button at the top of the page to start the step-by-step wizard for creating a new IAM user.   

![](iam-new-user-step2.png)



##### 4 - Name the User and Give it Programmatic Access

The first step for creating a new user is to give the user a name and to decide what type of access the user will have. In our case, the user will need to have **programmatic access** so make sure to select that check box. This user will not need AWS Management Console access so leave that check box unselected. 

![](iam-new-user-step3.png)



##### 5 - Configure Security Policy for the New User

The next step in the processs is to determine the permissions associated with the IAM user. This controls what features of your AWS account the IAM user has access to. Select **Attach existing policies directly** and give the user **Administrator Access** 

![](iam-new-user-step4.png)



##### 6 - Review User Configuration and Create

The next step is just an overview of the new user you are about to create. Confirm that the user has **programmatic access** and that the correct Permissions were associated.

![](iam-new-user-step5.png)



##### 7 - Record the new User Access Key ID and Secret Access Key

**IMPORTANT**  This is the only opportunity you have to view the secret access key associated with the newly created IAM user.  Make note of both the Access Key ID and the Secret Access Key shown on this page. 

For now, do not close this browser page until you have configured an AWS CLI profile using the access keys shown here. Instead, continue with **Step 8** below.



![](iam-new-user-step6.png)

### Configure a New AWS CLI Profile

Now that you have created an IAM user, we will move over to the AWS CLI and create a new profile mapped to the new IAM user you've just created.

The AWS CLI supports *named profiles* stored in the config and credentials files. You can configure additional profiles by using `aws configure` with the `--profile`option or by adding entries to the config and credentials files. The CLI stores credentials in a local file named `credentials` in a folder named `.aws` in your home directory. Home directory location varies but can be referred to using the environment variables `%UserProfile%` in Windows and `$HOME` or `~` (tilde) in Unix-like systems. 

For example, the following commands list the contents of the `.aws` folder:

**Linux, macOS, or Unix**

```
$ ls  ~/.aws
```

**Windows**

```
> dir "%UserProfile%\.aws"
```

In order to separate credentials from less sensitive options, region and output format are stored in a separate file named `config` in the same folder.

If you have never configured the AWS CLI before, you may not have the `.aws` folder, or either of the `config` or `credentials` files. In that case you can go ahead and create the files now, otherwise, just open the existing files for editing

The contents of the `~/.aws/config` file should look like this (if the file does not exist, go ahead and create it now):

```
[default]
region=eu-west-1
output=json
```

 While the contents of the `~/.aws/credentials` file should look like this:

```
[profile1]
aws_access_key_id=AKIAIOSFDAS5N56EXAMPLE
aws_secret_access_key=wJanFEMIlrXUtMDENGbPxRfiCYEXAMPLEKEY

[profile2]
aws_access_key_id=AKIAIOSFODNN7EXAMPLE
aws_secret_access_key=wJalrXUtnFEMIK7MDENGbPxRfiCYEXAMPLEKEY
```



##### 1 - Create a New Profile

In this step we will create a new AWS configuration profile named `ask-user`

Open the `~/.aws/credentials` file and add the following section at the end of the file:

```
[ask-user]
region=eu-west-1
aws_access_key_id=AKIAIGRETCINNOOSXQNA
aws_secret_access_key=examplewJalrXUtnFEMIK7MDENGbPxRfiCYKEY
```

Make sure to paste the Access Key and the Secret Key that were generated for the new IAM User that you have just created in the steps above!

The `region` parameter should match the AWS region that you whish to use.  

Close and save the file



##### 2 - Verify that the new profile works

After creating the new profile you can verify that it was setup correctly by issuing a couple of aws commands on the terminal, including the `--profile` option, like this:

```
$ aws --profile ask-user iam list-users
```

If all worked fine, you should see output similar(*) to this:

```
{
    "Users": [
        {
            "UserName": "cli-user",
            "Path": "/",
            "CreateDate": "2018-06-15T10:51:30Z",
            "UserId": "AIDAJZDED5LZ3DF3RSF4M",
            "Arn": "arn:aws:iam::12345678901:user/cli-user"
        }
    ]
}
```

**Note**:  depending on how many users you have in your account this list may be longer. 



###   🏆 **Congratulations** - You Have Completed the AWS CLI Setup! 🏆

 

## Next step:  [Amazon Developer Portal Setup](dev-portal-intro.md)
