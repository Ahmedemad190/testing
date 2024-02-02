# GIT WORLD


## what is git ?
VCS can handle s/w versions , which allow devs to contibute to the same project , __revert changes__ , collaborate to **create new feature**  
and it allows to __track the changes__

# Before git ? 
Devs use CVCS but those systemd had limitiaions and make a lot of backup of entire codeBase 
## now let's begin with the Concepts 

- Repo :
  is a container contain the files of a project with the help of the repo u can track the changes
- Push :
    to upload the code to the desired repo u can push code or branch **while be explanied up next**
- Pull : to get the project from the remote
- Branch : u can use branch when you need to make testing or add new feature without affect on the original copy
- untracked : server has no info about it u should  commit them 
- remote repo :  company'server where Devs pushe the code , github-gitlab 
- commit : after  finishing a feature fix bug ,etc like a checkpoit in ur local repo 
- tag : like a bookmark
- Annotated Tags : like bookmarks to tag an important commits you can mark it as a version and name the version with it's number insted of wasting hours searching in logs 
# how to create a repo 
- first choose the PATH : cd /PATH/TO/FILE
```
git init "repo_test" 

```
# get info about files :
```
git status
```
then you will get the info about the files if u hadn't commit anything yet , so it will get u the untracked msg 
first step you need to stage the changes 

___git add___ command put the fiels into staging area to be tracked 

```
git add <file_name> or use . if u wanna add all files in the file you are in
```
## remote : 
the version of the repo that hosted on a server or other location like github , gitlab outside ur local machine 

- to view remotes
```
git remote -v
```
if u get a blank space then u need to add ur remote by 
```
git remote add origin <repo_url>
```

let's assume that u get an idea and u need to test it away from the original repo , so u need to create new branch with 
```
git branch <Branch_name>
```
when u are done with ur new branch u need to merge the branches by 
```
git merge source 
```
- to switch to the branch you have created
  ```
  git swtich  <Branch_name>
  ```
- delete a branch
  ```
  git branch -d <branch_name> 
  ```
you need to mark a specific commit so u need a tag 

- first choose the commit by __git log___
then
```
git tag -a <Version-name> <commit-hash>

```
replace the version_name with yours 
to list the tags avaliable in the repo 
```
git tag
```
if u done tagging push the tag to remote 
```
git push origin <tag-name>
```
| Command | Description | 
| --- | --- | 
| git clone <URL> | clone ur local to remote  | 
|git init <repo_name>| create a repo |
| git status | List all new or modified files |
| git add | command put the fiels into staging area to be tracked |
| git commit| save your changes to the local repository. When you make changes to your project add -am for comment|
|  git add . -A | is used to stage all changes in your working directory  |
| git remote -v| to view remotes|
| if u get a blank space then u need to add ur remote  |git remote add origin ___<repo_url>___ |
| let's assume that u get an idea and u need to test it away from the original repo , so u need to create new branch with| git branch <Branch_name> |
when u are done with ur new branch u need to merge the branches by| git merge source |
| to switch to the branch you have created | git swtich  <Branch_name> |
|delete a branch | git branch -d <branch_name> |
| you need to mark a specific commit so u need a tag | git tag -a <Version-name> <commit-hash> |
| replace the version_name with yours to list the tags avaliable in the repo |  git tag |
|if u done tagging push the tag to remote  |  git push origin <tag-name> |
|fetch changes  | git pull <url>|
| git stash  | command is used to temporarily save changes that you don't want to commit at the moment |
| git stash pop |  to apply changes from last stash it's oppiste of git stash | | testing |


# Essential protocols  

http : It is an application layer protocol that allows for the transfer of various types of data, such as text, images, and multimedia, between clients and servers. It works on __port 80__

# :warning: Here are some features that HTTP has 
- HTTP is stateless : mean any request from client to server is standalone request
- HTTP methods :

GET: Retrieve data from the server.

POST: Submit data to be processed to a specified resource.

PUT: Update a resource or create a new resource if it does not exist.

DELETE: Request the removal of a resource.

## Headers:
Both requests and responses include headers, which provide additional information about the request or response. Headers can include details like content type, length, date, and more

## Status Codes:
HTTP responses include status codes that indicate the outcome of the request. Common status codes include . 
- 2xx: Success
- 3xx: Redirection
- 4xx: Client errors (e.g., 404 for "Not Found")
- 5xx: Server errors (e.g., 500 for "Internal Server Error")  

## security 

