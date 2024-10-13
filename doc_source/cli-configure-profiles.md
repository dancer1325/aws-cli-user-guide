--------

--------

# Named profiles for the AWS CLI<a name="cli-configure-profiles"></a>

* == collection of settings (".config") & credentials (".credentials") /
  * MULTIPLE can be stored
  * uses
    * apply | AWS CLI command
      * == 👁️a profile can be specified | running a command -- via -- `--profile profileName` 👁️
  * `default` profile
    * can be specified
    * 👁️if you do NOT specify parameter | AWS CLI -> `default` is used 👁️
* `AWS_PROFILE` environment variable
  * overrides the default profile / used

**Topics**
+ [Creating named profiles](#cli-configure-profiles-create)
+ [Using named profiles](#using-profiles)

## Creating named profiles<a name="cli-configure-profiles-create"></a>

* ways to configure additional profiles
  * [`aws configure --profile`](cli-configure-files.md#cli-configure-files-methods)
  * manually adding entries | `.config` and `.credentials`
    * [Configuration and credential file settings](cli-configure-files.md)

**Credentials profile**

* profileName | `credentials` vs profileName | AWS CLI `config`
  * 👁️NOT use the word `profile` prefix | `credentials` 👁️
* location
  * **`~/.aws/credentials`** | Linux & Mac
  * **`%USERPROFILE%\.aws\credentials`** | Windows

* _Example:_ `credentials` / 2 profiles

    ```
    [default]
    aws_access_key_id=AKIAIOSFODNN7EXAMPLE
    aws_secret_access_key=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
    
    [user1]
    aws_access_key_id=AKIAI44QH8DHBEXAMPLE
    aws_secret_access_key=je7MtGbClwBF/2Zp9Utk/h3yCo8nvbEXAMPLEKEY
    ```

**Config profile**

* uses
  * specify different 
    * credentials
    * AWS Regions
    * output formats
* 👁️profileName | `config`, MUST use `profile` as prefix 👁️
* location
  * **`~/.aws/config`** | Linux & Mac
  * **`%USERPROFILE%\.aws\config`** | Windows
* _Example:_ `config` / 2 profiles

    ```
    [default]
    region=us-west-2
    output=json
    
    [profile user1]
    region=us-east-1
    output=text
    ```

## Using named profiles<a name="using-profiles"></a>

* `--profile profileName` | your command
  * _Example:_ lists ALL your Amazon EC2 instances / defined | `user1` profile

    ```
    $ aws ec2 describe-instances --profile user1
    ```

* `AWS_PROFILE` environment variable 
  * allows
    * using a named profile | MULTIPLE commands
    * avoid specifying the profile / EVERY command
  * this environment variable priority < `--profile` priority
  * _Example:_
    * | **Linux or macOS**

    ```
    $ export AWS_PROFILE=user1
    ```

    * | **Windows**

      ```
      C:\> setx AWS_PROFILE user1
      ```
    
      * [set](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/set_1)
        * set an environment variable UNTIL
          * end of the current command prompt session
          * set the variable to a different value
      * [setx](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/setx)
        * set an environment variable / affects to ALL command shells created AFTER running the command
          * NOT affect command shells / ALREADY running
  * if you want to make environment variables / persistent ACROSS FUTURE sessions -> set [shell's startup script](cli-configure-envvars.md)
