# Subdomain-Takeover
## Amazon S3 Bucket Subdomain Takeover
* In this Write-up I will talk about a Subdomain Takeover which I encountered at Telenor Sweedish telecommunications company.
* I used a tool named HostileSubBruteForcer to test for the vulnerability through all the sundomains of the company under this url telenor.com.
* I ran this command in the terminal line inside the tool folder (ruby sub_brute.rb --fast telenor.com).
* While scanning the subdomains the tool detected that a url named download.telenor.com is pointing to a non-existing Amazon S3 Bucket in EU West 1 Region.
 ![Screenshot 2023-05-04 17_49_03](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/f98d47aa-4fb6-4c64-811f-9e2b93022001)
 
* While visiting the amazon download.telenor.com.s3-website-eu-west-1.amazonaws.com it gave a page that looks like this:
 ![Screenshot 2023-05-10 013654](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/f4315575-5ec5-4446-9868-fdd7c9ed6d1c)
* So I took the BucketName and I Went to Amazon S3 Storage services and I created a new bucket with the same BucketName and the same Region and made it public
* Then I created a simple html file for the poc.
 
   ![image](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/13444480-7100-4c5b-8fa3-c3625a263b9d)
   
* Then i choose the bucket that i created and uploaded the html file.
* If you visited download.telenor.com you would find the message the you wrote in the html file , This of course is not the issue anymore as it is fixed.

* Tool link: https://github.com/nahamsec/HostileSubBruteforcer


