#
Continous Integration
Continuous Integration (CI) is a development practice where developers integrate code into a shared repository frequently, preferably several times a day. Each integration can then be verified by an automated build and automated tests.
#
Continous Delivery
Continuous deployment is a strategy for software releases wherein any code commit that passes the automated testing phase is automatically released into the production environment, making changes that are visible to the software's users.
#
Why do we need these stuff?
Focus on building the product instead of deployment.
Quickly deliver fixes for bugs or breaking problems.
Maintain software reliability through tests.
Ability to easily rollback changes in the case of emergency.
Gives more confidence to the team.
CI/CD Gibberish based on Gitlab
Commit/Trigger: A code change.
Job: Instructions that a runner has to execute.
Pipeline: A collection of jobs split into different stages.
Runner: An agent or server that executes each job individually that can spin up or down as needed.
Stages: A keyword that defines certain stages of a job, such as build and deploy. Jobs of the same stage are executed in parallel.
alt text
#
Setting up CI/CD for ReactJS using GITLAB
Create a gitlab account
Create an AWS Account
Add the .gitlab-ci.yml on your project root.
Go gitlab project > CI/CD > Environment Variables
Create an S3 Bucket
Disable public access
Create a cloudfront distribution
Choose Web
Choose the S3 bucket as the Origin domain
Origin path should be /latest
Restrict Bucket Access select Yes
Select Create a New Identity
Yes, Update Bucket Policy
Default Root Object /index.html
Redirect HTTP to HTTPS
Lastly you can route the your domain to cloudfront using Route53.