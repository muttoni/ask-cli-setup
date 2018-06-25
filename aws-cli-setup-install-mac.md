# AWS & ASK CLI Setup Guide
[AWS Account](new-aws-account.md) | **[AWS CLI](aws-cli-setup-intro.html)** | [AWS CLI Profile](aws-cli-setup-profile.html) | [Amazon Developer Account](dev-portal-intro.html) | [ASK CLI](ask-cli-setup-intro.html) | [ASK CLI Profile](ask-cli-setup-profile.md) | [Deploy a Skill](deploy-sample-skill.html)




## AWS CLI Setup - Installation - macOS

You can install the AWS CLI on macOS using `pip`, a package manager for Python.

**Note**: If you already have the CLI installed, continue to [Setup an AWS CLI Profile](aws-cli-setup-profile.md), or, if you don't have an AWS account, follow the [guide to create an AWS account](new-aws-account.html) first.



#### Prerequisites

In order to install the AWS CLI on your Mac you should make sure to have:

* Python (v2.6+ or v3+)
* pip 

Check whether you have Python by running this command on the Terminal:

```bash
$ python --version
```

**Note** on some systems, Python may be installed as **python3** so if you don't get any results using the command above, you should also try running the command using `python3` instead of `python`



Check whether you have `pip` installed by running the following command on the Terminal:

```bash
$ pip --version
```

**Note** on some systems, pip may be installed as **pip3** so if you don't get any results using the command above, you should also try running the command using `pip3` instead of `pip`



If you don't already have Python and pip installed, the easiest way to get both is to use `Homebrew` - a package manager for Mac.

To install Homebrew, open `Terminal` or your favorite OSX terminal emulator and run

```bash
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

The script will explain what changes it will make and prompt you before the installation begins. Once you’ve installed Homebrew, insert the Homebrew directory at the top of your `PATH` environment variable. You can do this by adding the following line at the bottom of your `~/.profile` file

```bash
export PATH=/usr/local/bin:/usr/local/sbin:$PATH
```

Now, we can install Python 3:

```bash
$ brew install python
```

This will take a minute or two. 

**Note** Homebrew installs `pip` pointing to the Homebrew’d Python 3 for you.



#### Install the AWS CLI on macOS using pip

Use `pip` to install the AWS CLI:

```bash
$ pip install awscli --upgrade --user
```



Verify that the AWS CLI is installed correctly:

```bash
$ aws --version
AWS CLI 1.11.84 (Python 3.6.1)
```





**Troubleshooting**

If after installing the `aws` command doesn't work, you may need to update your OS's `PATH` environment variable. Follow the instructions [here](https://docs.aws.amazon.com/cli/latest/userguide/cli-install-macos.md#awscli-install-osx-path).



## Next step: [Setup an AWS CLI Profile](aws-cli-setup-profile.md)

