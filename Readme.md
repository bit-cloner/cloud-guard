### What is it ? 
The ambition of this product is to be a cloud scanning and reporting tool. Right now this works with AWS cloud. Future goal is to extedn this for other cloud providers.
Current features are 
- Scan AMIs that are public and owned by the account
- Scan for any newly created ECR repositories in the last 24 hours
- Scan for any orphaned load balancers without registered targets
- Scan for any newly created public load balancers
- Scan for any newly created public IP addresses

### Reporting
At present any findings are sent to a configured slack channel as an incoming webhook.

### Configuration
Configuration is done via environment variables
- SLACKHOOK holds the incoming webhook url 
- CHANNEL holds the channel to which messages are sent to

> Example:

`export SLACKHOOK="https://hooks.slack.com/services/EFD324FDF/SAGFG46898JKG/DSFGHGH6768MNBNDR"`

`export CHANNEL="#your-channel"`

This tool looks for typical authentication machanisms that AWS allows. i.e environment variables, AWS profile etc..
### Supported Platforms
Right now this tool is developed to work on Linux based systems. Future goal is to extend it to work on Windows, Mac and various CPU architectures.