- HTTPS (HTTP Secure) is a secure version of HTTP that uses encryption (usually TLS/SSL) to secure the data transmitted between the client and server. It helps protect against eavesdropping and tampering of the data during transit.

# :warning: HTTPS 
is a secure version of HTTP (Hypertext Transfer Protocol) used for secure communication over a computer network __uses port 443__

Here's a brief overview of HTTPS:

## Encryption : 

- It uses protocols like TLS or SSL to encrypt the data transmitted between the client (web browser) and the server. This encryption ensures that even if someone intercepts the communication, they would only see encrypted data, making it difficult to decipher.

## Secure Data Transmission

- HTTPS is designed to provide a secure channel for the transmission of sensitive information.

# Required for Modern Web Security Standards   
- The usage of HTTPS is encouraged or mandated by numerous contemporary web security best practices and standards. For instance, in order to comply with security regulations, websites that handle sensitive data or integrate with payment systems frequently need to use HTTPS.
  
# :warning:  DNS

DNS, or Domain Name System, is a hierarchical and distributed naming system that translates human-readable domain names into IP addresses, allowing users to access resources on the internet using easily memorable names instead of numerical IP addresses.

- Domain Names:

Domain names are human-friendly labels used to identify resources on the internet. For example, "www.example.com" is a domain name. Each domain name corresponds to a unique IP address.

- IP Addresses:
IP addresses are numerical labels assigned to devices on a network.

- Hierarchy :
The DNS hierarchy is organized into levels. The rightmost label of a domain is the top-level domain (TLD), such as ".com" or ".org." The next label to the left is the second-level domain (SLD), and so on. For example, in "www.example.com," ".com" is the TLD, "example" is the SLD, and "www" is a subdomain.

- DNS Resolution Process:
When you enter a domain name in a web browser, your device initiates a DNS resolution process to find the corresponding IP address. The process involves multiple steps, including querying DNS servers, starting from the root DNS servers, then moving to TLD servers, and finally reaching authoritative DNS servers for the specific domain.
- DNS Servers:
DNS servers store information about domain names and their corresponding IP addresses.

- Root DNS Servers: The starting point of the DNS hierarchy.
- TLD DNS Servers: Handle information about top-level domains.
- Authoritative DNS Servers: Store specific domain information
# caching 
- To improve efficiency and reduce the load on DNS servers, DNS resolvers and clients often cache DNS responses Cached information can be used to quickly resolve subsequent requests for the same domain.

# DNS Records:
DNS records are data entries associated with domain names Common types of DNS records include:

- A (Address) Record : Maps a domain to an IPv4 address.
- CNAME : Alias of one domain to another.
- MX : Specifies mail servers for the domain.
- NS : Identifies authoritative DNS servers for the domain.

# :warning:   SSL  

SSL stands for Secure Sockets Layer. It is a standard technology used to establish a secure and encrypted link between a web server and a web browser. SSL ensures that the data transmitted between the web server and the browser remains private and secure, protecting it from potential eavesdropping or tampering  SSL prevents unauthorized access to data by encrypting it while it is transferred between the user's browser and the server. This is especially crucial when sending sensitive information over the internet, such credit card numbers, login credentials, or personal data.

# :warning: TLS 

TLS stands for Transport Layer Security It is a cryptographic protocol designed to secure communication over a computer network. TLS evolved from its predecessor, SSL (Secure Sockets Layer), and is a more modern and secure version. 
Ensuring data integrity and privacy between two communicating applications is the main goal of TLS.

- Features of TLS :
- Encryption:TLS uses encryption algorithms to encode the data transmitted between the client and server This helps protect sensitive information from eavesdropping.
- Authentication: TLS supports various methods for authenticating the identities of the communicating parties. This helps ensure that users are connecting to legitimate servers and not falling victim to man-in-the-middle attacks.
## :warning: What is OSI model ? 
is a reference framework that explains the process of transmitting data between computers. It is divided into seven layers that work together to carry out specialised network functions, allowing for a more systematic approach to networking.

- Physical Layer – Layer 1
The lowest layer of the OSI reference model is the physical layer. It is responsible for the actual physical connection between the devices. The physical layer contains information in the form of bits. It is responsible for transmitting individual bits from one node to the next. When receiving data, this layer will get the signal received and convert it into 0s and 1s and send them to the Data Link layer, which will put the frame back together.
- Data Link Layer – Layer 2
The data link layer is responsible for the node-to-node delivery of the message. The main function of this layer is to make sure data transfer is error-free from one node to another, over the physical layer. When a packet arrives in a network, it is the responsibility of the DLL to transmit it to the Host using its MAC address. 
- Network Layer – Layer 3
 The network layer works for the transmission of data from one host to the other located in different networks. It also takes care of packet routing i.e. selection of the shortest path to transmit the packet, from the number of routes available. The sender & receiver’s IP addresses are placed in the header by the network layer. __used protopcls__ ip,icmp

