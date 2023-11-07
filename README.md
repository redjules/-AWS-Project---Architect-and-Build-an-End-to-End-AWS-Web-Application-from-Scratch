# AWS Project Architect and Build an End to End AWS Web Application from Scratch


AWS services used in this project:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/50f850f3-6de8-41a6-881f-e625a392f9cc)

Architecture:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/b57debff-6c78-4e37-83d7-13ff72d5cdda)


Final website:

![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/d15bebec-1c6f-4cd1-abd8-f94f50eb52b1)


I used Lambda to define the math function for the website:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/7c2f3299-6f0c-488c-a304-26ab6b06daec)

![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/bbe4ea3d-8f7f-437d-b526-dcc4d0968ca2)

I defined a Test event to check that the Lambda function worked:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/17893299-91e7-48e2-8817-6176338fc41f)

I used API Gateway to invoke the math functionality:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/7957c9c2-1169-4b32-b6b1-fda68611a8cd)

I created a POST Method:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/cd05e071-843b-478f-a53d-39d68d0b2285)

I enabled CORS(Cross Origin Resource Sharing) to allow the web app running in one origin or domain to be able to access resources in a different origin or domain (our web runs in one domain and amplify and lambda are running in other domains).

I copied the Invoke URL for later:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/9b25bb93-8786-49f4-a40d-64b6addb3876)

I tested the method:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/c66bbe26-34e9-41f5-84d0-c3bff4c21c21)

I used a DynamoDB to store/return the math result. I created a table:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/6d29c639-e555-4674-bb8e-8dceefcb750d)

I copied the ARN (Amazon Resource Name) for later:

![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/834002df-6d56-4452-963c-5a61fd2860d5)

I added permission to Lambda:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/82a18c1d-94ab-4db8-8c8c-326a6586a795)

I copied the JSON code from attachments to create the policy and added the ARN link to "Resource" section.
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/9721c07e-0309-4a0e-8dfa-3d03bd2c61a2)

![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/f782cd91-0425-405e-ab97-3a392af57b69)


I uploaded code in Lambda and tested:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/fbf437a6-5d4b-4fa4-a7f7-1b32fbd351f2)
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/7256b098-7be4-494d-a896-ac31e64de182)

I put in section fetch the API Gateway code in the index.html code:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/abe668ab-274e-4107-8dda-8dedf17dd51a)

I deployed the index file in Amplify:
![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/1e0a0c95-9d82-4e5c-b09d-0aaa4d386aa9)

And we got the final funcitoning website:

![image](https://github.com/redjules/-AWS-Project---Architect-and-Build-an-End-to-End-AWS-Web-Application-from-Scratch/assets/106017493/71f752fe-dd24-4cb6-8251-61a8aa103c02)
In the website, we enter our numbers, when we click the calcluate button, the script in the index.html page is calling API Gateway, that will trigger the Lambda function, which does the calculation, that gets into the DynamoDB database, and  then we get a message in return from the browser thru API Gateway.
