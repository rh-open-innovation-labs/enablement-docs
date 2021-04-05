<!-- .slide: data-background-image="images/RH_NewBrand_Background.png" -->
## DevOps Culture and Practice <!-- {_class="course-title"} -->
### Continuous Integration, Delivery, and Deployment <!-- {_class="title-color"} -->
DO500 <!-- {_class="title-color"} -->



<!-- .slide: id="continuous-integration" -->
## Continuous Integration



### Continuous Integration
Continuous Integration (**CI**) is a development practice where developers integrate code into a shared repository frequently, 
preferably several times a day

These actions are repeated frequently ensuring that the code base can **continuously integrate**



### Continuous Integration
#### _What is It?_
* Developers submit **small and frequent changes** to the source code
* **Automated** build and test steps are run to ensure code works as expected
* Developers are notified if anything fails and developers react quickly to fix
* The tests and build steps are typically run in an automation server (Tekton, Jenkins, GitLab CI/CD, Apache Airflow...)



### Continuous Integration
#### _Why Use It?_
* Automated testing reduces busy work and improves software quality.
* Small, regular code commits reduce the number of integration problems.
* Rapid feedback loops make it easier for new contributors to get started.
* Shipping of functional software in small increments is more enjoyable than 
waiting for someone to manually test a giant code change.




### Jenkins Pipeline
![Jenkins](images/cicd/pipeline.png)



### Tekton Pipelines
![Tekton](images/cicd/tekton.png)



<!-- .slide: id="continuous-delivery"-->
## Continuous Delivery



### Continuous Delivery
Continuous delivery (**CD**)  is an extension of continuous integration since it automatically deploys all code changes to a testing and/or production environment after the build stage. 



### Continuous Delivery
#### _What is It?_
* A software engineering practice
* Each change can be **potentially** ready for release to production
* Builds upon the **continuous integration** practice
* Consider automating release to a "demo" area
* Typically implemented with an automation server such as Jenkins or Tekton



### Continuous Delivery
#### _Why Use It?_
* Automation reduces the manual work required to do a release
* Faster feedback cycles from quality engineers, product owners, and stakeholders
* Produces a happier operations team
* Prepares the way for push button deployments



<!--.slide: id="continuous-deploymen" -->
## Continuous Deployment




### Continuous Deployment
Continuous deployment (**CD**) is a strategy for software releases wherein any code that has been committed which passes the automated testing phase is automatically released into the production environment, making changes that are visible to the software's users




### Continuous Deployment
#### _What is It?_
* Software development practice
* Development team maintains software so that it can be **released to production** at any moment
* Builds upon the practices of **continuous integration** and **continuous delivery**
* Software configuration and deployment orchestration becomes part of the
development team's duty to maintain the software



### Continuous Deployment
#### _Why Use It?_
* Team maintains deployable code and configuration over new features
* Fast feedback from end users
* Features can be pushed out after completion
* Enforces best practice of **eveything as code**
* Configuration and deployment orchestration needs to be part of automation
* Enables quick rollbacks and recovery from failures



### Continuous Deployment
#### _How to Do It?_
* Collaborate closely with everyone involved in deployment and delivery of software
to production
* Automate everything as much as possible
* Build "feature toggles" or "dark launches" to allow for quick rollback if needed
* Provide adequate automated monitoring of the application



<!-- .slide: id="pre-attack-pipelines-summary"-->
## Summary



<!-- .slide: id="pre-attack-pipelines-summary"-->
## Summary
#### Wrap-up
* **Continuous Integration**: Integrate several changes into a shared repo and rely heavily on testing to make sure that the changes and commits works and have passed all (unit testing / code quality / code conduct).
* **Continuous Delivery**: The goal is to have a working artifact that's ready to be deployed at any time. It relies on testing and automation to make sure that it has passed all functional tests and can be Manually deployed (push button).
* **Continuous Deployment/Release**: One step further now that we are sure that this is ready to deploy to production then we can rely on features toggle, dark launches or other deployment strategy to promote to other critical environments asap using these techniques for the new features/fixes won't risk the operation.



## Summary
![Pipeline](images/cicd/cdcd.png)



<!-- .slide: id="attack-pipelines"-->
## The Attack of the Pipelines



### Lab Exercise 2: The Attack of the Pipelines
* This exercise is all about creating a pathway to production from source
to a live application
* We explore the sample TO DO List application
* We create a Jenkins pipeline to build and deploy our code
* As a learner you will be able to:
  1. Build and run the full stack of the TO DO List application locally
  2. Create an un-gated pipeline using the Jenkins user interface for
  the backend and frontend of the application
  3. Add branching to the pipeline to target a specific OpenShift namespace




### Why are pipelines important and how do they help?
* A pathway to production:
  * Puts the product in the hands of the customer more quickly
  * Enables seamless and repeatable deployments
  * Using a more production-like infrastructure increases assurance of quality
  * "We have already done it"-behavior reduces risk of going live
* Assurance: drive up code quality and remove the need for dedicated deployment
and release management teams
* Freedom: allow developers to take ownership of how and when code gets built and shipped
* Reliability: pipelines execute the same way each and every time they are run



### What new Tools and Frameworks will we use?
* **Jenkins**: Open source build automation server that is highly customizable
via plugins.
* **Node.js**: Node.js(R) is a JavaScript runtime build on Chrome's V8 JavaScript
engine. It uses an event-driven, non-blocking I/O model that makes it lightweight and efficient.
* **MongoDB**: A data store for JSON-like documents giving flexibility to data structures.
* **VueJS**: A progressive framework for building user interfaces known as single-page
applications.



### The Big Picture
![BP2](images/cicd/bp-2-attack-pipelines.jpg)



### Let's Go!!!
Lab Exercise 2: _The Attack of the Pipelines_



<!-- .slide: data-background-image="images/chef-background.png", class="white-style" -->
### DevOps practices used in this section:
- [Continuous Integration](https://openpracticelibrary.com/practice/continuous-integration)
- [Continuous Delivery](https://openpracticelibrary.com/practice/continuous-delivery)
- [Continuous Deployment](https://openpracticelibrary.com/practice/continuous-deployment)
