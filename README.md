SETTING UP S3 BUCKET WITH STATIC WEBSITE ENABLED

1. Type s3 on the AWS search bar
2. click create bucket
![CREATE_S3_BUCKET.png](docs/CREATE_S3_BUCKET.png)

3. choose bucket type
4. Bucket name - specify your Bucket name or choose bucket if you have an existing bucket
5. uncheck "Block all public access"
![ENABLE_PUBLICACCESS_STATICWEBSITE.png](docs/ENABLE_PUBLICACCESS_STATICWEBSITE.png)

6. check "I acknowledge that the current settings might result in this bucket and the objects within becoming public."
7. leave all other settings to default and click create bucket
8. click properties after bucket is successfully created, scroll down to static website hosting, click edit button on static website hosting and enable 
![CREATES3_STATIC_WEBSITEHOSTING.png](docs/CREATES3_STATIC_WEBSITEHOSTING.png)

9. leave hosting type @ "Host a static website"
10.type "index.html" on the Index document slot and "error.html" on the Error document slot and save changes
11.Go back to your bucket and click Upload
![UPLOAD_OBJECT.png](docs/UPLOAD_OBJECT.png)

12.click Add files to and select the html files of your website and upload
13.click add folder and select the image folder of your website and upload
14.Upload
15.close
16.Go to bucket and click permission
17.edit Bucket policy
18.create Bucket policy
![CREATE_BUCKET_POLICY.png](docs/CREATE_BUCKET_POLICY.png)

19.Go to properties,copy "Bucket website endpoint"
20.open new browser tab and paste your "Bucket website endpoint" to verify your configuration can be publicly viewed
![STATIC-PUBLIC-ACCESS-SUCCESS.png](docs/STATIC-PUBLIC-ACCESS-SUCCESS.png)

SET UP CLOUDFRONT FOR S3 BUCKET
1. Type CloudFront on the AWS search bar
2. click "create distribution"
3. create Distribution name 
![CREATE_CLOUDFRONT.png](docs/CREATE_CLOUDFRONT.png)

4. choose Distribution type
5. click Next
6. Specify Origin "choose origin type"
7. Origin:s3 origin: click browse origin
8. choose your created bucket
9. click "Use Website Endpoint" If you plan to use this distribution as a website
10.Enable Security: Select "Enable Security Protection"
![ENABLE_WAF_SECURITY.png](docs/ENABLE_WAF_SECURITY.png)

11.click next
12.Review and Create
13.create Distribution
14.copy distribution domain name and paste in paste in browser to test configuration
