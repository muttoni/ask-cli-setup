# AWS & ASK CLI Setup Guide
[AWS Account](new-aws-account.md) | **[AWS CLI](aws-cli-setup-intro.html)** | [AWS CLI Profile](aws-cli-setup-profile.html) | [Amazon Developer Account](dev-portal-intro.html) | [ASK CLI](ask-cli-setup-intro.html) | [ASK CLI Profile](ask-cli-setup-profile.md) | [Deploy a Skill](deploy-sample-skill.html)



## AWS CLI Setup - Installation - Linux



You can install the AWS CLI on Linux using `pip`, a package manager for Python.

**Important**

The `awscli` package is available in repositories for other package managers such as APT and yum, but it is not guaranteed to be the latest version unless you get it from `pip`



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



1. If Python 2.7 or later is not installed, install Python with your distribution's package manager. The command and package name varies:

   - On Debian derivatives such as Ubuntu, use `APT`:

     ```bash
     $ sudo apt-get install python3
     ```

   - On Red Hat and derivatives, use `yum`:

     ```bash
     $ sudo yum install python
     ```

   - On SUSE and derivatives, use `zypper`:

     ```bash
     $ sudo zypper install python3
     ```

2. If you don't have `pip`, install `pip` with the script provided by the Python Packaging Authority.

   - Download the installation script from [pypa.io](https://www.pypa.io/):

     ```bash
     $ curl -O https://bootstrap.pypa.io/get-pip.py
     ```

     

   - Run the script with Python:

     ```bash
     $ python get-pip.py --user
     ```

   - Make sure to add `pip` to your environment's `PATH` variable

     

 

#### Install the AWS CLI on macOS using pip

Use `pip` to install the AWS CLI:

```bash
$ pip install awscli --upgrade --user
```



Verify that the AWS CLI is installed correctly:

```bash
$ aws --version
aws-cli/1.11.84 Python/3.6.2 Linux/4.4.0-59-generic botocore/1.5.47
```





**Troubleshooting**

If after installing the `aws` command doesn't work, you may need to update your OS's `PATH` environment variable. Follow the instructions [here](https://docs.aws.amazon.com/cli/latest/userguide/awscli-install-linux.md#awscli-install-linux-path).

You may also need to ensure that the `aws` script has a file mode that is executable. Follow instructions [here](https://docs.aws.amazon.com/cli/latest/userguide/troubleshooting.md).



## Next step: [Setup an AWS CLI Profile](aws-cli-setup-profile.md)

