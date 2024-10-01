--------

--------

# Configuring the AWS CLI<a name="cli-chap-configure"></a>

* goal
  * configure the settings / AWS CLI use
    * security credentials
    * default output format
    * default AWS Region

* AWS requires
  * 👁️ALL incoming requests are cryptographically signed 👁️
    * made automatically by AWS CLI
    * "signature" == date time stamp + ...
      * -> ⚠️ your computer's date and time must set correctly ⚠️	
        * else, AWS rejects the request 

**Topics**
+ [Configuration basics](cli-configure-quickstart.md)
+ [Configuration and credential file settings](cli-configure-files.md)
+ [Named profiles for the AWS CLI](cli-configure-profiles.md)
+ [Configuring the AWS CLI to use AWS IAM Identity Center \(successor to AWS Single Sign\-On\)](cli-configure-sso.md)
+ [Environment variables to configure the AWS CLI](cli-configure-envvars.md)
+ [Command line options](cli-configure-options.md)
+ [Command completion](cli-configure-completion.md)
+ [AWS CLI retries](cli-configure-retries.md)
+ [Sourcing credentials with an external process](cli-configure-sourcing-external.md)
+ [Using credentials for Amazon EC2 instance metadata](cli-configure-metadata.md)
+ [Using an HTTP proxy](cli-configure-proxy.md)
+ [Using an IAM role in the AWS CLI](cli-configure-role.md)