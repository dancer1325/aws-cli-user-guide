--------

--------

# What is the AWS Command Line Interface?<a name="cli-chap-welcome"></a>

* open source tool /
  * allows
    * interacting with AWS services -- via -- commands | command-line shell
      * **Linux shells**
        * available |
          * Linux
          * MacOs
        * _Example:_ [https://www.gnu.org/software/bash/](https://www.gnu.org/software/bash/), [http://www.zsh.org/](http://www.zsh.org/), and [https://www.tcsh.org/](https://www.tcsh.org/)
      * **Windows command line**
        * available |
          * Windows
        * _Example:_ Windows command prompt, PowerShell
      * **Remotely**
        * available |
          * EC2 instances
        * _Example:_ remote terminal program (PuTTY, SSH) or with AWS Systems Manager
    * developing shell scripts -- to manage -- your resources 
  * 👁️-- direct access to -- AWS API 👁️
    * AWS API command -- has an equivalent -- AWS CLI command
    * some AWS services -- provide customizations for the -- AWS CLI 
* alternatives
  * AWS Management Console
    * browser\-based 
  * AWS API
* 👁️ALL IaaS \(infrastructure as a service\) AWS necessity (management, function, ..) is available | 👁️
  * AWS API
  * AWS CLI
  * AWS Management Console


## About AWS CLI version 2<a name="welcome-versions-v2"></a>

* AWS CLI version 2
  * MOST recent major version of the AWS CLI
  * supports ALL of the LATEST features
  * vs AWS CLI v1
    * features / introduced | v2 -- NOT supported | v1
      * if you want to use those features -> you MUST upgrade to v2
    * "breaking" changes from v1
      * [Migrating from AWS CLI version 1 to version 2](cliv2-migration.md)
  * way to install it
    * 👁️ONLY as a bundled installer 👁️
      * if you find it | package managers -> unsupported and unofficial packages
      * [Installing or updating the latest version of the AWS CLI](getting-started-install.md)
  * `aws --version`
  * [AWS CLI version 2 Changelog](https://github.com/aws/aws-cli/blob/v2/CHANGELOG.rst?plain=1)

## Maintenance and support for SDK major versions<a name="sdks-major-versions-maintenance-support"></a>

* [AWS SDKs and Tools Reference Guide](https://docs.aws.amazon.com/sdkref/latest/guide/overview.html)
  * [AWS SDKs and tools maintenance policy](https://docs.aws.amazon.com/sdkref/latest/guide/maint-policy.html)
  * [AWS SDKs and tools version support matrix](https://docs.aws.amazon.com/sdkref/latest/guide/version-support-matrix.html)

## About Amazon Web Services<a name="about-aws"></a>

* AWS
  * == collection of digital infrastructure services (computing, storage, database, application synchronization as messaging and queuing, ...)
  * pricing
    * pay as-you-go service model
      * == charged ONLY for the services / you—or your applications—use
    * [AWS Free Tier](http://aws.amazon.com/free/)
  * if you want to get an AWS account -> **Create an AWS Account** | open the [AWS home page](http://aws.amazon.com/) 