- Transport Layer – Layer 4
The transport layer provides services to the application layer and takes services from the network layer. The data in the transport layer is referred to as Segments. It is responsible for the End to End Delivery of the complete message. The transport layer also provides the acknowledgment of the successful data transmission and re-transmits the data if an error is found. __used protocols__ TCP,UDP 

- Session Layer – Layer 5
This layer is responsible for the establishment of connection, maintenance of sessions, and authentication, and also ensures security. 

- Presentation Layer – Layer 6
The presentation layer is also called the Translation layer. The data from the application layer is extracted here and manipulated as per the required format to transmit over the network. ___used protocols__ SSL/TLS

- Application Layer – Layer 7
At the very top of the OSI Reference Model stack of layers, we find the Application layer which is implemented by the network applications. These applications produce the data, which has to be transferred over the network. This layer also serves as a window for the application services to access the network and for displaying the received information to the user ___used protols___ SMTP HTTP


## :warning: SCP Network 

SCP is frequently used for secure file transfers, particularly when files need to be moved securely across a network between systems. System administrators and developers frequently use it to safely move files to and from remote servers.

```
scp [options] [source] [destination]
```
# :warning: reserve proxy
A server or piece of software that stands in between client devices and a web server is called a reverse proxy. Serving as the server's representative, it takes requests from clients and sends them to the intended web server. The direction of communication is the primary difference between a reverse proxy and a standard (forward) proxy.

# :warning: Forward proxy
A forward proxy, which is also commonly called a "proxy server," is a software program or server that serves as a middleman between client devices (such web browsers) and the internet. A client sends a request to the forward proxy server, which on the client's behalf passes it to the target server, in order to obtain the resource via the internet. After that, the proxy server receives the response from the destination server and forwards it to the client.

# You may ask yourself what is the key differenece between forward proxy and reverse proxy 
The key difference between a forward proxy and a reverse proxy lies in their primary functions and how they interact with clients and servers: 
Direction of Communication:

Forward Proxy: Acts on behalf of clients to access resources from the internet. It sits between client devices and the internet, forwarding requests from clients to the server and then returning the server's response to the clients.
Reverse Proxy: Acts on behalf of servers to handle requests from clients. It sits between client devices and the server, forwarding client requests to the appropriate server and returning the server's response to the clients.

Security:
Forward Proxy: Often used to enhance security by inspecting and filtering outgoing traffic. It can be employed to enforce security policies and protect clients from malicious content.
Reverse Proxy: Can provide an additional layer of security by hiding the internal server structure from external clients and handling tasks like SSL encryption, protecting backend servers from direct exposure to the internet.


# :warning: Linux file commands 
| Command | Description | 
| --- | --- | 
| mkdir | create a new directory  | 
|rm <file_name> | create a repo |
| mkdir | create a new directory  | 
|rm -r directory_name	 | 	Remove a directory recursively. |
| mkdir | create a new directory  | 
|cp source_file destination_file	 | 	Copy the contents of one file to another file using the cp command. |
| cp -r <source_directory> <destination_directory>	 | Move or rename files or directories.| 
|mv <source_file> <destination_file> | create a repo |
| touch <file_name>| Create a new file using touch. | 
|cat <file_name>	 | Show the contents of a file |
| head <file_name>	| Show the first ten lines of a file. | 
|tail <file_name>	 |Show the last ten lines of a file with the tail command |
# :warning: System Based Commands 
| Command | Description | 
| --- | --- | 
| uname | Displays system information: kernel version, machine type, and more.| 
| uname -r | Displays the running Linux kernel's release version.| 
| hostname -i | Displays the IP address of the current host.| 
| last reboot | Shows last reboot times and durations in logs.| 
| date | Displays the current date and time information.| 
| timedatectl	| Displays detailed system clock and time zone information.| 
| cal |  Displays a simple calendar of the current month.| 
| w	| Shows who is logged on and their activity.| 
| whoami | Displays the username of the current user.| 
| finger username	| Displays information about a user named 'username'.| 

