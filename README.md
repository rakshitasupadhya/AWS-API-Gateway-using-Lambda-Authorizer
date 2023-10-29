# AWS-API-Gateway-using-Lambda-Authorizer
This is a demonstration on invoking API using Lamba Authorizer
# Architecture
<img width="565" alt="image" src="https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/d88e6cc5-61cb-4503-8164-7a86c2351d04">

# Implementation 
1. Create a Simple Lambda function to return **hello**
   <img width="703" alt="image" src="https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/1f587a78-312f-4963-80f4-7dbff93f1cf1">
   <img width="561" alt="image" src="https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/32e25704-1c32-4216-a116-4009e02b9b7f">
2. Create a Lambda function for Lambda Authorizer(update the code after creating API Gateway endpoint)
   <img width="905" alt="image" src="https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/40feb0c1-85bc-4119-97a7-451dfa4765da">
3. Create REST API Gateway
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/693d64ed-4b0c-4546-bd28-62784fea3b2c)
4. Create Resource:
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/1a332c29-0eff-4462-a4e3-a5310d2d7171)
5. Create GET Method
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/618214a3-b19f-438f-b619-2c3a8a6f4e27)
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/c4652be4-c993-4613-8e9b-add44f833060)
6. Create Authorizer
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/8b5ef2c8-c583-4401-bfcf-bc0a0ed73eec)
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/e6eb9e04-ac94-45f0-a72c-be9c1b022cf5)
7. Go to Resources option  click on GET method and select the ARN until *
   ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/0805896e-e68f-4f3b-ba44-3b9510357016)
8. Paste the ARN in Lambda created in step 2 and deploy
   <img width="743" alt="image" src="https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/e05ff264-202e-482c-9b56-1038941b1b75">
9. Go to Resources option  click on GET method and click on GET Request. Under Authorization select the authorizer created in step 6
![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/bb47451a-bd1e-4836-8da4-a07e3a25a59b)
![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/a7a5bf29-a5e5-4520-95ae-e7c09d974079)
10. Go to Resources option, click on Actions -> Deploy API
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/8417c5e6-0c53-4aee-87fa-53843813dfbc)
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/eafdd5e8-f7be-4964-b8df-785dafb4cab3)
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/4505b9b7-c588-4fbd-b0ac-950c397d13f5)
11. Click on Authorizer -> click on Test ; Verify if 200 response is received along with Allow effect
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/711b5f93-3b7f-4bca-998c-2763e19917f2)
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/1d16e1e1-5202-4f47-a3a0-74ea4df4eb8e)
12. Give wrong token code and verify if 200 response is received with deny effect
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/81815d68-154e-4899-b67c-e1f6eb4693ed)
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/848c6c05-1cab-4387-a34a-6893ca20387f)
13. Go to Resources -> Get Method -> Test -> Test button 
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/d327a45b-04f8-4daf-a6f1-bc94e2144681)
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/42c87d82-3958-48cb-923a-4b12fbda2b7e)
14. Get the API endpoint under Stages and append Resourcename given in Step 4 and paste in Postman. Click on Headers in Postman and provide the key and wrong value
    ![image](https://github.com/rakshitasupadhya/AWS-API-Gateway-using-Lambda-Authorizer/assets/107621546/b28cc4fb-0a65-4a3b-adab-62860918a6b4)
 












   










