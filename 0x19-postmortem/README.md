## POSTMORTEM: Outage on fan voting System

Issue Summary:
The fan voting system encountered an outage on December 12th, 2021, that lasted almost two hours. Users were unable to use the system’s services at this time, which had a substantial negative impact on production.

Timeline: The outage started at 12:00 PM, when users began to report problems using the system.

- 12:10 PM — The system’s monitoring systems discovered that one of the servers had a high CPU utilization rate.
- 12:15 PM — The team began looking into the problem and found that the server was overwhelmed because of heavy traffic.
- 1 …………..
- 1:00 PM — The problem persisted, and the team discovered that the method used for load balancing the system had a fault at its core.
1:30 PM: The team released a hotfix to repair the bug and get the system back to working normally.Root Cause and Resolution:
The root cause of the issue was a bug in the system’s load-balancing algorithm, which caused the traffic to be unevenly distributed among the servers. This led to one server becoming overloaded, resulting in an outage.

The problem was fixed by the team by deploying a hotfix that fixed the load-balancing algorithm error. This made it possible to uniformly spread the traffic among the servers, avoiding congestion and eventual failures.
Corrective and Preventive Actions: The team has put the following steps into place to ensure that similar problems don’t arise again:

- Consistent load testing to make sure the system can manage heavy traffic loads.
- Enhanced monitoring tools to find problems before they affect the performance of the system.
- A codebase review to find and fix any other potential problems that may exist in the load-balancing algorithm or other crucial components.

In conclusion, a fault in the load-balancing algorithm caused overloading and repeated outages, which in turn caused the outage on the fan voting system. The group responded swiftly and applied a hotfix to correct the problem. The team has put remedial and preventative measures in place to guarantee the system’s functionality and stability in order to avoid such problems in the future.