# :warning: File Permission Commands

| Command | Description | 
| --- | --- | 
| chmod | Change file permissions chmod u+rwx file.txt grants read, write, and execute permissions to the owner of the file. |
| chown	| Change file ownership chown user file.txt changes the owner of “file.txt” to the specified user. |
| chgrp	| Change group ownership. chgrp group file.txt changes the group ownership of “file.txt” to the specified group. |
| umask	| umask 022 sets the default file permissions to read and write for the owner, and read-only for group and others.|
# Software development life cycle (SDLC) :
SDLC is a process followed for software building within a software organization. SDLC consists of a precise plan that describes how to develop, maintain, replace, and enhance specific software. The life cycle defines a method for improving the quality of software and the all-around development process

# :warning: Stages of the Software Development Life Cycle

SDLC specifies the task(s) to be performed at various stages by a software engineer or developer. It ensures that the end product is able to meet the customer’s expectations and fits within the overall budget. Hence, it’s vital for a software developer to have prior knowledge of this software development process. 


  ![Screenshot 2024-01-31 230751](https://github.com/Ahmedemad190/testing/assets/130619786/f1805c81-5dee-4eba-a740-42a5b60aaad9)


- Stage-1: Planning and Requirement Analysis : Planning is a crucial step in everything, just as in software development. In this same stage, requirement analysis is also performed by the developers of the organization. This is attained from customer inputs, and sales department/market surveys.

![Screenshot 2024-02-02 113031](https://github.com/Ahmedemad190/testing/assets/130619786/c49d97c4-4d8c-4e38-954e-11bac0713918)  


# :warning: Stage-2: Defining Requirements

In this stage, all the requirements for the target software are specified. These requirements get approval from customers, market analysts, and stakeholders

![aa](https://github.com/Ahmedemad190/testing/assets/130619786/3ffcfdf6-525c-4021-a1f4-1940d340907c)

# :warning: Stage-3: Designing Architecture

SRS is a reference for software designers to come up with the best architecture for the software. Hence, with the requirements defined in SRS, multiple designs for the product architecture are present in the Design Document Specification (DDS). 

![zz](https://github.com/Ahmedemad190/testing/assets/130619786/d66568b8-55a0-49a7-a65e-6ccbd54a295b)  



# :warning:  Stage-4: Developing Product

At this stage, the fundamental development of the product starts. For this, developers use a specific programming code as per the design in the DDS. Hence, it is important for the coders to follow the protocols set by the association. Conventional programming tools like compilers, interpreters, debuggers, etc. are also put into use at this stage. Some popular languages like C/C++, Python, Java, etc. are put into use as per the software regulations. 

![qq](https://github.com/Ahmedemad190/testing/assets/130619786/ede2e77c-9c0b-4b68-96c0-70e2b6c3a90a)


# :warning: Stage-5: Product Testing and Integration 

After the development of the product, testing of the software is necessary to ensure its smooth execution. Although, minimal testing is conducted at every stage of SDLC. Therefore, at this stage, all the probable flaws are tracked, fixed, and retested. This ensures that the product confronts the quality requirements of SRS. 

Documentation, Training, and Support: Software documentation is an essential part of the software development life cycle. A well-written document acts as a tool and means to information repository necessary to know about software processes, functions, and maintenance. Documentation also provides information about how to use the product. Training in an attempt to improve the current or future employee performance by increasing an employee’s ability to work through learning, usually by changing his attitude and developing his skills and understanding. 

![pp](https://github.com/Ahmedemad190/testing/assets/130619786/e38fd4ee-070c-4d91-a7a5-37157c7912f6)

 # :warning: Stage 6: Deployment and Maintenance of Products 

 After detailed testing, the conclusive product is released in phases as per the organization’s strategy. Then it is tested in a real industrial environment. It is important to ensure its smooth performance. If it performs well, the organization sends out the product as a whole. After retrieving beneficial feedback, the company releases it as it is or with auxiliary improvements to make it further helpful for the customers. However, this alone is not enough. Therefore, along with the deployment, the product’s supervision. 

 ![ee](https://github.com/Ahmedemad190/testing/assets/130619786/be561673-39e7-464c-b6d0-695bff8a9656)


 # :warning:  What is the Agile methodology?
 
Agile methodology is a project management framework that breaks projects down into several dynamic phases, commonly known as sprints. 
The Agile framework is an iterative methodology. After every sprint, teams reflect and look back to see if there was anything that could be improved so they can adjust their strategy for the next sprint.

![image](https://github.com/Ahmedemad190/testing/assets/130619786/1488c42e-ffaa-4580-8182-23289a6360be)


## What is the Agile Manifesto?

The Agile Manifesto is a document that focuses on four values and 12 principles for Agile software development. It was published in February 2001 by 17 software developers who needed an alternative to the more linear product development process.  

What are the 4 pillars of Agile?
- Individuals over processes and tools: Agile teams value team collaboration and teamwork over working independently and doing things "by the book.”
- Working software over comprehensive documentation: The software that Agile teams develop should work. Additional work, like documentation, is not as important as developing good software.
- Customer collaboration over contract negotiation: Customers are extremely important within the Agile methodology. Agile teams allow customers to guide where the software should go. Therefore, customer collaboration is more important than the finer details of contract negotiation.
- Responding to change over following a plan: One of the major benefits of Agile project management is that it allows teams to be flexible. This framework allows for teams to quickly shift strategies and workflows without derailing an entire project.


# :warning: What are the 12 Agile principles?

- Satisfy customers through early, continuous improvement and delivery. When customers receive new updates regularly, they're more likely to see the changes they want within the product. This leads to happier, more satisfied customers—and more recurring revenue.

- Welcome changing requirements, even late in the project. The Agile framework is all about adaptability. In iterative processes like Agile, being inflexible causes more harm than good.
  
- Deliver value frequently. Similar to principle #1, delivering value to your customers or stakeholders frequently makes it less likely for them to churn. 

- Break the silos of your projects. Collaboration is key in the Agile framework. The goal is for people to break out of their own individual projects and collaborate together more frequently. 

- Build projects around motivated individuals. Agile works best when teams are committed and actively working to achieve a goal. 

- The most effective way to communicate is face-to-face. If you’re working on a distributed team, spend time communicating in ways that involve face-to-face communication like Zoom calls. 

- Working software is the primary measure of progress. The most important thing that teams should strive for with the Agile framework is the product. The goal here is to prioritize functional software over everything else.

- Maintain a sustainable working pace. Some aspects of Agile can be fast-paced, but it shouldn't be so fast that team members burn out. The goal is to maintain sustainability throughout the project.

- Continuous excellence enhances agility. If the team develops excellent code in one sprint, they can continue to build off of it the next. Continually creating great work allows teams to move faster in the future. 

- Simplicity is essential. Sometimes the simplest solution is the best solution. Agile aims to not overcomplicate things and find simple answers to complex problems. 

- Self-organizing teams generate the most value. Similar to principle #5, proactive teams become valuable assets to the company as they strive to deliver value.

- Regularly reflect and adjust your way of work to boost effectiveness. Retrospective meetings are a common Agile practice. It's a dedicated time for teams to look back and reflect on their performance and adapt their behaviors for the future.


# :warning: Continuous Integration

There could be scenarios when developers in a team, work in isolation for an extended period and only merge their changes to the master branch once their work is completed. This not only makes the merging of code very difficult, prone to conflicts, and time-consuming but also results in bugs accumulating for a long time which are only identified in later stages of development. These factors make it harder to deliver updates to customers quickly. With Continuous Integration, developers frequently commit to a shared common repository using a version control system such as Git. A continuous integration pipeline can automatically run builds, store the artifacts, run unit tests, and even conduct code reviews using tools like Sonar. We can configure the CI pipeline to be triggered every time there is a commit/merge in the codebase.


# :warning: Continuous Delivery

Continuous delivery helps developers test their code in a production-similar environment, hence preventing any last-moment or post-production surprises. These tests may include UI testing, load testing, integration testing, etc. It helps developers discover and resolve bugs preemptively.
By automating the software release process, CD contributes to low-risk releases, lower costs, better software quality, improved productivity levels, and most importantly, it helps us deliver updates to customers faster and more frequently. If Continuous Delivery is implemented properly, we will always have a deployment-ready code that has passed through a standardized test process.


# :warning: Continuous Deployment
the final stage of CI and CD will be continuous deployment. It’s an extension of continuous delivery, which automate the proper code to the code repository, continuous deployment will automate the related app for production purpose because there is not having any manual gate at the stage of the pipeline before production, continuous deployment relies on high automation.

in simple language, it is a change of application that goes through the cloud which is carried by the developer and it will live within a few minutes of writing pass with the automated testing.

# :warning: Permission in Linux 
How to Check the Permission of Files in Linux

```
ls -l
```
