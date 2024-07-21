#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |


### What is AWS Route53?

**AWS Route53:** Amazon Route 53 is a scalable Domain Name System (DNS) web service designed to route end users to Internet applications by translating human-readable domain names (like www.example.com) into IP addresses (like 192.0.2.1) that computers use to identify each other on the network.

### Benefits of Route53

1. **Highly Reliable**:
   - Built on AWS’s highly available infrastructure, ensuring consistent routing to web applications via distributed DNS servers.

2. **Scalable**:
   - Automatically scales resources during high traffic and handles large queries without user intervention.

3. **Easy to Use**:
   - User-friendly interface for DNS settings configuration; DNS queries start resolving within minutes.

4. **Health Check**:
   - Monitors application health and redirects traffic to healthy resources if failures are detected.

5. **Flexible**:
   - Allows for various routing policies based on needs.

6. **Simple**:
   - Manages global traffic with different routing types.

7. **Cost-Effective**:
   - Pay only for the services used.

8. **Secure**:
   - Integrates with IAM for secure access, providing permissions to authorized users only.

9. **Integration with AWS Services**:
   - Maps domain names to Amazon EC2 instances, S3 buckets, and other AWS resources.
----
### What is a Hosted Zone in Route53?

- **Hosted Zone:** A container that holds information about how you want Amazon Route 53 to respond to DNS queries for a domain and its subdomains. It consists of a collection of resource record sets (RRsets) that Route 53 returns in response to DNS queries.

### Types of Hosted Zones

1. **Public Hosted Zone:** Manages domain names that are publicly accessible on the internet.
2. **Private Hosted Zone:** Manages domain names within an Amazon VPC (Virtual Private Cloud) and is accessible only from instances within the VPC.
----
### Lab Session - Creating a Public Hosted Zone in AWS Route53

1. **Sign in to AWS Management Console:**
   - Navigate to the Route 53 Dashboard at [AWS Management Console](https://console.aws.amazon.com/route53/).

2. **Create Hosted Zone:**
   - Click on "Create Hosted Zone."
   - Enter your domain name (e.g., example.com).
   - Choose the type (public or private).
   - Click "Create" to create the hosted zone.
----
### What are Records in a Hosted Zone?

- **Records:** Resource record sets (RRsets) within a hosted zone define how Route 53 responds to DNS queries for that domain name.

### Types of Records

1. **A Record:** Maps a domain name to an IPv4 address.
2. **AAAA Record:** Maps a domain name to an IPv6 address.
3. **CNAME Record:** Maps an alias name to another domain name.
4. **MX Record:** Specifies the mail servers responsible for accepting email on behalf of your domain.
5. **TXT Record:** Provides text information to sources outside your domain.
6. **NS Record:** Delegates a DNS namespace to a set of name servers.
----
### What is Routing Policy?

- **Routing Policy:** Specifies how Amazon Route 53 responds to DNS queries. It determines which resource records to serve based on various criteria such as geographic location, latency, or health checks.

### Types of Routing Policies

1. **Simple Routing:** Associates a single resource record set with a single endpoint.
2. **Weighted Routing:** Distributes traffic among multiple resources based on assigned weights.
3. **Latency-Based Routing:** Directs traffic based on the lowest network latency for end users.
4. **Failover Routing:** Routes traffic to a standby resource in case of primary resource failure.
5. **Geolocation Routing:** Routes traffic based on the geographic location of the end user.
6. **Multi-Value Answer Routing:** Allows Route 53 to respond to DNS queries with up to eight healthy records selected at random.
----
### Lab Session - Creating a Record in a Hosted Zone

1. **Sign in to AWS Management Console:**
   - Navigate to the Route 53 Dashboard at [AWS Management Console](https://console.aws.amazon.com/route53/).

2. **Select Hosted Zone:**
   - Choose the hosted zone where you want to create the record.

3. **Create Record:**
   - Click on "Create Record Set."
   - Enter the details for the record (name, type, value, TTL).
   - Click "Create" to create the record set.
----
### Lab Session - Creating a Private Hosted Zone in AWS Route53

1. **Sign in to AWS Management Console:**
   - Navigate to the Route 53 Dashboard at [AWS Management Console](https://console.aws.amazon.com/route53/).

2. **Create Private Hosted Zone:**
   - Click on "Create Hosted Zone."
   - Enter your domain name (e.g., example.internal).
   - Choose the type as "Private hosted zone for Amazon VPC."
   - Select the VPCs where you want the private hosted zone to be accessible.
   - Click "Create" to create the private hosted zone.
----
### Lab Session - Configuring Query Logging for a Hosted Zone

1. **Sign in to AWS Management Console:**
   - Navigate to the Route 53 Dashboard at [AWS Management Console](https://console.aws.amazon.com/route53/).

2. **Select Hosted Zone:**
   - Choose the hosted zone for which you want to enable query logging.

3. **Configure Query Logging:**
   - Click on "Create Query Logging Config."
   - Configure the logging details (log group, IAM role).
   - Click "Create" to enable query logging.
----
### Lab Session - Deletion of a Hosted Zone

1. **Sign in to AWS Management Console:**
   - Navigate to the Route 53 Dashboard at [AWS Management Console](https://console.aws.amazon.com/route53/).

2. **Select Hosted Zone:**
   - Choose the hosted zone you want to delete.

3. **Delete Hosted Zone:**
   - Click on "Delete Hosted Zone."
   - Follow the confirmation prompts to delete the hosted zone.
