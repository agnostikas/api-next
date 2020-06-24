<p align="center">
  <a href="https://talaikis.com/">
    <img alt="Talaikis Ltd." src="https://github.com/TalaikisInc/talaikis.com_react/blob/master/media/logo.png" width="228">
  </a>
</p>

# Users Cubed 5.0

This is the 5th generation user management/ CMS system for rapid project development. It will be useful for any project, which needs user management system with a scalable architecture. It is a complete rewrite from scratch.

## What's new

* Every feature is now on separate Lambda and using DynamoDB as a database, because dealing with JSON on S3 was more cumbersome with complex data structures.
* Codebase is greatly reduced.
* Paswordless sign in, sign up, this allowed to remove password reset endpoint.
* Account confirmation step is now just sign up.
* All emails are now on templates and managed via AWS SES
* Separate Lambdas now allow much easier expansion of required features independently of each other
* Licence changed to MIT, but repo won't be public
* Some features were removed, but they were never fully finished on the first place, so this project is now just about user management, nothing more
* Protocol buffers were removed, because they didn't provide much of an advantage over JSON for REST-style API without Lambda support.
* Currently on over 30 Lambdas and growing

## Features

* User sign in/ sign out/ sign up/ confirm account, delete account
* Passwordless sign up/ sign in
* Dependency minimization
* Token auto expiration
* Email checking before sign up/ sign in with teh DNS records
* Push, SMS, Email notifications
* Admin system
* Automatic database backups
* Contact us service
* Upload service
* A/B testing service
* Billing service
* Newsletter service
* Referral service
* Encrypted database entries (AWS KMS + AWS Secrets Manager), upon request
* Encrypted JWT secret and admin passwords (AWS Secrets Manager), upon request

## Infrastructure

* [AWS Lambda](https://aws.amazon.com/lambda/)
* [AWS DynamoDB](https://aws.amazon.com/dynamodb/)
* [AWS S3](https://aws.amazon.com/s3/)
* [AWS SES](https://aws.amazon.com/ses/)
* [AWS SNS](https://aws.amazon.com/sns/)
* [AWS API Gateway](https://aws.amazon.com/api-gateway/)

## API Clients

All requests should have the following auth headers:

* x-api-key

## Install

```bash
npm install -g serverless
npm i
```

## Deploy

```bash
# Edit .env.production and config.js

# Then, long running deployment process:
npm run deploy
```

## Previous versions

* [React starter API](https://github.com/TalaikisInc/react_starter_api)
* [Users Cubed](https://github.com/TalaikisInc/users-cubed)
* [Users Cubed S3](https://github.com/TalaikisInc/users-cubed-s3)
* [Users Cubed API Next](https://github.com/TalaikisInc/users-cubed-api-next)

## Frontend Next 5.0

* [Frontend Next](https://github.com/TalaikisInc/frontend-next) - SSR frontend for this API

### How to easily spawn multiple projects

1. Clone repo
2. Change service name inside `.env.production`
3. Add your own functions if needed
4. Deploy: `npm run deploy`

## How to get it

Please contact me via [form here](https://talaikis.com)

## Licence

MIT
