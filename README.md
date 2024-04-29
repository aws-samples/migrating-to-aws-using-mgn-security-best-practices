## Migrating to AWS Using Application Migration Service(MGN) Security Best Practices

This cloudformation template is intended to be used as an MGN After-Action, to enable SSM Session Manager for access to your newly migrated EC2.  

Launch this template in your account via the cloudformation console, and provide a name for the Systems Manager Automation Role it will create.

Upon launch, this template will create an SSM Automation Runbook that you can add to your MGN after-action template.

Note: to run this against an EC2 outside of the MGN console, you must do the following:
- Install the SSM Agent on the EC2 instance
- Create an EC2 Instance Profile IAM role that has [Session Manager required permissions](https://docs.aws.amazon.com/systems-manager/latest/userguide/getting-started-create-iam-instance-profile.html)
- Attach the EC Instance Profile role to your EC2 instance
- run the cloudformation template in this repo
- go to systems manager console, find the newly created Automation Runbook, and run it against the EC2 of your choice.


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

