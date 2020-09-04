## Network > Release Notes

### March 24, 2020

#### Feature Updates 

##### Load Balancer

* Added Certificate management through the Cert Manager service.
* By registering a certificate at Cert Manager and connecting it to the listener, you can receive an email on certificate expiration date.

### Feb. 25, 2020

#### Feature Updates

##### Security Group

* Added "Description" entry to security group rules. You can add description for each security group rule.

### Dec. 24, 2019

#### More Features

##### DNS Plus

* Added GSLB (Global Server Load Balancing) to allow stable load balancing of traffic at an endpoint server.
* The GSLB domain can be configured either, according to routing rules, Disaster Recovery (DR), Random, or Global Load Balancing. 
* The pool serves as a grouping element for endpoint servers at the minimum unit so as to apply the routing rule. 
* Health check is conducted on a regular basis for endpoint servers included to a pool so as to support stable services. Health check is supported for HTTP/HTTPS/TCP. 

#### Feature Updates

##### DNS Plus

* Updated to select user's GSLB domain for CNAME record set type, for creating/updating the record set. 

### Dec. 17. 2019.

#### Feature Updates
* [Korea/Japan/US Region] Every network interface connected with an instance can be assosicated with each floating IP. 

### Oct. 29, 2019.

#### Feature Updates

##### Load Balancer

* Added the feature of notification via web console, for chain certificate registration, when an individual certificate which is included in the certificate file has an invalid format.

### Aug. 27, 2019 

#### Feature Updates 

##### Load Balancer

