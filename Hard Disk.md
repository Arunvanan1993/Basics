# hard Disk type

What is Magnetic Drive?

Rotating magnetic drives, your cheapest solution in terms of large storage space.

What Is an HDD?

1. An HDD is a data storage device that lives inside the computer. It has spinning disks inside where data is stored magnetically. The HDD has an arm with several "heads" (transducers) that read and write data on the disk. 
2. HDDs are considered a legacy technology, meaning they’ve been around longer than SSDs. In general, they are lower in cost and are practical for data that does not need to be accessed frequently, such as backups of photos, videos or business files. They are available in two common form factors: 2.5 inch (commonly used in laptops) and 3.5 inch (desktop computers)

What Is an SSD?
1. SSDs got their name—solid state—because they use solidstate devices under the hood. In an SSD, all data is stored in integrated circuits. 
2. This difference from HDDs has a lot of implications, especially in size and performance. Without the need for a spinning disk, SSDs can reduce to the shape and size of a stick of gum (what’s known as the M.2 form factor) or even as small as a postage stamp.
3. Their capacity—or how much data they can hold—varies, making them flexible for smaller devices, such as slim laptops, convertibles, or 2 in 1s. And SSDs dramatically reduce access time since users don’t have to wait for platter rotation to start up.
4. SSDs are more expensive than HDDs per amount of storage (in gigabytes (GB) and terabytes (TB)), but the gap is closing as SSD prices decline at a faster pace that HDD prices year over year.


Type of SSDs.

1. SATA SSD

SATA SSDs are the first generation of SSDs. They can reach a read speed of up to 570MB per second. These first-generation SSDs are generally 5 times faster than a traditional HDD. The most common SATA variant in laptops is a 2.5-inch SSD. These SSDs start your laptop within 15 seconds and load large games within mere moments.

2. NVMe SSD

NVMe is a protocol that allows you to reach even higher speeds than with a SATA SSD. This means an NVMe SSD can reach a read speed of 2600MB per second. That's almost 5 times as fast as a SATA drive! Do you use large zip files a lot? If so, we recommend a laptop with NVMe M.2.


Similarities between HDD and SDD:

1. Both are used to store data.
2. Both are used to boot the system.
3. Both are I/O devices.
4. Differences between HDD and SDD :

<img width="955" alt="image" src="https://user-images.githubusercontent.com/93850355/174438376-de20592d-26d8-4d85-853b-1dd2c35e2bf6.png">

Amazon EBS volume types : 

Amazon EBS provides multiple volume types that allow you to optimize storage performance and cost for a broad range of applications. 
These volume types are divided into two major categories: SSD-backed storage for transactional workloads, such as databases, virtual desktops and boot volumes, and HDD-backed storage for throughput intensive workloads, such as MapReduce and log processing.

SSD-based volumes include the highest performance EBS volumes (io2 and io1) for your most demanding transactional applications including SAP HANA, Microsoft SQL Server and IBM DB2, and General Purpose SSD volumes (gp3 and gp2) that balance price and performance for transactional applications, including virtual desktops, test and development environments, and interactive gaming applications. 

HDD-based volumes include Throughput Optimized HDD (st1) for frequently accessed, throughput intensive workloads and the lowest cost Cold HDD (sc1) for less frequently accessed data.

The following tables show use cases and performance characteristics of each EBS volume:

SSD-based volumes

io2 : 

io2 is a new generation of the Provisioned IOPS SSD volumes that is designed to provide 100X durability of 99.999% as well as a 10X higher IOPS to storage ratio of 500 IOPS for every provisioned GB –at the same price as the previous generation (io1). io2 is a high performance EBS storage option designed for business-critical, I/O intensive database applications, such as SAP HANA, Oracle, Microsoft SQL Server, and IBM DB2 that have high durability requirements.

