# Hosting-Website-using-Amazon-S3-and-accelerate-content-delivery-using-Cloudfont-in-AWS

# 🌐 Static Website Hosting with Amazon S3 & CloudFront

> Scalable, secure, and globally optimized static website deployment using Amazon Web Services (AWS).

---

## 📌 Project Overview

This project demonstrates how to host a fully functional static website using **Amazon S3** and accelerate content delivery globally using **Amazon CloudFront**. The setup ensures high availability, low latency, secure access (HTTPS via ACM), and is ideal for portfolio sites, landing pages, blogs, and documentation platforms.

---

## 🛠️ AWS Services Used

| Service                | Purpose                                                                 |
|------------------------|-------------------------------------------------------------------------|
| **Amazon S3**          | Stores and serves static files (HTML, CSS, JS, media)                   |
| **Amazon CloudFront**  | Delivers content globally with low latency and high transfer speed      |
| **AWS Certificate Manager (ACM)** | Provides SSL/TLS certificates for enabling HTTPS            |
| **CloudWatch (optional)** | Monitoring and logging performance metrics                          |

---

## 🏗️ Architecture Diagram

> ![Architecture Diagram Placeholder](#)
> *Insert architecture diagram here showing S3 → CloudFront → Browser*

---

## 🚀 Implementation Steps

### 1. Create and Configure S3 Bucket
- Create an S3 bucket (preferably named after your domain)
- Enable static website hosting
- Upload website files (`index.html`, etc.)
- Configure bucket policies or use **Origin Access Identity (OAI)**

### 2. Configure Bucket Permissions
- Adjust block public access settings
- Use bucket policy or OAI to secure access via CloudFront

### 3. Set Up CloudFront Distribution
- Set S3 as the origin
- Enable caching, compression, geo-restrictions (optional)
- Set default root object to `index.html`

### 4. Attach SSL Certificate
- Request certificate via **ACM**
- Attach to CloudFront for HTTPS support

### 5. Test and Validate
- Access the website via CloudFront URL or custom domain
- Check HTTPS, performance, and rendering

### 6. Monitor and Optimize
- Enable **CloudWatch** & **CloudFront logs**
- Use invalidations to refresh cache

---

## 🔒 Security Configuration

### S3:
- **Block Public Access** unless using CloudFront OAI
- Enable **Versioning** to protect content integrity

### CloudFront:
- Enforce **HTTPS** using viewer policy
- Use **Signed URLs/Cookies** for private content
- Enable **Geo-restrictions** where necessary

---

---

## 🧪 Results

- Website loads securely and efficiently across geographies
- HTTPS ensures user trust and SEO benefit
- Cache invalidation enables fast updates
- Resilient and scalable solution with zero server management

---

## ⚠️ Challenges Faced

- 🔐 Configuring secure bucket policies with CloudFront OAI
- ⏳ CloudFront propagation delays (up to 30 mins for updates)
- 🔄 Cache invalidation required post-deployment changes

---

## 📚 References

- [Amazon S3 Documentation](https://docs.aws.amazon.com/s3/index.html)  
- [Static Website Hosting with Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)  
- [CloudFront Documentation](https://docs.aws.amazon.com/cloudfront/index.html)  
- [Using CloudFront with S3](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigin.html)

---

## 👨‍💻 Authors

- **M. Mani Prasoon** — 22881A05N8  
- **D. Sai Praneeth** — 22881A05M1  
- **M. Hari Vardhan** — 22881A05P1  

Supervised by:  
**Dr. Ravula Arun Kumar**  
Assistant Professor, Dept. of CSE  
Vardhaman College of Engineering, Hyderabad

---

## 📜 License

MIT License — free for use with attribution.

---

**“Fast. Secure. Global. Cloud-Native Web Hosting with AWS.”**
