*setup*:
Google app engine is a lightweight, serverless and super easy tool that can be used to deploy read only serverless apps that scale to 0 and are extreamly efficient. to build an app engine app all you need to serve static content is an app.yaml, and index html inside a www/ directory

*Deployment*:
this is a basic app engine web app, the app.yaml specifies the apps runtime, its instance class wich governs how the instance is managed, and handler scripts for urls.

*Management*:
the instances scale under a app -> service -> version -> instance model where the application is a top level container. 
-services behave like micro services so you can run your whole app in a single service or you can design and deploy multiple services to run as a set of microservices. 
-Versions allow for app rollbacks, testing or traffic routing between identical versions via splitting traffic. 
-and instances are read only instances thats scale to match load to provide consistant performance, and scale down to minimise cost.
we have specified our instance class as an F1, this is automatic scaling witch use dynamic instances that get created based on request rate, response latencies, and other application metrics. you can also specify a minimum number of idle instances and a maximum number of instances.
