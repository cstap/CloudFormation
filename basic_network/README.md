# Basic network and RDS with CloudFormation

Setup basic network and RDS with CloudFormation.

## Design

```
1 VPC Network
1 RouteTable
1 InternetGateway

1 Public Subnet for web server
1 SecurityGroup for web server

2 Private Subnet for RDS
1 SecurityGroup for RDS
1 RDS Instance (MySQL)
```

## Setup

Change app name in `network.template.json` file.

ex.)

```
$ sed -e "s/YOUR_APP_NAME/置換後文字列/g" network.template.json > network.template
```

Upload `network.template` file to S3 and run CloudFormation.
