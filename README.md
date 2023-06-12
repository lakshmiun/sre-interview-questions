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
<br>
</details>

<details>
<summary><b> Explain layers in lambda</b></summary>
In the lambda you have to create a layer we have to just refer the compatible runtime this will help you to add easily to your layer to your function
<br>
</details>

<details>
<summary><b>How do you access our web server application in the public?</b></summary>
If you want to access our web server application in the public, you have to keep it in the public subnet. And you can keep your database servers in the private subnet. And we can just enable the NAT so that you can access outgoing traffic and you can do some batch update. And you can create the load balancer which will automatically redirect the load and load balance across the web servers or we can just create the auto scaling feature which will automatically scale up and scale down the instances based on the usage. If you want to register your DNS in the cloud, you can use the route 53 And also it is act as a regional level failover, if any region goes down, it will switch and it will access from another region.
<br>
</details>

<details>
<summary><b>How do you update the patches in the server?</b></summary>
If you want to update the patches you have to attach the NAT gateway in the private subnet. So that you can able to install the patches in newer servers which is resides in the private subnet.
<br>
</details>

## Kubernetes and Docker
<details><summary><b>Explain the states of docker container?</b></summary>
Docker container will be in running state and paused state, created state and it will be in the restarting state and it will be in the exited state. And It will be in the dead state. 
Created means it has been created but has not been started 
running means it's currently running and executing its main process. 
paused means it's processed or temporarily stopped 
restarting means either it automatically or manually it will be restarted. 
exited means it has stopped and running it main process has exited. And containers stopped running due to an error or some other issues if it is a dead state.
<br>
</details>

<details><summary><b>Explain restart policies in docker container</b></summary>
so basically Docker have some different restart policy which is no the container will not restart it automatically even if it stopped for any reason on failure unless stopped always so on failure the container will be restarted only if stopped with nonzero exit code. And unless stopped the container will always be restarted unless it is stopped manually always means the container will restart regardless of exit code or the reason for stopping
<br></details>

<details><summary><b>Explain Kubernetes worker nodes and master nodes.</b></summary><br></details>

<details><summary><b>How do you upgrade Kubernetes clusters?</b></summary><br></details>

<details><summary><b>Explain Kube proxy and kubelet</b></summary><br></details>

<details><summary><b>What is init container?</b></summary><br></details>

## CI/CD

<details><summary><b>Explain your branching strategy </b></summary><br></details>

<details><summary><b>What is continuous integration, continuous delivery and continuous deployment? </b></summary><br></details>

<details><summary><b>Explain your CI/CD pipeline and  how do you integrate git with Jenkins</b></summary><br></details>

<details><summary><b>What is a Jenkins Shared Library and how it is useful? </b></summary><br></details>

<details><summary><b>What happens when a Jenkins agent is offline and what is the best practice in that situation? </b></summary><br></details>

<details><summary><b>How do you checkout code from repository using Jenkins? </b></summary><br></details>

<details><summary><b>What is the process for creating a Jenkins backup? </b></summary><br></details>

<details><summary><b> Explain difference betweeb Declarative and scripted pipelines</b></summary><br></details>

## Terraform

<details><summary><b>How do you use terraform for resource creation? </b></summary><br></details>

<details><summary><b>Explain terraform state file </b></summary><br></details>

<details><summary><b>What happens if you have lost terraform state file? </b></summary><br></details>

## SRE
<details><summary><b> Name some of the deployment strategies</b></summary><br></details>

<details><summary><b>What are SLO,SLA and SLI and error rates? </b></summary><br></details>

<details><summary><b>Name some SRE Pillars </b></summary><br></details>

<details><summary><b>Difference between monitoring and Observability </b></summary><br></details>

## Linux


## Programming

### BASH
<details><summary><b>How to check if the last command has ran successfully?</summary><br><b>
Explanation:

  `echo $?` if returns 0 that last command executed successfully

</b></details>

### Python
<details><summary><b>Name some python libraries you have used </b></summary><br></details>

<details><summary><b>Explain some of the automation scripts you have written using python?</b></summary><br></details>








