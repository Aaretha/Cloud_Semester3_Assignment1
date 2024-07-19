# Cloud_Semester3_Assignment1  

### Step 1: Create an S3 Bucket  
Logining into the AWS Management Console.  
Going to the S3 service.  
Clicking on "Create bucket".  
Entering a bucket name.  
Unclicking the option to block public access.  
Keeping the default settings and click "Create bucket".  

### Step 2: Upload Website Files to the S3 Bucket
Opening the newly created bucket.  
Clicking on the "Upload" button.  
Selecting the files to upload.  
Once uploaded, selecting the files and click on "Actions" > "Make Public".  

### Step 3: Configure Bucket Policy  
Going to the Permissions tab of the bucket.  
Clicking on "Bucket Policy".  
Adding a policy allowing public read access to the bucket  
```
{  
    "Version": "2008-10-17",    
    "Statement": [  
        {  
            "Sid": "PublicReadGetObject",  
            "Effect": "Allow",  
            "Principal": {  
                "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity EEXY7NC7B7HD6"  
            },  
            "Action": "s3:GetObject",  
            "Resource": "arn:aws:s3:::semester3assignment1/*"  
        }  
    ]  
}
```

### Step 4: Enable Static Website Hosting
Going to the Properties tab of the bucket.  
Clicking on "Static website hosting".  
Selecting "Use this bucket to host a website".  
Entering the index document (index.html).  
Clicking "Save".  

### Step 5: Create a CloudFront Distribution  
Going to the CloudFront service.  
Clicking on "Create Distribution".  
Choosing "Web" as the delivery method.  
Seting the origin domain name to the S3 bucket endpoint.  
Clicking "Create Distribution".   

### Step 6: Test Website  
Once the CloudFront distribution is created, noting down the domain name (https://d3s9yjf8ptg012.cloudfront.net).  
Visiting the website using the CloudFront domain name/index.html
