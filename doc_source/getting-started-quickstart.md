--------

--------

# Quick setup<a name="getting-started-quickstart"></a>

* goal
  * configure basic settings of AWS CLI
    * security credentials
    * default
      * output format
      * AWS Region

**Topics**
* [New configuration quick setup](#getting-started-quickstart-new)
* [Using existing configuration and credentials files](#getting-started-quickstart-existing)

## New configuration quick setup<a name="getting-started-quickstart-new"></a>

* `aws configure`
  * AWS CLI prompts 
    * / you need to enter
      * [Access key ID](cli-configure-quickstart.md#cli-configure-quickstart-creds)
      * [Secret access key](cli-configure-quickstart.md#cli-configure-quickstart-creds)
      * [AWS Region](cli-configure-quickstart.md#cli-configure-quickstart-region)
      * [Output format](cli-configure-quickstart.md#cli-configure-quickstart-format)
    * are stored | *profile*
      * == collection of settings /
        * named `default`
        * | "credentials" file
          * [Configuration and credential file settings](cli-configure-files.md)
      * uses
        * when you run an AWS CLI command
          * if you do NOT specify the profile -> `default` is used 
  * _Example:_

    ```
    $ aws configure
    AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
    AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
    Default region name [None]: us-west-2
    Default output format [None]: json
    ```
  * [Configuration basics](cli-configure-quickstart.md)

## Using existing configuration and credentials files<a name="getting-started-quickstart-existing"></a>

* TODO:
If you have existing configuration and credentials files, these can be used for the AWS CLI\. 

To use the `config` and `credentials` files, move them to the folder named `.aws` in your home directory\. Where you find your home directory location varies based on the operating system, but is referred to using the environment variables `%UserProfile%` in Windows and `$HOME` or `~` \(tilde\) in Unix\-based systems\. 

You can specify a non\-default location for the `config` and `credentials` files by setting the `AWS_CONFIG_FILE` and `AWS_SHARED_CREDENTIALS_FILE` environment variables to another local path\. See [Environment variables to configure the AWS CLI](cli-configure-envvars.md) for details\. 

For more detailed information on configuration and credentials files, see [Configuration and credential file settings](cli-configure-files.md)\.