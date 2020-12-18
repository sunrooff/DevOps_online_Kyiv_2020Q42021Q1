# Module 2 Virtualization and Cloud Basic

## TASK 2.2


1. I briefly check guidelines on AWS free tier and it's billing.
2. AWS free tier account is registered.</br></br>
![1](./screenshots/2.png)</br>


3. Hands-on tutorials. Accomplished list :</br></br>
   - Amazon Lightsail - done ✓
   - Launch and configure a WordPress instance (Lightsail) - done ✓
   - Amazon S3 bucket creation - done ✓
   - Package upload files to Amazon S3 via AWS CLI - done ✓


4. Linux VM via Amazon Lightsail service is launched :</br></br>
![1](./screenshots/4.png)</br>


5. Linux VM via EC2 service (t2 instance, CentOS) is launched :.</br></br>
![1](./screenshots/5.png)</br></br>
![1](./screenshots/5.1.png)</br>


6. Created snapshot of instance (as a backup). See AMI below :.</br></br>
![1](./screenshots/6.1.png)</br></br>

    - And of course related snapshot of AMI's volume/EBS :
    ![1](./screenshots/6.2.png)</br></br>


7. Creation of additional EBS/Volume to the main instance :</br></br>
     - EBS/Volume is created :</br></br>
     ![1](./screenshots/7.1.png)</br></br>
     - EBS is attached to the main instance :</br></br>
     ![1](./screenshots/7.2.png)</br></br>
     - Check_file.txt is stored on new volume :</br></br>
     ![1](./screenshots/7.3.png)</br></br>
     ![1](./screenshots/7.4.png)</br></br>

8-9) Launched instance from AMI and attached to this instance Disk_D :</br></br>
![1](./screenshots/8.png)</br></br>

10. WordPress instance (via Lightsail) is launched and configured :</br></br>
![1](./screenshots/10.1.png)</br></br>
![1](./screenshots/10.2.png)</br></br>


11. I created bucket in S3 and uploaded/deleted file and folder in it using guideline :</br></br>
![1](./screenshots/11.png)</br></br>

12. Uploading files to Amazon S3 using the AWS CLI:</br>
    - IAM user "AWS_admin" is created :</br></br>
    ![1](./screenshots/12.2.png)</br></br>
    - AWS CLI is configured :</br></br>
    ![1](./screenshots/12.1.png)</br></br>
    - File is uploaded to Amazon S3 via AWS CLI :</br></br>
    ![1](./screenshots/12.3.png)</br></br>

13. Only explored possibilities of creating my own domain and domain name.
14. Cluster is created Amazon Elastic Container Service (Amazon ECS) :</br></br>
![1](./screenshots/14.png)</br></br>

15. Static website on Amazon S3 :</br>
http://sunroof-index.s3-website.eu-central-1.amazonaws.com/

 * no domain was registered via Route 53 (I couldn't find free of charge way to do that)
