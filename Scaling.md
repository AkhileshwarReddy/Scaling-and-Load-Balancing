Consider you have a server up and running, which has a good amount of traffic. Your server can handle that traffic easily. What about when the traffic is huge? As the traffic increases, the load on the server also increases. Available resources are not sufficient at this point. Due to this, Your server responds to the requests slowly. In the worst-case scenario, The users may get the worst experience.  

To avoid such problems, you've to design a scalable system.

## **What is Scaling?**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Scalability is a characteristic of the system to perform well under an increased or expanded workload. A scalable system can handle the growing amount of work by adding resources to it.

Typically, Scaling falls under two categories.  
- Horizontal Scaling
- Vertical Scaling

### **Horizontal Scaling**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Horizontal Scaling means adding more nodes or machines to the system/server pool. This can also be described as **scale-out**. An example for horizontal scaling is adding more servers to the server pools.

### **Vertical Scaling**  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vertical Scaling means increasing the resources of the existing server. Typically, increasing processing power of the server by adding more memory, more CPU's.
Vertical Scaling can also be described as **scale-up**.

## **What to Choose? Scale-out or Scale-up?**
We've to consider various factors in choosing between the two. They are:
- **Performance** - Horizontal scaling/Scale-out allows you to combine the power of all the machines in the server pool as a single virtual machine. It's worth working out if you have a single machine to meet your scalability needs.

- **Flexibility** - If you have the flexibility to choose the optimal configuration setup for better performance at optimal cost anytime, then scaling out might be the better option. If there is a minimum price set by the hardware you are using, then scaling up is the better option.

- **Regularity of Upgrades** - In vertical scaling, Whenever you want to upgrade the system, you've to bring down the entire system. Whereas in horizontal scaling, you just need to decouple the system, you want to upgrade from the pool.

- **Redundancy** - Vertical scaling has a single point of failure as there is one large system. If the system fails, the user may not get their services. Whereas in horizontal scaling, if one system in the pool fails, the rest of the server pool continues the services.

- **Geographical Distribution** - If you need to spread the application across the globe or in different data centers to reduce latency geographically or to handle the disaster recovery scenarios, then you have only one option. that is scale-out.

## What is Load Balancing?
Load balancing is nothing but distributing the network traffic across multiple servers or a server pool.

A Load balancer routes the client requests across the servers in the server pool capable of serving each request and ensures that no one server is overloaded.
If any of the servers fails, the requests are redirected to the remaining servers. If a new server is added to the pool, the load balancer automatically sends requests to it. Load balancer sends requests only to the servers that are online to ensure availability and reliability.

There are different Load Balancing Algorithms to specify how to route the requests across the servers. Different algorithms provide different benefits. You've to choose the algorithm based on your needs.

- **Round Robin** - Requests are distributed sequentially across the server pool.
- **Least Connections** - New request is sent to the server with less connections.
- **Least Time** - Requests are sent to the server select by a formula that combines the fastest response and fewer connections.
-  **Hash** - Requests are distributed across the pool based on a key that you define.
-  **IP Hash** - client IP address is used to determine which server serves the request.
-  **Random with Two Choices** - Two random servers are picked. The request is sent to the server with less connections.

## Resources
https://en.wikipedia.org/wiki/Scalability  
https://en.wikipedia.org/wiki/Load_balancing_(computing)  
https://www.nginx.com/resources/glossary/load-balancing/  

