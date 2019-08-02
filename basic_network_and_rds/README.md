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

Change app name in `cloudformation_network.yml.example` file.

Do not include `-` in DB_NAME.

ex.)

```
$ sed -e "s/YOUR_APP_NAME/置換後文字列/g" cloudformation_network.yml.example > cloudformation_network.yml
```

Upload `cloudformation_network.yml` file to S3 and run CloudFormation.
