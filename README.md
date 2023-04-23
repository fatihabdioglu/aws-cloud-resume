# AWS Cloud Resume Challenge

Hi, This is my first Cloud Resume Challenge attempt. This challenge provided me with the opportunity to gain technical experience and improve my skills using AWS. Development is ongoing, I will share updates. The project was published by Forrest Brazeal.

[My website is here](https://resume.fatihabdioglu.link/)

[The challenge website is here](https://cloudresumechallenge.dev/)

## Architecture Diagram

![alt text](./architecture.png)

### Tech-stack ###

+ HTML/CSS
+ S3
+ AWS CloudFront
+ Certificate Manager
+ Route53
+ AWS Lambda
+ DynamoDB
+ GitHub Actions

### Details ###

+ First, a website template was created using html and css. Then a Java-written file was added for the visitor counter.
+ These files were uploaded to an s3 bucket. Then the origin domain of the CloudFront distribution is created by selecting the bucket where the website is. Viewer protocol policy is set to HTTPS for secure connection.
+ A record was created by choosing the distribution of cloudfront as alias from Route53.
+ The python code for the visitor counter has been added to aws Lambda and a table has been created to keep these results in DynamoDB.
+ Finally, a repo with website files was created on GitHub. Necessary secrets for Actions (Bucket Name, Access Key, Secret Access Key) were created. Thus, when any change on the website is pushed, the updates will be automatically reflected to the S3 bucket and from there to the domain.
+ The repo will be updated when these steps are done as iac, CI/CD for Back-end is added or any changes occur.
