Day_56: Student Handout
# AWS CLI Student Handout

## Introduction to AWS CLI

### What is AWS CLI?
The AWS Command Line Interface (CLI) is a tool that allows you to manage AWS services from your terminal or command prompt. It is useful for automation, scripting, and efficient management of AWS resources.

---

## Benefits and Use Cases of AWS CLI

- **Automation**: Automate repetitive tasks with scripts.
- **Efficiency**: Perform tasks faster than using the AWS Management Console.
- **Scripting**: Ideal for creating scripts to manage resources and deploy applications.
- **Cross-Platform**: Works on Windows, macOS, and Linux.

---

## Overview of Supported Platforms

AWS CLI is supported on:
- **Windows**
- **macOS**
- **Linux**

Commands are consistent across all platforms.

---

## Installing AWS CLI on Windows

### Step 1: Downloading and Installing AWS CLI v2 for Windows

1. **Download the Installer**: Visit the [AWS CLI download page](https://aws.amazon.com/cli/) and download the `.msi` installer.
2. **Run the Installer**: Double-click the `.msi` file and follow the instructions.
3. **Verify Installation**: Open Command Prompt and type:
   ```bash
   aws --version
   ```

### Step 2: Configuring AWS CLI with AWS Credentials

1. **Obtain AWS Credentials**: Log in to AWS Management Console, navigate to IAM, and generate an Access Key and Secret Key.
2. **Configure AWS CLI**: In Command Prompt, type:
   ```bash
   aws configure
   ```
   Enter your Access Key, Secret Key, Region, and Output Format.
3. **Testing the Installation**: Run:
   ```bash
   aws s3 ls
   ```

---

## Installing AWS CLI on macOS and Linux

### Step 1: Installing AWS CLI on macOS Using Homebrew

1. **Install Homebrew**:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. **Install AWS CLI**:
   ```bash
   brew install awscli
   ```
3. **Verify Installation**:
   ```bash
   aws --version
   ```

### Step 2: Installing AWS CLI on Linux Using Package Managers

1. **For Ubuntu/Debian**:
   ```bash
   sudo apt update
   sudo apt install awscli
   ```
2. **For CentOS/RedHat**:
   ```bash
   sudo yum install awscli
   ```
3. **Verify Installation**:
   ```bash
   aws --version
   ```

### Configuring AWS CLI on macOS/Linux with IAM Credentials

1. **Run the Configuration Command**:
   ```bash
   aws configure
   ```
2. **Enter AWS Credentials**: Provide Access Key, Secret Key, Region, and Output Format.
3. **Testing the Installation**:
   ```bash
   aws s3 ls
   ```

---

## Managing Multiple AWS Profiles with the CLI

### Step 1: Setting Up Named Profiles

1. **Create a Profile**:
   ```bash
   aws configure --profile dev
   ```
2. **Switch Between Profiles**:
   ```bash
   aws s3 ls --profile dev
   ```

### Step 2: Listing All Profiles

Check the `~/.aws/credentials` file (macOS/Linux) or `C:\Users\<YourUsername>\.aws\credentials` (Windows).

---

## Hands-On: Installing, Configuring, and Testing AWS CLI on Your Platform

Follow the steps for your platform to install, configure, and test AWS CLI.

---

## Potential Gaps or Unclear Points

1. **Understanding AWS Credentials**: Access Key and Secret Key are like your username and password for AWS services.
2. **Region Confusion**: Regions represent AWS data centers in specific geographic locations.

---

## Diagrams to Help Understand

### Diagram 1: AWS CLI Workflow

```
+-------------------+       +-------------------+
|   Your Computer    |       |   AWS Services    |
| (AWS CLI Installed)|       | (S3, EC2, etc.)   |
+-------------------+       +-------------------+
         |                           |
         | AWS CLI Command            |
         |-------------------------->|
         |                           |
         | AWS Response               |
         |<--------------------------|
         |                           |
```

### Diagram 2: AWS CLI Configuration

```
+-------------------+
|   AWS CLI Config   |
+-------------------+
| Access Key        |
| Secret Key        |
| Region            |
| Output Format     |
+-------------------+
```

---

## Conclusion

You should now understand what AWS CLI is, how to install it on different platforms, and how to configure it with your AWS credentials. AWS CLI is a powerful tool for managing AWS services efficiently. Try it out on your platform and run some basic commands to get familiar with it.
