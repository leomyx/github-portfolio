# AWS Integrating AWS Lambda as an authoriser with OpenID as an Identity Provider to provide access to a RESTful API Gateway

## Architecture diagram

![AWS Integrating AWS Lambda as an authorizer with OpenID as an Identity Provider to provide access to a RESTful API Gateway](aws-lambda-authoriser-openid-rest-api-gateway.svg)

```diagram
                       +-----------------------+
                       |                       |
                       |  OpenID Connect       |
                       |   Identity Provider   |
                       |                       |
                       +-----------^-----------+
                                   |
                                   |
                                   |
                       +-----------+-----------+
                       |                       |
                       |    API Gateway        |
                       |                       |
                       +-----------^-----------+
                                   |
                                   |
                                   |
                       +-----------+-----------+
                       |                       |
                       |    AWS Lambda         |
                       |    Authorizer         |
                       |                       |
                       +-----------^-----------+
                                   |
                                   |
                       +-----------+-----------+
                       |                       |
                       | RESTful API Resouces  |
                       |                       |
                       +-----------------------+

```

### Sequence Flows

1. OpenID Connect Identity Provider - Google Account / Workspace
2. AWS Lambda Authorizer validate tokens and create policy/scopes attached to the token
3. API Gateway Rest API based on open api swagger.yaml

### Additional details

TBD