io2 is designed to deliver a consistent baseline performance of up to 500 IOPS/GB to a maximum of 64,000 IOPS. io2 volumes also provide up to 1,000 MB/s of throughput per volume. To maximize the benefit of io2, we recommend using EBS-optimized EC2 instances. When attached to EBS-optimized EC2 instances, io2 is designed to achieve single-digit millisecond latencies and is designed to deliver the provisioned performance 99.9% of the time. For more information about instance types that can be launched as EBS-optimized instances, see Amazon EC2 Instance Types. For more information about Amazon EBS performance guidelines, see Increasing EBS Performance.

To achieve the limit of 64,000 IOPS and 1,000 MB/s throughput, the volume must be attached to an EC2 instance built on the AWS Nitro System.

Volume Type: EBS Provisioned IOPS SSD (io2)
Short Description: High performance SSD volume designed for business-critical latency-sensitive applications
Use Cases: I/O-intensive NoSQL & relational databases
API Name: io2
Volume Size: 4 GB – 16 TB
Durability: 99.999%
Max IOPS*/Volume: 64,000
Max Throughput**/Volume: 1,000 MB/s
Max IOPS/Instance: 160,000
Max IOPS/GB: 500 IOPS/GB
Max Throughput/Instance: 4,750 MB/s
Latency: single digit millisecond
Price:
$0.125/GB-month
$0.065/provisioned IOPS-month up to 32,000 IOPS
$0.046/provisioned IOPS-month from 32,001 to 64,000 IOPS
Dominant Performance Attribute: IOPS and volume durability

*io1/io2/gp2 based on 16K I/O size, st1/sc1 based on 1 MB I/O size
**volume throughput is calculated as MB = 1024^2 bytes

io2 Block Express : 

io2 Block Express offers the highest performance block storage in the cloud with 4x higher throughput, IOPS, and capacity than io2 volumes, along with sub-millisecond latency. Block Express is the latest generation of Amazon EBS storage server architecture purpose-built to meet the performance and latency requirements of the most demanding applications. io2 Block Express is designed to provide 4,000 MB/s throughput per volume, 256,000 IOPS/volume, up to 64 TiB storage capacity, and 1,000 IOPS/GB as well as 99.999% durability making it ideal for your largest, most I/O intensive, mission-critical deployments of Oracle, SAP HANA, Microsoft SQL Server, and SAS Analytics.

io2 Block Express is available with X2idn, X2iedn, R5b, and C7g instances, with support for other EC2 instances coming soon. All io2 volumes attached to X2idn, X2iedn, R5b, and C7g instances are on io2 Block Express.
Volume Type: EBS Provisioned IOPS SSD (io2 Block Express)
Short Description: High performance SSD volume designed for business-critical latency-sensitive applications
Use Cases: I/O-intensive NoSQL & relational databases
API Name: io2
Volume Size: 4 GB – 64 TB
Durability: 99.999%
Latency: sub-millisecond
Max IOPS/Volume: 256,000
Max Throughput*/Volume: 4,000 MB/s
Max IOPS/Instance: 260,000
Max IOPS/GB: 1,000 IOPS/GB
Max Throughput/Instance: 7,500 MB/s
Price: 
$0.125/GB-month
$0.065/provisioned IOPS-month up to 32,000 IOPS
$0.046/provisioned IOPS-month from 32,001 to 64,000 IOPS
$0.032/provisioned IOPS-month for greater than 64,000 IOPS
Dominant Performance Attribute: IOPS, throughput, latency, capacity, and volume durability

*volume throughput is calculated as MB = 1024^2 bytes

io1 : 

io1 is backed by solid-state drives (SSDs) and is a high performance EBS storage option designed for critical, I/O intensive database and application workloads, as well as throughput-intensive database and data warehouse workloads, such as HBase, Vertica, and Cassandra. These volumes are ideal for both IOPS-intensive and throughput-intensive workloads that require low latency and have moderate durability requirements or include built-in application redundancy.

