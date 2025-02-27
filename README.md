# Cloud Infrastructure Engineering - (6 Months) Entry Assessment

## Objective

This assessment aims to test your resourcefulness, the ability to understand IT concepts, and produce a viable answer to the problems listed.

---
## Submission

- Create an account in github.com
- Fork this repository to your account
- Use the online editor to edit this file (README.MD)
- Save your changes
- Submit the URL of this repository 
- Ensure your URL is publicly accessible

---
## Expected Audience

- Individuals with an IT background to diversify/expand their skills and/or intending to switch to a software developer role.
    - Those with IT or Engineering degree/diploma, or
    - Those with IT or Engineering experience professionally
- Individuals with systems and infrastructure administration background.
- Individuals who have attended basic infrastructure or cloud courses.

---

## Problems

Please attempt the solve the problems described:

**Question 1 - IP Address**

What is the Bash command to discover the IP Address of `www.skillsunion.com`?

```sh
 nslookup www.skillsunion.com
 or 
 host www.skillsunion.com
```

---

**Question 2 - Copy a Directory**

What is the command to copy a directory from `~/my_project` to `/etc/projects`?

```sh
 sudo cp -r ~/my_project /etc/projects
```
---

**Question 3 - Shell Scripting**

Implement a bash script that does the follow:
1. Convert a string "one,two,three" into an array delimited by comma (,).
1. Loop through the array and print each element.

```sh
 #!/bin/bash
 var="one,two,three"
 IFS=,
 array=( $var ) 
 for i in "${array[@]}"
 do echo "$i"
 done
```

---

**Question 4 - System Architecture Diagram**

Use [draw.io](draw.io) to draw a system architecture diagram as described below:

- A load balancer to manage request between 4 application servers.
- The load balancer is connected to the internet gateway.
- All application servers are connected to a cluster of database.
- The cluster of database contains an instance for reading and another instance for writing.
- The database must not be connected to the internet gateway.

Share the link to your image of diagram.

```sh
https://drive.google.com/file/d/1y79-J5DsORwV6zErObfyj_nfDCL83Q4N/view?usp=sharing
or
https://drive.google.com/file/d/1hDPtcKGaLpYBTmxWE1vbZfiEnvxIviQF/view?usp=sharing
```
---

**Question 5 - System Error Management**

Alan has deployed his web application to Amazon Web Service. Unfortunately, the web application encountered errors as complained by the customers (public users). Whenever there is a complaint, Alan would take a long time to trace the issue and get back to the customers. 

*Q5A: Which of the following described the scenario given?*

A - The principle of security is not applied.

B - The principle of observability is not applied.

C - The principle of availability is not applied.

D - The principle of performance is not applied.

*Q5B: What do you suggest could be done to improve the situation?*

```
Q5A
B: The principle of Observability is not applied. The fact that 
Alan takes a long time to trace the issues implies Alan probably 
has not made full use of the tracking resource availabile in the
OS to do trouble shooting, which can save a lot of time.

Q5B
According to IBM, the principle of observability requires a few 
things, namely logs, metrics, traces and dependencies. First, he 
should do tracing by getting records of users experience describing
its "end to end" journey from the UI through distributed architecture 
and back to the user. This can enable Alan to reproduce user 
experience to get first hand feeling of what problem the client is 
facing. Then he should look at the system and applications log to 
find out what are the specific issues that lead to the problem. 
Sometimes looking at the metrics such as application performance, 
memory usage etc can provide some hints of the issues arising 
from using the application, and check if some of the dependencies
of the applications are out of date. 
```

---

END
