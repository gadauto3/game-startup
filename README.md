# Game Microservice Architecture and Pipeline
The following architecture and pipelines supported an audience of 200K students playing cross-platform mobile games that reported student concept mastery and behavioral data to their teachers and admins on a responsive site.

## Architecture

![alt text](startup_game_architecture.png "Startup Game Architecture")

*Benefits:*
1. Using CloudFormation for deployments provided a simple and efficient way to create and manage all of the necessary AWS resources, allowing for quick releases and scaling with demand, ensuring that the gaming experience remained smooth and uninterrupted for all users.
2. Scala is a powerful programming language that allowed for efficient and scalable data processing, making it an ideal choice for the backend of a gaming application with heavy data reporting needs. Its functional programming features make it easy to write highly modular, reusable, and well-tested code for asynchronous data processing, leading to faster dev times and reduced maintenance/testing costs.
2. MongoDB is a highly scalable, flexible NoSQL DB, making it an excellent choice for gaming applications that require fast and reliable data access. Its ability to handle large amounts of unstructured data allows for the storage and retrieval of complex data that changed regularly due to the evolutions of the games to improve learning and fun.
3. WebGL artifacts embedded in an AngularJS site and native iOS apps provided responsive and interactive UIs that were accessed from the devices and platforms most important to our users.
4. REST APIs were secured by API keys and TLS encryption ensuring that all data transmitted was kept private and secure, protecting sensitive user data from potential security breaches.
5. The use of Nginx as a reverse proxy helped to distribute the workload evenly across the EC2 instances, improving the overall performance and reliability of the system.

*Overview:*
This architecture for cross-platform mobile games consisted of components designed to provide a seamless and secure gaming experience. The system was deployed using AWS CloudFormation, which provided a simple and efficient way to create and manage all of the necessary AWS resources, allowing for easy scaling as demand grew and ensuring that the gaming experience remained smooth and uninterrupted for users. The backend was built using Scala, which allowed for efficient and robust data processing while providing real-time dashboards to teachers and admins. The backend was hosted on EC2 instances and connected to a MongoDB database that stored all of the game-related data. MongoDB is a highly scalable and flexible NoSQL DB, an ideal choice for gaming applications that require fast, flexible, and reliable data access. To improve the performance and reliability of the system, an Nginx server was used as a reverse proxy to route incoming requests to the appropriate EC2 instances. 

For the frontend of the system, WebGL artifacts were embedded within an AngularJS site, providing a responsive and interactive UI. In addition to the web-based frontend, native iOS apps were also available for classrooms with iPads. All of the communication between the frontend and backend was done through REST APIs secured using API keys and TLS encryption. This ensured that all data transmitted between the frontend and backend was kept private and secure.

## SDLC Pipeline

The entire SDLC pipeline along with the major tools and services we used are included below. Rather than exhaustively explain, here's some cool features:

1. Unity Cloud Build was managed by Unity itself which meant it remained compabitible as new versions were released. In addition to providing binary files that were smaller than those we generated on local computers, it also provided online previews that we leveraged for certain user tests on bleeding-edge features.
2. The ELK stack was extremely cost-effective for the startup while providing visibility across the system.

![alt text](startup_devops_pipeline.png "Startup Game Devops Pipeline")