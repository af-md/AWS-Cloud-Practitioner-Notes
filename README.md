# AWS Cloud practiotioner  

## Around the world with AWS 

## Heading 3

## S3 101

*

*Paste the image here

###Charge 
*storage
*requests 
*storage management

###Transers Accelration:
*Fast transfer for file
**Using cloud front and edge locations(this will cache)
**avaliablity zones
**superfast network
*cross reion replication 
**allows to have to buckets in different regions for disaster recovery 
**exam tips
*** S3 is a universal namespace
*** links understanding 
*** is object based(200 for success upload)
*** key value pair
*** Puts & Deletes concepts??
*** remember 6 storage classes 

*** name that is unique to you 
*** bucket that is global or you can in different region 
*** you can replicate the content 
*** encyrption & different options
*** Restricting bucket Access 
****policy 
****object policies(individual policies ((this needs to be defined both ways for users to access)))
****IAM to restrict bucket access for different departments
***Host website for a large number (static, server side rendered, client side rendered) 

##Cloud Front 
### A big CDN(definition)
** edge locations. location where the content wil be cached 
** origin this si the of all the files that the cdn wil distrubute
** cloud front caching when second user access the same resource stored very far
** ttl cache expiry date 
## terminology: 
*web distribution 
*rtmp 


##Elastic Compute Cloud (EC2)
###What is it?
*Is the server that is scalable and durable for you're services 
*It removes all IT infrastructure needed
*It provides a virtual machine for people to use 
###Pricing 
*On demand
** pay fixed rate
** not long term engage with app (good for testing)
*Reserved 
** contract for hours
** predicatable usage or steady state 
** user are able to make upfront payments to save them money
** standard these offer up 75% off on demand 
** convertible these offer upto 54% of on demand capability to change the attrubites of RI. 
** scheduled reserved instances: there are abaliable to launch wihtin the time withoy you reserved 
*Spot
** bid a price that you want to pay. 
** application that have flexible start and end times
** appl that are only feasible at very low compute prices 
** user twith ugent comuting need for landge of addicional capacity 

*Dedicated hosts
** Physical dedicated server for you. softwre license that you might need
** useful for organization that may not suoort multi tenant virstyallsation 
** can be purchesed on demand 
** can be puschesd as  arevesation 
## What is EBS
*is the virtual hard disk for used on the EC2. 
* you can install anything needed on it to do you're stuff 
*EBS are replicated around you're regions
##What is SSD?
*Genral Purporse SSD (GP2) balances price and perfomance for a arent of worloads 
*prviosed IOPS highe peromase ssd colume mission low latency of high though 
*magnetic thourgh optimsed low const vlument deisgn for frequelty access 
###exam tips
*use  aprivate to conncet to EC2 (do not share you;re private key)
*administer the on linux servser on port 22
*firewall is between the computer and communicator
*always deisng for failure (multiple avaliablity zones)

##you can interact with AWS environemnt
*using console


##Roles 
* need to redo the course and re study it. try to login to aws using ssh  
* roles are universal


##Load balancers 
###Types of load bal 
*app load bal 
** 
*net lad bal 
*classic load bal 

##Databases
###multi a-z
*for disaster recovery 
*one fails you can use the other
###read replicas
* for performance enhancement

## Redshift 

## Elasticache 
* It's a wenb serviace that meakes it easy to deploy operate, and scale and in memory cacne in the cloud.
* memcache; redis (elastci cache engine)
* red shift olap

### Route 53
* amazon DNS service 
* you can use it to direct traffic all around the world
* it's global similiar to IAM and S3

## Elastic Beanstalk 
### What is it?
* a way of deploying AWS resources
* deploy and manage AWS cloud services
  
## RDS (Relational Database Service)
* Multi A-Z for disaster recovery 
* Read Replicas - For Performance 

## Cloud Formation 
 ### What is it?
 * Turns you're infrastructure into code. You can create an infrastructure in minutes through writin code.
### What are templates?
  * Templates are files that are used to create the stack. 

## AWS Global Services
### Which AWS service are global?
* IAM
* Route53
* CloudFront
* SNS
* SES (Simple Email service)

ther are some that offer global view but regional services

## AWS services on premise
### Which ones?
* Snowball
* Snowball Edge (computer wiht storage lombda functions as well as storage)
* Storage Gateaway (virtual machine or physical ddevice. Caching you;re file from you data unit into S3. Having files storate)
* CodeDeploy to deploy application on premise. 
* Opsworks cheif to automated deployment into ec2 or on premise web service
* IoT green grass on premise service as well??