io1 is designed to deliver a consistent baseline performance of up to 50 IOPS/GB to a maximum of 64,000 IOPS and provide up to 1,000 MB/s of throughput per volume. To maximize the benefit of io1, we recommend using EBS-optimized EC2 instances. When attached to EBS-optimized EC2 instances, io1 is designed to achieve single-digit millisecond latencies and is designed to deliver the provisioned performance 99.9% of the time. For more information about instance types that can be launched as EBS-optimized instances, see Amazon EC2 Instance Types. For more information about Amazon EBS performance guidelines, see Increasing EBS Performance.

To achieve the limit of 64,000 IOPS and 1,000 MB/s throughput, the volume must be attached to an EC2 instance built on the AWS Nitro System.

Volume Type: EBS Provisioned IOPS SSD (io1)

Short Description: High performance SSD volume designed for latency-sensitive transactional workloads
Use Cases: I/O-intensive NoSQL & relational databases
API Name: io1
Volume Size: 4 GB – 16 TB
Durability: 99.8% - 99.9%
Max IOPS*/Volume: 64,000
Max Throughput**/Volume: 1,000 MB/s
Max IOPS/Instance: 260,000
Max IOPS/GB: 50 IOPS/GB
Max Throughput/Instance: 7,500 MB/s
Latency: single digit millisecond
Price: $0.125/GB-month + $0.065/provisioned IOPS-month
Dominant Performance Attribute: IOPS
*io1/io2/gp2 based on 16K I/O size, st1/sc1 based on 1 MB I/O size
**volume throughput is calculated as MB = 1024^2 bytes

gp3 : 

Amazon gp3 volumes are the latest generation of general-purpose SSD-based EBS volumes that enable customers to provision performance independent of storage capacity, while providing up to 20% lower pricing per GB than existing gp2 volumes. The new gp3 volumes deliver a baseline performance of 3,000 IOPS and 125 MiBps at any volume size. Customers looking for higher performance can scale up to 16,000 IOPS and 1,000 MiBps for an additional fee. gp3 volumes are designed to offer single-digit millisecond latency while delivering the provisioned performance 99% of the time, making them ideal for a wide variety of applications that require high performance at low cost, including virtual desktops, medium sized single instance databases such as Microsoft SQL Server, Cassandra, MySQL, and Oracle DB, Hadoop analytics clusters, low-latency interactive apps, dev & test, and boot volumes. If you need a greater number of IOPS than gp3 can provide, we recommend that you use io2 volumes. To maximize the performance of gp3, we recommend using EBS-optimized EC2 instances.

Volume Type: EBS General Purpose SSD (gp3)
Short Description: General Purpose SSD volume that balances price performance for a wide variety of transactional workloads
Use Cases: virtual desktops, medium sized single instance databases such as MSFT SQL Server and Oracle DB, low-latency interactive apps, dev & test, boot volumes
API Name: gp3
Volume Size: 1 GB – 16 TB
Durability: 99.8% - 99.9% durability
Max IOPS/Volume: 16,000
Max Throughput***/Volume: 1000 MB/s
Max IOPS/Instance: 260,000
Max Throughput/Instance: 7,500 MB/s
Latency: single digit millisecond
Storage Price: $0.08/GB-month
Provisioned Performance Price: 3,000 IOPS free and $0.005/provisioned IOPS-month over 3,000 IOPS; 125 MB/s free and $0.04/provisioned MB/s-month over 125 MiBps
Dominant Performance Attribute: $/IOPS

gp2 : 

gp2 is the default EBS volume type for Amazon EC2 instances. These volumes are backed by solid-state drives (SSDs) and are suitable for a broad range of transactional workloads, including dev/test environments, low-latency interactive applications, and boot volumes. gp2 is designed to offer single-digit millisecond latency, deliver a consistent baseline performance of 3 IOPS/GB (minimum 100 IOPS) to a maximum of 16,000 IOPS, and provide up to 250 MB/s of throughput per volume. gp2 volumes smaller than 1 TB can also burst up to 3,000 IOPS. I/O operations are included in the price of gp2, so you only pay for each GB of storage you provision. gp2 is designed to deliver the provisioned performance 99% of the time. If you need a greater number of IOPS than gp2 can provide, such as a workload where low latency is critical or you need better performance consistency, we recommend using io1. To maximize the performance of gp2, we recommend using EBS-optimized EC2 instances.

