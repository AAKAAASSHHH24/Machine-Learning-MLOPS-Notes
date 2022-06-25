# Machine-learning-Notes

MLOps is an ML engineering culture and practice that aims at unifying ML system development (Dev) and ML system operation (Ops).

In the following, we describe a set of important concepts in MLOps such as Iterative-Incremental Development, Automation, Continuous Deployment, Versioning, Testing, Reproducibility, and Monitoring.

The complete MLOps process includes three broad phases of “Designing the ML-powered application”, “ML Experimentation and Development”, and “ML Operations”.

DESIGN >>>>>> DEVELOPMENT >>>>>>> OPERATE

![mlops-loop-en](https://user-images.githubusercontent.com/101935492/175368951-ff4a6f4c-cc2d-46f6-a4a8-c750385bc9b9.jpg)

The first phase is devoted to business understanding, data understanding and designing the ML-powered software. 

Initially, we define ML use-cases and prioritize them. 
The best practice for ML projects is to work on one ML use case at a time. 

Furthermore, the design phase aims to inspect the available data that will be needed to train our model and to specify the functional and non-functional requirements of our ML model. 
We should use these requirements to design the architecture of the ML-application, establish the serving strategy and create a test suite for the future ML model.

The follow-up phase “ML Experimentation and Development” is devoted to verifying the applicability of ML for our problem by implementing Proof-of-Concept for ML Model. Here, we run iteratively different steps, such as identifying or polishing the suitable ML algorithm for our problem, data engineering, and model engineering. The primary goal in this phase is to deliver a stable quality ML model that we will run in production.

The main focus of the “ML Operations” phase is to deliver the previously developed ML model in production by using established DevOps practices such as testing, versioning, continuous delivery, and monitoring.


Automation:
The level of automation of the Data, ML Model, and Code pipelines determines the maturity of the ML process. 
With increased maturity, the velocity for the training of new models is also increased. 
Triggers for automated model training and deployment can be calendar events, messaging, monitoring events, as well as changes on data, model training code, and application code.

To adopt MLOps, we see three levels of automation:
1. Manual process. This is a typical data science process, which is performed at the beginning of implementing ML. This level has an experimental and iterative nature. Every step in each pipeline, such as data preparation and validation, model training and testing, are executed manually. The common way to process is to use Rapid Application Development (RAD) tools, such as Jupyter Notebooks.
2. ML pipeline automation. The next level includes the execution of model training automatically. We introduce here the continuous training of the model. Whenever new data is available, the process of model retraining is triggered. This level of automation also includes data and model validation steps.
3. CI/CD pipeline automation. In the final stage, we introduce a CI/CD system to perform fast and reliable ML model deployments in production. The core difference from the previous step is that we now automatically build, test, and deploy the Data, ML Model, and the ML training pipeline components.

Automated ML pipeline with CI/CD routines:

![mlops-automated](https://user-images.githubusercontent.com/101935492/175422911-5f5220b9-2ab6-4836-8735-bd528fabaf84.jpg)

The main concepts attributed to CI/CD are continuous integration, continuous delivery, and continuous deployment. It automates the machine learning pipeline (building, testing and deploying) and greatly reduces the need for data scientists to intervene in the process manually, making it efficient, fast, and less prone to human error.

Example of CI/CD pipeline (App Developer vs. Data Scientist). Source: Microsoft:

![cicd pipeline microsoft](https://user-images.githubusercontent.com/101935492/175451597-229cc70e-7982-48d7-ba94-dd7709bfca5d.png)

Machine learning pipelines consist of multiple sequential steps that do everything from data extraction and preprocessing to model training and deployment.
Machine learning pipelines are iterative as every step is repeated to continuously improve the accuracy of the model and achieve the end goal.

![model feedback](https://user-images.githubusercontent.com/101935492/175602953-37de73cd-020e-4b2d-b3c5-75163ce9edef.png)

 
The picture below shows that the model monitoring can be implemented by tracking the precision, recall, and F1-score of the model prediction along with the time. The decrease of the precision, recall, and F1-score triggers the model retraining, which leads to model recovery

![model-decay-monitoring](https://user-images.githubusercontent.com/101935492/175595397-eb6c401c-30ac-4dfd-88c4-4ce57565fb63.jpg)

ML Systems Require Extensive Testing and Monitoring. The key consideration is that unlike a manually coded system (left), ML-based
system behavior is not easily specified in advance. This behavior depends on dynamic qualities of the data, and on various model configuration choices.

![image](https://user-images.githubusercontent.com/101935492/175776217-af0cac33-cb7f-47d0-9f6b-88526cdbba46.png)

The complete ML development pipeline includes three levels where changes can occur: Data, ML Model, and Code. This means that in machine learning-based systems, the trigger for a build might be the combination of a code change, data change or model change. The following table summarizes the MLOps principles for building ML-based software:

MLops Principles:
![MLOPS PRINCIPLES](https://user-images.githubusercontent.com/101935492/175783662-9b5adc73-4b4c-4c12-b840-3babd3e1f138.jpg)

MLOps Best Practices
![MLops best practices](https://user-images.githubusercontent.com/101935492/175783754-bdf0cb0b-07d9-4158-af85-90e6d1909c07.jpg)


