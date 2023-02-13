# AWS Infrastructure
This documentation provides an overview of the infrastructure setup for our application, built using Amazon Web Services (AWS) services.

## Simple Storage Service(S3)
For hosting the frontend of our application, we use the Amazon Simple Storage Service (S3). The frontend assets are bundled and uploaded to an S3 bucket which is then made publicly readable.

[Udagram S3](http://udagram03211230.s3-website-us-east-1.amazonaws.com/)

## Relational Database Service(RDS)
We use AWS RDS Postgres as our database solution for storing and retrieving information.

-RDS Endpoint:
```bash
database-1.ckh6tos1nndf.us-east-1.rds.amazonaws.com
```

## Elastic Beanstalk(EB)
The backend server is deployed on AWS Elastic Beanstalk service.

[AWS EB](http://udagram-api-dev.eba-hg2pdx9c.us-east-1.elasticbeanstalk.com)
