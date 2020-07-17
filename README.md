# Mlops-Task02

Complete Automation ( Integration of Jenkins, Docker & Git)

» Following is the detailed description of the task :-
Create container image that has jenkins installed using Dcokerfile.
When we launch this image , it should automatically starts jenkins service in the container.
Create a job chain of job1 , job2 , job3 , and job4 using build pipeline plugin in jenkins.

job1: Pull the Github repository automatically when some developers push repo to Github.
job2: By looking at the code or program file , jenkins should automatically start the respective language interpreter install image container to deploy code (e.g. If code is of PHP , then jenkins should start the container that has PHP already installed) .
Job3: Test your app if it is working or not .
job4: If app is not working , then send email to developer with error messages.
Create one extra job Job5 for monitor::If container where app is running, fails due to any reason then this job should automatically start the container again.

» Required Tool :
•Install docker in Redhat(linux).
• Install jenkins in Redhat(linux) .
• Install Git in Redhat(linux) .
• Install Python in Redhat(linux) .
» Dockerfile :
Create container image that's has jenkins installed using Dockerfile.
Docker imageTo build Dockerfile-
docker build -t img-name:version <path of image>
when Dockerfile is successfully build , it will create a container image -
docker image createdNow we have to run this image , command is following for the same -
docker run -it - privileged -p 1325:8080 -v /:/host - name jenkinsos jenkins:v1
jenkins running successfullyNow jenkins will unlocked by using above generated password.
So ,whole requirements is now done , now we will create our jobs -
» JOB1 :-
pull the Github repo automatically when developers push repo to the Github.
Console Output» JOB2 :-
By looking at the code , jenkins should automatically start the respective language interpreter install image container to deploy the code.
Job2 will triggered by Job1 and here I have used the post build action , if the container is failed to run then , it will trigger to the task2.4 , and here I have have used html , PHP can also be used.
console output» JOB3 :-
This job will show that whether it is working or not , either it is working fine or notifies the developer.
» JOB 4:
create one extra job not belong to the pipeline to monitor. If the container where the webpage is running fails due to any reason then this job will automatically start the container again.
job failed because OS is running alreadyHere , job chain of job1 , job2 , job3 and job4 using build pipieline plugin in jenkins.
Buid pipelineSo , here my task2 is done.