* It is available to specify TLS version to communicate with clients via TERMINATED_HTTPS load balancer.
    * For more details on the setting of load balancer in TLS version, see [user guide](https://docs.toast.com/en/Network/Load%20Balancer/en/overview/#ssltls-version-for-load-balancer).

##### DNS Plus

* Exceeded the maximum available number of record sets to be created. For each DNS zone, up to 5,000 record sets can be created. 
* Modified, in the query of record set statistics for CNAME, to query A record set type along with AAAA record set type. 

### June 25, 2019

#### Release of New Products

##### DNS Plus

* DNS Plus provides features for domain management.
* It is easy to configure a DNS server.

### May 30, 2019

#### Updates

##### Load Balancer

* [Japan Region] IP access control is available.
    * IP-based access control is available for load balancer.
    * For more details on IP access control, see user guides.

### May 28, 2019

#### Feature Updates 

##### VPC

* [Korea Region] Creating a peering can be made available again. 

### April 25, 2019

#### Feature Updates 

##### Load Balancer

* IP access control is available. 
    * IP-based access control is available at load balancer. 
    * For more details on IP access control features, see User Guide. 
    * List of IPs for control has been auto-applied to the IP acces control group named Default.  

### December 27, 2018

#### Feature Updates 

##### VPC

* Creating a new peering is not going to be provided for the time, due to concerns for packet flooding between peered VPCs. Such concerns, however, are not related to communication between previously created peering, and features are provided as usual, except peering creation.  

### November 27, 2018

#### Bug Fixes 

##### Load Balancer

* Fixed a bug occuring when a listener is added to load balancer, in which, an instance member that is newly added to a deactivate instance is created while activated.   

#### Feature Updates 

##### Load Balancer

* Added the statistics feature for load balancing, with the following statistical volume provided on a chart.
    * Session count, Session increase volume of client per second, Session increase volume of instance per second, In/Out traffic volume, Number of exceptions to load balancing
    * Statistics on deleted load balancers, listeners, or members are not provided.  
    * Traffic volume does not include L2, L3, and L4 headers. 
    * For more details, see User Guide. 


### September 20, 2018 

#### Bug Fixes 

##### Load Balancer

* Fixed an issue in which some listener members still remain afte an instance which is registered as member of load balancer is deleted.  

#### Feature Updates

##### Load Balancer

* Added dedicated load balancer services. 
* Since dedicated load balancer services are created by occupying hardware resources, 1Gbps bandwidth for 48 thousand concurrent sessions are supported.   

### August 28, 2018 

#### Bug Fixes 

##### VPC

* Fixed an issue in which deleting may be tried to VPC with subnets that have routes 

#### Feature Updates 

##### VPC

* Updated the maximum available numbers to create subnet, routing table, and route. 
* Check the maximum available numbers to create each resource of VPC from description on the right of the popup.  
    * Subnet: Available up to 10 for each VPC. 
    * Routing Table: Available up to 10 for each VPC. 
    * Route: Available up to 10 for each routing table. 

##### Load Balancer

* For TCP or HTTPS protocol, a proxy protocol can be activated to check client IP. 
* Keepalive timeout can be configured for load balancer.  


### April 24, 2018 

#### Bug Fixes 

##### VPC

* Fixed failed access to load balancer of a peer VPC from instance of a local VPC. 

##### VPC

* You can find information of attached resources on Overview of VPC, Subnet, Routing Table, and Internet Gateway. 

##### Floating IP

* Applied pagination to Floating IP list. 

##### Security Group

* Added rule editing. 

##### Load Balancer

* Changed the Keeaplive Timeout to 5 minutes. 
* Up to 60,000 session limit can be configured for listener. 

### March 22, 2018

#### Bug Fixes

##### VPC

* Fixed failure in getting an IP via DHCP when an instance is attached to a newly added subnet.
* Fixed an issue in which the same target of a previous routing policy may be entered to add a routing policy. 
* Fixed infrequently failed commuication of an instance associated to a floating IP with an instance located at a different subnet.

### February 22, 2018

#### Bug Fixes 

##### VPC

* Fixed failed traffic from an instance associated with floating IP to a local network. 

#### Feature Updates

##### Adopted VPC as Basic Model for Network 

* You can use many subnets. 
* A port can be created by the subnet and attached to an instance. 
* More routing policies can be added.
* Added the peering feature for communication between VPCs. 
* Many VPC ports may be added to or deleted from an instance.  
* For more details, Overview and User Guide of VPC.  


### November 23, 2017

#### Bug Fixes

##### Load Balancer
* Fixed the display of invalid connection limit for listener, when a load balancer is created. 

### October 26, 2017

#### Bug Fixes

##### Load Balancer
* Fixed failure in certificate registration when a load balancer is created. 

### September 21, 2017

#### More Features

##### Added Public API 

* Like Object Storage, you can also manage Compute & Network by using APIs. 
* The feature is limited at the moment, but will be extended by adding more APIs. 

#### Bug Fixes

* Fixed to disallow users without project admin authority to modify security group.
* Updated not to show the Network menu to users, except authorized admin users of a project.   

### August 24, 2017

#### Bug Fixes

##### Load Balancer
* Fixed a bug in which the session persistence of load balancer did not show properly. 

### April 20, 2017

#### Bug Fixes
##### Load Balancer
* Fixed a bug in which the popup for certificate registration is frequently missing while uploading certificate files to listener.  


### March 23, 2017

#### Bug Fixes
##### Floating IP
* Fixed failed display of the "Create" button on the popup for associating with floating IP. 


### February 23, 2017

#### Feature Updates

##### Load Balancer

* Updated to notify that deleting a listener is unavailable, if there is only one registered listener to a load balancer. 
	  * There's no defacto change in the process: sending no notification may have been confusing to some users.
	  * The updated version now allows the user to be notified clearly that it is unavailable to delete. 

##### Floating IP

* Updated to prevent a floating IP from being deleted, if it is associated with an instance or a load balancer. 
	  * Previously, deleting a floating IP which is associated with an instance or a load balancer might have caused a failure to service. 
	  * To prevent any potential error, the updated version disallows an associated floating IP to be deleted. 
* Name Changes: 'Port' -> 'Network Interface'
	  * Name for the target of floating IP to be associated with is changed from "Port" to "Network Interface". 


### January 19, 2017 

#### Bug Fixes
##### Load Balancer
* Fixed the issue in which the restricted connection setting was not applied when creating a load balancer. 



### December 22, 2016

#### Bug Fixes

##### Load Balancer
* Fixed failed editing of listener when the Health Check Protocol is TCP. 

##### Floating IP
* Fixed failed display of the name of load balancer associated with floating IP. 

##### Security Group
* Fixed an issue in which security group list disappears when a duplicate rule is added.






### December 8, 2016 

#### Bug Fixes

##### Load Balancer
* Fixed failed display of Health Check URL of load balancer. 
* Fixed the show of "/", instead of a registered Health Check URL, at the click of Edit Listener, 








### November 29, 2016

#### Bug Fixes
##### Load Balancer
* Fixed failure in creating TERMINATED_HTTPS-type load balancers.



### November 24, 2016

#### Feature Updates
##### Load Balancer
* Updated to show the value of session limit per listener of load balancer. 

#### Bug Fixes
##### Load Balancer
* Fixed failure in creating load balancers at a particular project. 

### August 4, 2016

#### Feature Updates
##### Load Balancer
* Added SSL offloading of load balancer. 

#### Bug Fixes
##### Load Balancer
* Fixed infrequent failure in closing when load balancer is removed. 
