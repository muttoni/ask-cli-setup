# AWS & ASK CLI Setup Guide
[AWS Account](new-aws-account.md) | **[AWS CLI](aws-cli-setup-intro.md)** | [AWS CLI Profile](aws-cli-setup-profile.md) | [Amazon Developer Account](dev-portal-intro.md) | [ASK CLI](ask-cli-setup-intro.md) | [ASK CLI Profile](ask-cli-setup-profile.md) | [Deploy a Skill](deploy-sample-skill.md)



## AWS CLI Setup - Installation - Windows

You can install the AWS CLI on Windows with a standalone installer or `pip`, a package manager for Python. If you already have Python and `pip`, follow the instructions for installing using pip as that makes upgrading to newer versions easier, otherwise the MSI Installer provides a streamlined experience.

**Note**: If you already have the CLI installed, continue to [Setup an AWS CLI Profile](aws-cli-setup-profile.md), or, if you don't have an AWS account, follow the [guide to create an AWS account](new-aws-account.md) first.



#### MSI Installer

The AWS CLI is supported on Microsoft Windows XP or later. For Windows users, the MSI installation package offers a familiar and convenient way to install the AWS CLI without installing any other prerequisites.

When updates are released, you must repeat the installation process to get the latest version of the AWS CLI.

**To install the AWS CLI using the MSI installer**

1. [Download the AWS CLI MSI installer for Windows](https://s3.amazonaws.com/aws-cli/AWSCLISetup.exe)

   **Note** *The MSI installer for the AWS CLI does not work with Windows Server 2008 (version 6.0.6002). Use [pip](https://docs.aws.amazon.com/cli/latest/userguide/awscli-install-windows.md#awscli-install-windows-pip) to install with this version of Windows.*

2. Run the downloaded MSI installer.

3. Follow the instructions that appear.

The CLI installs to `C:\Program Files\Amazon\AWSCLI` (64-bit) or `C:\Program Files (x86)\Amazon\AWSCLI` (32-bit) by default. To confirm the installation, use the `aws --version` command at a command prompt (open the START menu and search for "cmd" if you're not sure where the command prompt is installed).



**Troubleshooting**

If after installing the `aws` command doesn't work, you may need to update your OS's `PATH` environment variable. Follow the instructions [here](https://docs.aws.amazon.com/cli/latest/userguide/awscli-install-windows.md#awscli-install-windows-path).



## Next step: [Setup an AWS CLI Profile](aws-cli-setup-profile.md)