## AWS Architecting 
### Tradiotnal vs cloud 
* IT assets as provisioned resources 
* Global, avaliable and scaleable capacity
* HIgher level managed services (you can use these higher level management services)
* Built-in security (MFA, access key, sec key)
* Architecting For Cost (ac loud gugru pays 400$ though serverless)
* Operations on AWS (re factory)
* Re architecture
  ### Scalabity
  * Scale up (increasing amount of RAM, and CPPU in virtual machine)
  * Scale out (more virtu mahcine)
    * Stateless Applications (lambda) 
    * Distribute load to multiple nodes
    * Stateless componenets (personalize information login or something)
    * Statefull compoenents (cookies in user browser to know that they are purchasing. store this information on database)
    * Implement Session Affinity (sticky session for one particular CPU)
    * Elastic map reduce (large complex jobs. Fleets of EC2 to do stuff)
  ### Disposable  resource instead of fixed sersers
    * Instaing compute resources 
      * boostratpping 
      * golden images (deployng on ec2)
      * containers
      * Hybrid
    * Infrastrucre as code 
      * CloudFormation  (build you're cloud in code)
      * Serverless management and deployment (lambda & deployment)
      * Infrastrucure management and deployment
        * AWS Elastic beanstalk 
        * Amaza EC2 auto recoery 
        * AWS system manger
        * Auto scaling
    * Alamsn and events 
      * Cloudwath elerms 
      * Cloudwatch events (uploading S3. Responding to a change to the envinronemt)
      * AWS lambda scheduled events
      * WAF in front of it securty automations 
  * Loose coupling(how do you achieve this) Asynchronous integration
    * Wel devined interfaces 
      * amazon api GATEWAY (designer)
    * SERVICE discovery
      * implement service discovery (EC2)
  * Distrubited systems 
  * Service not server 
    * Mnaged services 
    * serverless architecures
  ### Databases
  * Relations detabases
    * Scalability 
    * Joinsd & stuff 
  * No SQL
    * Dynamo DB
    * HIgh avaliability Multi A-Z
  * Data wareohuse
    * Red shift
      * scalabity 
      * pnline transactions processing
  * Search
    * Scalability
    * High availability 
  * Graph databases
    * Amazon neptune 
    * High avaliability 
    * Scalability
  * Manageing encaresing volume data
    * Data lake 
    * Lots of data readility avaliable to be consumed & etc. 
    * You can store them in S3 with athena
  * Removing sinle point of failure
    * INroduicng reducndancy 
    * DEtect failure 
    * Durable data storeage 
    * Automated muti data center eseilienc e
    * Fault isolation tradional horizantal scaling
    * Vertical scaling 
    * Sharding data (ES)
  * Opitmize for Cost 
    * Risht sizing 
    * Elasticity(Blakc Friday)
    * Take advanatege of the viarue of purchasing 
  * Caching 
    * APlication cahcine 
    * edche cachine (elastic cache)
    * cdn cackche 
  * Securoty 
    * Use AWS features for dehense in depth
    * Share security responsibility with AWS
    * Reduce priviliged accesss
    * Security as code
    * Golden environments
    * Real time auditing (you're environment
  * Exam tips
    * read the white paper
  ##Cloudwatch 
    ### What is it?
        * MONITOR    youre aws resources
        * Compute
        * EC2 INSTANCE AUTOSLACING GROUPS 
        * ELASTI LOAD BALANCER
        * ROUTE 53 HEALTH CHEKS 
      * STORAGE & CONTENT DELIVERY
    * EBS volume 
      * Storage gateways 
    * Host level mtecics cosnts of 
      * CPU 
      * Netword
      * Disk 
      * Status 
  * Exam tips
    * what is it suded for?
    * can watch most of aws
    * you creat costum metrics (inside the SDK)
    * EC2  will mnitor it events by default 
    * you can turn the detail monitorin 
    * overrall is about performance monitoring
  ## AWS Systems manager (ec2 fleet example ot install the software of the system manageer to run a commnad on multiple instances)
  * exam tips 
    * systema cna be use to manange a fleet of ec22
    * a piace of sotawre is isntalle don each C,
    *can be both inside the aws on and primise 
    run command is used to install path unistal software

## Summary of cloud coneptes en technology
    ### Know the 6 advantages of the cloud 
    * Choosing the right aws region?
      * Data sovereginity laws 
      * latency to end users (where are you're users) 
      * AWS services (if you need the latest then you might want to use the north virgiania)
    * Understand teh different support packages
    * Billing alerts
    * IAM (it's global) create user of group
  
  
