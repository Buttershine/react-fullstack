# react-fullstack

What this repo's about? Fullstack framework for myself who is lazy and wants to start a project. 

Goals - to learn and to integrate the following technologies.

core: 
- react
- typescript
- node.js
- postgresql

addons:
- graphql
- redis
- elixir
- rabbitmq

Identify the following for any system:
	Actors
	Actions
	Assumptions (System)
	Latency
	Consistency
	Availability
	Throughput
	Data

E.g. Instagram 
	Brainstorm Features:
Upload images
users follow users
Generate feed of images
Scale: 10 million users

Actors: Users
Assumptions 10 million users monthly
2 photos per month
5 MB per photo
10^7*2*5MB = 100,000,000 1 hundred million MB per month = 100 TB = 1.2PB a year
Data Model:
	Users, Photos	

Reduce bottlenecks: Caches, Queues, Delay Computation, Parallel processing
Use caches, reducing network and disk bottlenecks. But remember that knowing when to evict from a cache eviction can a hard problem in some situations.
Use message queues to decouple components in the system. This way you can add more hardware to specific parts of the system that need it.
Delay computation when possible (often by using message queues). This takes the heat off the system during high-processing times.
Of course, design the system for parallel processing wherever possible. One host doing processing is NOT scalable. Note: most relational databases fall into the one-host bucket, this is why NoSQL has become suddenly popular; but not always appropriate (theoretically).
Use eventual consistency if possible. Strong consistency is much harder to scale.
