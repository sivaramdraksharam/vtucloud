# Amazon Simple Storage Service (S3) Student Handout

## Introduction to Amazon S3

Amazon S3 (Simple Storage Service) is a cloud-based storage service provided by Amazon Web Services (AWS). It allows you to store and retrieve any amount of data, at any time, from anywhere on the web.

---

## Key Concepts in S3

### Buckets
- **Definition**: A bucket is a container for storing data in S3.
- **Example 1**: A bucket named `company-backups` for storing database backups.
- **Example 2**: A bucket named `website-assets` for storing images and videos for a website.
- **Example 3**: A bucket named `user-uploads` for storing files uploaded by users of an application.

### Objects
- **Definition**: An object is the actual data stored in S3, such as a file, image, or video.
- **Example 1**: A PDF document stored as an object in the `company-backups` bucket.
- **Example 2**: A JPEG image stored as an object in the `website-assets` bucket.
- **Example 3**: A CSV file stored as an object in the `user-uploads` bucket.

### Keys
- **Definition**: A key is the unique identifier for an object within a bucket.
- **Example 1**: The key `backup-2023-01-01.sql` for a database backup file.
- **Example 2**: The key `logo.png` for a company logo image.
- **Example 3**: The key `user123/profile.jpg` for a user's profile picture.

---

## S3 Storage Classes

### S3 Standard
- **Use Case**: Frequently accessed data.
- **Example 1**: Storing website images that are accessed daily.
- **Example 2**: Storing application logs that are frequently analyzed.
- **Example 3**: Storing user-generated content that is accessed often.

### S3 Intelligent-Tiering
- **Use Case**: Data with unpredictable access patterns.
- **Example 1**: Storing seasonal sales data that is accessed sporadically.
- **Example 2**: Storing archived emails that may be accessed occasionally.
- **Example 3**: Storing research data with varying access frequency.

### S3 Glacier
- **Use Case**: Long-term data archiving.
- **Example 1**: Storing compliance documents that need to be retained for years.
- **Example 2**: Storing historical financial records.
- **Example 3**: Storing old project files that are rarely accessed.

---

## Creating and Configuring S3 Buckets

### Bucket Naming Conventions
- **Requirement**: Must be globally unique across all AWS accounts.
- **Example 1**: `my-first-s3-bucket`
- **Example 2**: `project-archive-2023`
- **Example 3**: `user-data-storage`

### Region Selection
- **Consideration**: Choose a region closest to your users to reduce latency.
- **Example 1**: Selecting the `us-east-1` region for users in the eastern United States.
- **Example 2**: Selecting the `eu-west-1` region for users in Europe.
- **Example 3**: Selecting the `ap-south-1` region for users in India.

---

## Uploading, Downloading, and Managing Objects

### Methods
- **S3 Console**: Web-based interface for uploading and managing objects.
- **AWS CLI**: Command Line Interface for interacting with S3.
- **SDKs**: Software Development Kits for programming languages like Python, Java, and Node.js.

### Example Operations
- **Example 1**: Uploading a file using the S3 Console.
- **Example 2**: Downloading a file using the AWS CLI.
- **Example 3**: Managing object permissions using the S3 Console.

---

## Understanding S3 Pricing

### Cost Factors
- **Storage**: Cost based on the amount of data stored.
- **Requests**: Cost based on the number of requests made to S3.
- **Data Transfer**: Cost for transferring data out of S3.

### Example Costs
- **Example 1**: Storing 100 GB of data in S3 Standard.
- **Example 2**: Making 10,000 GET requests to retrieve objects.
- **Example 3**: Transferring 50 GB of data out of S3 to a local machine.

---

## Hands-On Exercise

### Creating an S3 Bucket and Uploading/Downloading Files

1. **Create a Bucket**
   - Go to the S3 console.
   - Click "Create Bucket."
   - Enter a unique bucket name (e.g., `my-first-s3-bucket`).
   - Choose a region (e.g., Mumbai).
   - Click "Create."

2. **Upload a File**
   - Select your newly created bucket.
   - Click "Upload."
   - Drag and drop a file from your computer.
   - Click "Upload."

3. **Download the File**
   - Select the file you just uploaded.
   - Click "Download."

---

## Conclusion

Amazon S3 is a scalable, durable, and cost-effective cloud storage service. By understanding key concepts like buckets, objects, and keys, and choosing the right storage class, you can optimize your storage costs and ensure your data is secure.
