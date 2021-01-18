# The Serverless Distributed Web Crawler

This is naive crawler that's a Proof of Concept and not appropriate for production usage. Do not use against production websites. Do not use against websites where you do not have permission to crawl. Do not violate AWS Terms & Conditions.

This code is provided for educational purposes only with no warranty implied. 

Misuse may result in considerable AWS expenses and may negatively impact target websites.

Do not run this code unless you understand the implications of web crawling. You are entirely responsible for the consequences of running this code.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Support](#support)

## Installation

Clone and ```npm install``` in your downloaded directory.

## What is the Tech Stack behind this?
* AWS Lambda for the processing of the HTML pages and data scraping
* DynamoDB for caching the urls to be captured, and to trigger lambda functions
* RDS MySQL as the end database for the processed and structured data to be stored

## Usage
Don't forget to:

- Update your testEvent.json
- Create the DynamoDB table 'crawler' - the table should have a partition key called 'url', no sort key and capacity set to on-demand.
- Add the stream ARN in serverless.yaml (when you are ready)
- Spend time to test and understand what the code is doing


