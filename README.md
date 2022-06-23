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
