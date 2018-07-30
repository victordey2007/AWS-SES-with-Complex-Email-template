1. Install AWS CLI command 
2. Setup your credential ( access key ,region etc) 

3. Create one email template where HtmlPart is used for sending HTMl enabled email , if recepient end HTML does not support use TextPart .
 check the sample email template mytemplate.json

4. user the command to create the template. Please make  sure your user has proper policy attached in case your user does not have administratorAccess.

5. aws ses create-template --cli-input-json file://mytemplate.json

6.Create one input file ex myemail.json , incase if you call webservice your input will be almost same .

7.aws ses send-templated-email --cli-input-json file://myemail.json



The template feature in Amazon SES is based on the Handlebars template system which support for,if , array 

ref https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-personalized-email-advanced.html

