# Cloud_Semester3_Assignment1  

### Step 1: Create an S3 Bucket  
Logining into the AWS Management Console.  
Going to the S3 service.  
Clicking on "Create bucket".  
Entering a unique bucket name and choose the region.  
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

### Step 4: Enable Static Website Hosting
Going to the Properties tab of the bucket.  
Clicking on "Static website hosting".  
Selecting "Use this bucket to host a website".  
Entering the index document (e.g., index.html).  
Clicking "Save".  

### Step 5: Create a CloudFront Distribution  
Going to the CloudFront service.  
Clicking on "Create Distribution".  
Choosing "Web" as the delivery method.  
Seting the origin domain name to the S3 bucket endpoint (e.g., BUCKET_NAME.s3.amazonaws.com).  
Configuring other settings as needed (e.g., default cache behavior).  
Clicking "Create Distribution".  

### Step 6: Update DNS  
Once the CloudFront distribution is created, noting down the domain name (e.g., xyz123.cloudfront.net).  
Updating the DNS records to point to the CloudFront distribution domain name.  

### Step 7: Test Website  
Waiting for the DNS changes to propagate.  
Visiting the website using the CloudFront domain name.  
