# sirawit_shop

After completing my first project, I took some time to learn more about web development technologies and then started my second project, which I named 'Shop'. The project is called 'Shop' because it is designed to simulate an online shopping experience, including features such as browsing products, adding items to cart and removing items from cart. On the client-side, I used 'React' and 'Redux' to manage state in 'React'. On the server-side, I used 'Golang'.

The server-side is built on the hexagonal architecture pattern and follows the microservices concept. The server-side consists of 4 distinct services: 'User', 'Product', 'Logger' and an asynchronous queue named 'Worker'. All these services are deployed on Amazon Elastic Kubernetes Service (EKS) using Github Actions.

The client-side of our application is able to connect only to 2 of these services via REST API: 'User' and 'Product'. The 'User' service handles tasks such as logging in and registering. The 'Product' service is responsible for the cart system and browsing products.

Whenever a user logs in or registers, the 'User' service sends user information via GRPC to the 'Logger' service, which inserts a login timestamp into the database. Addtionally, the 'User' service sends a task to the 'Worker' service to send a welcome email to a new user.

Thank you to everyone who has taken the time to review my project, and I promise to continue improving my skills and knowledge in the field of software development. Have a pleasant day, everyone! :D
