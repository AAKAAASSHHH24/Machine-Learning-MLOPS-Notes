# Machine-learning-Notes

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
