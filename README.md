# lambdadaily
A lambda version of the daily increase script. Deployed to production.

This script runs on AWS Lambda. It downloads the latest Excel spreadsheet from the Scottish Governement's website and calculates the daily increase in NHS Lothian.

To deploy to AWS Lambda please cd into the directory and run "zip lambda_function.zip ./ -r". 
Once the zip file is created upload to AWS Lambda's console. Then set up a Cloudwatch Event Trigger to run as often as you wish (I run it each day at 14:10 UTC as the new data is uploaded at 14:00)

If there are issues with the code you will need to modify locally as the IDE on the Lambda console can't handle files as big as this zip. 

Enjoy!
