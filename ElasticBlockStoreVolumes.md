Elastic Block Store (EBS) Volumes

# There are three types of storage on AWS;
Block-based Storage: Instance Store and Elastic Block Store (EBS)
Object-based Storage: Simple Storage Service (S3)
File-based Storage: Elastic File System (EFS)

EBS →Persistent, durable, low-latency block-level storage volumes for EC2 instances.
S3 →Economics, pay as you go. No upfront investment, no commitment. Secure, durable, and scalable object storage infrastructure.
EFS → Simple, scalable, shared file storage service for Amazon EC2 instances. Reduce time to market. Focus on your business, not your infrastructure.
We'll focus on the EBS for this article.

# What is Volumes?

An Amazon EBS volume is a durable, block-level storage device that you can attach to your instances. After you attach a volume to an instance, you can use it as you would use a physical hard drive. EBS volumes are flexible.
You can use EBS volumes as primary storage for data that requires frequent updates, such as the system drive for an instance or storage for a database application.
You can attach multiple EBS volumes to a single instance. The volume and instance must be in the same Availability Zone.
Volumes are durable storage devices (virtual) that can be attached to EC2 instances.
They are location in which the associated machine stores its data or loads its applications.
There are two volume types in the block storage category. These are Instance Store (Ephemeral) and Elastic Block Store (EBS).

# Block-based Storage
# Instance Store and Elastic Block Store
# Instance Store 
Instance Store is located on disks that are physically attached to the host computer.
You can specify instance store for an instance only when you launch it.
 The data in an instance store persists only during the lifetime of its associated instance.
Data in the instance store is lost under these situations:
The underlying disk drive fails
The instance hibernates
The instance stops
The instance terminates

That is why we usually choose EBS.


# Elastic Block Store (EBS)
Elastic Block Store is connected to the on the network, hypervisor and accessible to each machine associated with the hypervisor.
EBS volumes are flexible.
EBS volumes persist independently from the running life of an EC2 instance.
You can attach multiple EBS volumes to a single instance. The volume and instance must be in the same Availability Zone.
You can use Multi-Attach to mount a volume to multiple instances at the same time.(Considerations and limitations)

## EC2 INSTANCE STORE VS ELASTIC BLOCK STORE
Direct connect to one instance X Connect to different instances (strong side)
Non-persistent data storage X Persistent data storage (strong side)
No replication X Replicates data in the same AZ (strong side)
Snapshots are not available X Snapshots are available (strong side)
Both SSD and HDD Backed X Both SSD and HDD Backed

# EBS Volumes
There are 6 types of volumes in 2 categories for the different use cases.

• HDD-backed volumes are used for large streaming workloads where throughput is a better performance measure than IOPS.
• SSD-backed volumes are used for frequent read/write operations where the dominant performance attribute is IOPS.