Volume Type: EBS General Purpose SSD (gp2) *
Short Description: General Purpose SSD volume that balances price performance for a wide variety of transactional workloads
Use Cases: Boot volumes, low-latency interactive apps, dev & test
API Name: gp2
Volume Size: 1 GB – 16 TB
Durability: 99.8% - 99.9% durability
Max IOPS**/Volume: 16,000
Max Throughput***/Volume: 250 MB/s
Max IOPS/Instance: 260,000
Max Throughput/Instance: 7,500 MB/s
Latency: single digit millisecond
Price: $0.10/GB-month
Dominant Performance Attribute: IOPS
*Default volume type
**io1/io2/gp2 based on 16K I/O size, st1/sc1 based on 1 MB I/O size
***volume throughput is calculated as MB = 1024^2 bytes


HDD-based volumes : 

st1 : 

st1 is backed by hard disk drives (HDDs) and is ideal for frequently accessed, throughput-intensive workloads with large datasets and large I/O sizes, such as MapReduce, Kafka, log processing, data warehouse, and ETL workloads. These volumes deliver performance, measured in MB/s of throughput, and include the ability to burst up to 250 MB/s per TB, with a baseline throughput of 40 MB/s per TB and a maximum throughput of 500 MB/s per volume. st1 is designed to deliver the expected throughput performance 99% of the time and has enough I/O credits* to support a full-volume scan at the burst rate. To maximize the performance of st1, we recommend using EBS-optimized EC2 instances.

Volume Type: Throughput Optimized HDD (st1)
Short Description: Low cost HDD volume designed for frequently accessed, throughput-intensive workloads
Use Cases: Big data, data warehouses, log processing
API Name: st1
Volume Size: 125 GB – 16 TB
Durability: 99.8% - 99.9% durability
Max IOPS**/Volume: 500
Max Throughput***/Volume: 500 MB/s
Max IOPS/Instance: 260,000
Max Throughput/Instance: 7,500 MB/s
Price: $0.045/GB-month
Dominant Performance Attribute: MB/s
* I/O credits are used to burst large amounts of I/O above baseline performance
**io1/gp2 based on 16K I/O size, st1/sc1 based on 1 MB I/O size
***volume throughput is calculated as MB = 1024^2 bytes

sc1 : 

sc1 is backed by hard disk drives (HDDs) and provides the lowest cost per GB of all EBS volume types. It is ideal for less frequently accessed workloads with large, cold datasets. Similar to st1, sc1 provides a burst model. These volumes can burst up to 80 MB/s per TB, with a baseline throughput of 12 MB/s per TB and a maximum throughput of 250 MB/s per volume. For infrequently accessed data, sc1 provides extremely inexpensive storage. sc1 is designed to deliver the expected throughput performance 99% of the time and has enough I/O credits* to support a full-volume scan at the burst rate. To maximize the performance of sc1, we recommend using EBS-optimized EC2 instances.

Volume Type: Cold HDD (sc1)
Short Description: Lowest cost HDD volume designed for less frequently accessed workloads
Use Cases: Colder data requiring fewer scans per day
API Name: sc1
Volume Size: 125 GB – 16 TB
Durability: 99.8% - 99.9% durability
Max IOPS**/Volume: 250
Max Throughput***/Volume: 250 MB/s
Max IOPS/Instance: 260,000
Max Throughput/Instance: 7,500 MB/s
Price: $0.015/GB-month
Dominant Performance Attribute: MB/s
* I/O credits are used to burst large amounts of I/O above baseline performance
**io1/gp2 based on 16K I/O size, st1/sc1 based on 1 MB I/O size
***volume throughput is calculated as MB = 1024^2 bytes


Below Link for Reference 

***https://aws.amazon.com/ebs/volume-types/ ***
