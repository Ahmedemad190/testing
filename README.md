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
# :warning: Linux file command 
| Command | Description | 
| --- | --- | 
| mkdir| | creat new directory|
