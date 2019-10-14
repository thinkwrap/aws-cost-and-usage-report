# Generating spending report for AWS account as Google sheet

This is quick guide how to create spending report for AWS account that can be loaded to / manipulated by Google sheet.

I was adapted the Python script from <https://github.com/aws-samples/aws-cost-explorer-report>.

The forked and modified version is available at <https://github.com/thinkwrap/aws-cost-and-usage-report> (public repo).

## Changes against original

* removed the hardcoded us-east-1
* changed grouping from ACCOUNT =\> SERVICE to SERVICE =\> REGION

## Pre-requisites

* Python 3.7 (or pyenv and some 3.x)
* Pipenv
* aws credentials for the account or access to SSO - [https://pivotree.awsapps.com/start\#/](https://pivotree.awsapps.com/start#/)

## Installation

* clone the repo 

  `git clone git``@github``.com:thinkwrap/aws-cost-and-usage-report.git`

  `cd cd aws-cost-and-usage-report`
* Install dependencies (boto3)

  `pipenv install`

  `pipenv shell`
* Run the report, save result in file

  `python aws-cost-and-usage-report.py --days ``365` `>2019b.tsv`
* Open Google Docs, File → Import, select generated file, import