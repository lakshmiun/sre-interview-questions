# DevOps/ SRE interview-questions
Hi, I'm Sahaja undavalli and in this repository there is a collection of DevOps/Site Reliability Engineer (SRE) interview questions and answers.

## Cloud
<details>
<summary><b> What are the limitations of aws lambda? </b></summary><br>
Limitations of AWS lambda is : it supports only one GB of memory and it supports only 15 minutes of run time when you want to run small kind of code. Based on the event you have to go for the AWS Lambda. the execution time and memory allocation is the unlimited access to resources is the limitations of AWS lambda
If your function requires more memory than this it will fail to execute and it will take longer than 15 minutes to complete. Maximum execution time is 15 minutes or less.
And also when a lambda function is invoked for the first time it can experience a <b>cold start latency</b> as the infrastructure is initialized.
Because the AWS lambda function have some limited access to resources outside of their own environment, such as databases for file system it can be more complex than traditional server based architecture.
<br>
</details>



