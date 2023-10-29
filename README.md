# Subdomain-Takeover
## Amazon S3 Bucket Subdomain Takeover
* In this Write-up I will talk about a Subdomain Takeover that I encountered at Sweedish telecommunications company.
* I used a tool named HostileSubBruteForcer to test for the vulnerability through all the sundomains of the company under this url xxx.com.
* I ran this command in the terminal line inside the tool's folder (ruby sub_brute.rb --fast xxx.com).
* While scanning the subdomains the tool detected that a url named download.xxx.com is pointing to a non-existing Amazon S3 Bucket in EU West 1 Region.
 ![1](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/56c92bfe-dd8d-4a5c-a7a4-baffe89d4a0e)
 
* While visiting the amazon download.xxx.com.s3-website-eu-west-1.amazonaws.com it gave a page that looks like this:
 ![Screenshot 2023-05-10 013654](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/f4315575-5ec5-4446-9868-fdd7c9ed6d1c)
* So I took the BucketName and I Went to Amazon S3 Storage services and I created a new bucket with the same BucketName and the same Region and made it public.
* Then I created a simple html file for the poc.
 
   ![image](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/13444480-7100-4c5b-8fa3-c3625a263b9d)
   
* Then I choose the bucket that I created and uploaded the html file.
* If you visited download.xxx.com you would find the poc message , This of course is not the issue anymore as it is fixed.
* The poc message looked like this:

  ![Screen](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/b202feb2-0d46-4c6c-ae6e-f85a425dcd90)

* And by that the exploitation is done.
* Tool link: https://github.com/nahamsec/HostileSubBruteforcer


