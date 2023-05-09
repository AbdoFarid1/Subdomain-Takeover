# Subdomain-Takeover
## Amazon S3 Bucket Subdomain Takeover
* In this Writeup i will talk about a Subdomain Takeover which I encountered at Telenor Sweedish telecommunications company.
* I used a tool named HostileSubBruteForcer to test for the vulnerability through all the sundomains of the company under this url telenor.com.
* I ran this command in terminal ruby (sub_brute.rb --fast telenor.com)
* While scanning the subdomains the tool detected that a url named download.telenor.com is pointing to a non-existing Amazon S3 Storage in EU West 1 Region.
 ![Screenshot 2023-05-04 17_49_03](https://github.com/AbdoFarid1/Subdomain-Takeover/assets/128148536/f98d47aa-4fb6-4c64-811f-9e2b93022001)

