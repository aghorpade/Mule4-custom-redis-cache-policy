# Mule4-custom-redis-cache-policy
This is repo for Mule 4 custom HTTP cache policy backed by redis

HTTP Custom policy backed by redis cache
home
The HTTP Custom Caching policy enables you to store HTTP responses from an API implementation or an API proxy for reuse. To optimize against computation-heavy processing, this policy avoids performing multiple calls to the backend when the response of a service does not change often. This policy uses a cache, which enables a faster service for data requests.

In Mule 4 mulesoft already provide HTTP cache policy which is available out of the box with standard configuration and works very well with runtime object store v2. If existing out of box of policy is available then why do we need custom policy.

This means your runtime application needs to be deployed on cloudhub , runtime applications deployed on customer hosted runtime can’t use this in built policy
it works with standard configuration while in case if you need custom configuration or expression to be used to pick up key then it is not possible with out of the box policy
In this custom cache policy- cache is backed by redis storage which is an open source (BSD licensed), in-memory data structure store, used as a database, cache, and message broker. In this example we are using upstash service provider for redis as they provide on cloud redis and 5mins to get a new redis instance(trial version)

This custom cache policy flow is shown as below -

<img width="603" alt="custom cache policy" src="https://user-images.githubusercontent.com/5318345/117317137-25048700-ae81-11eb-86f8-0b46eb0b60ee.PNG">


create a trial redis server for us on upstash. it takes 5min to get a redis database and can do testing using redis-cli . ref-  Getting Started | Upstash: Serverless Redis, Documentation 

Additional References
Redis
HTTP Caching Policy

Code repo - https://github.com/aghorpade/Mule4-custom-redis-cache-policy

how to develop mule 4 custom policy- https://docs.mulesoft.com/api-manager/2.x/policies-managing-custom-policies
