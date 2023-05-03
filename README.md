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

<details>
<summary><b> What is the cold start time in aws lambda? </b></summary><br>
So the cold start time is just nothing but it's a time that lambda spends initialization of the function, which includes loading the function code, starting the runtime and initializing the function code with the snap start lambda initializes your function when you publish function version. So cold start problem is just a delay that can occur when a lambda function is invoked for the first time after a period of inactivity, underlying infrastructure provision and initializes the resources needed to execute the function to address this problem. Lambda has few strategy first we have to reduce the function package says the larger function package take longer to load increasing the likelihood of cold start consider reducing the size of our function package by removing the unnecessary dependencies are using a smaller runtime environment. And we have to use a provision the concurrency. AWS offers a feature called provisioned concurrency that enables you to pre warm a number of instances of your function so that they are ready to handle incoming requests without experiencing cold starts. You can configure the number of provision to concurrency instances based on the expected traffic and we can also implement the connection pooling. If your lambda function connects to a database, or other external service, consider implementing connection pooling to reuse existing connection instead of creating the new one for each request. So this can help reduce the time needed to initialize the function.
you can increase the memory and timeout settings also. We can allocate more memory and increase the timeout settings

</details>





