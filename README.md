# Sample Python App

This is a simple Python Flask app that can be deployed via Jenkins running in an EC2 instance in a VPC.  Basically just add this code to a GitHub repo that you will use for testing Jenkins webhooks.  Please see steps in the README of aws-jenkins-in-vpc for how to set up the entire environment.

Once deployed, any update should send a webhook and trigger a pipeline run.  It may be possible for multiple to get triggered.  

Perhaps this time...  I just keep buildin
