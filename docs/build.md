# How to build it

**Step 1: Create S3 Bucket with Name**

![2024-06-24_17h07_04](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/05eb2499-dab6-4036-b18e-5072431c1e1a)


**Step 2:  Upload the Files**

![2024-06-24_17h37_05](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/d43d3ba1-9980-4612-b422-206ba3d6baf7)


**Step 3: AWS SES follow the SS**

![2024-06-24_18h28_28](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/05e38362-f3f2-4983-bac8-a85ee72634d7)


![2024-06-24_18h29_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/62ec7b3c-703f-4904-b75d-91f8c2d5ce5a)


![2024-06-24_18h31_00](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/1336b9e3-d572-497f-b19d-5af92bbdb3b5)


**Step 4: Verify the Emails**

![2024-06-24_18h35_50](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a186683c-d4a8-429d-85bb-bc286cb00506)


![2024-06-24_18h32_42](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/247c234b-bb24-49ea-bc33-635c6b78681b)


**Step 5: Create the Identities**

![2024-06-24_18h39_35](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/84189b2f-b058-4a32-b8f8-31d66ee63869)


**Step 6: Send the Test Email**

![2024-06-24_18h42_00](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/25fafcad-b5c1-4061-9870-54c2e209c123)


![2024-06-24_18h42_59](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/b2f1d955-d66a-4e0b-b0a3-b9763c4b3816)


**Step 7: Create the Lambda Functions**

![2024-06-24_18h51_50](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/2db44d80-e22f-4af6-9b46-8f2719581803)


![2024-06-24_18h52_10](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/73612d89-1cad-4899-ba5e-d3917216f17c)


**Step 8: Paste Lambda Function Python Code from the file**

<!-- ![2024-06-24_18h54_48](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/adf3f3ab-50f1-48f0-8ff5-65a4769070f6) -->

![2024-06-24_19h43_47](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/172902eb-abd8-40c1-b95f-3287cfacac75)

See the complet code [here](../main.py).


**Step 9: Paste Lambda Function Test Event**

![2024-06-24_19h44_44](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/b4010f0f-7779-4aa1-b18c-a17c328e5db4)

```json
{
  "comment": "Generic test event for scheduled Lambda execution. The function does not use this event data.",
  "test": true
}
```


<!-- ![2024-06-24_19h46_01](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/cc47adec-6079-42b4-98eb-341101b3f78a) -->


**Step 10: Successfully tested the Event**

![2024-06-24_19h49_10](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/ed815c23-bf8a-44c1-a4b9-fd9ac31663d4)


**Step 11: Creating IAM Role & Add Policy**

![2024-06-24_19h53_54](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/4d3af022-9708-484b-9681-2b5444d91494)


![2024-06-24_19h54_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/4644a869-2f51-45f0-9b4a-029ec043d425)


![2024-06-24_19h56_39](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/656585b4-d196-441a-996e-c8d625376f87)


**Step 12: Add permissions in Policy**

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": "arn:aws:s3:::ttt-email-marketing/*"
        },
        {
            "Effect": "Allow",
            "Action": [
                "ses:SendEmail",
                "ses:SendRawEmail"
            ],
            "Resource": "*"
        }
    ]
}
```

<!-- ![2024-06-24_23h04_38](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/86a86128-0974-442a-b3e6-c08a4e9e0ca2) -->


![2024-06-24_23h04_12](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/b0d4cbb6-8ad2-4183-9f35-5d32fff80de8)


**Step 13: Finally**


![2024-06-24_23h06_34](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/7724cae3-af9a-4657-aeeb-ea63e28567fc)



![2024-06-25_00h05_02](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/dd7ce9ed-bdcc-428b-9cf2-f84ad85a3314)


**Step 14: Add Policy 7 Test the Event**

![2024-06-25_00h05_19](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/844e6283-51c9-4453-8e69-42fdaa72164a)

![2024-06-25_00h07_40](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/946e1dc3-23a3-47a4-8def-0e8fe27f60b7)


**Step 15: Email Marketing Template has Sentto the mail**

![2024-06-25_00h08_21](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/1a028a71-15c6-4a9b-8cac-7436a9b70873)


![2024-06-25_00h09_01](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/5337a64f-9ce8-40b0-810e-dfeaa9f0273e)


**Step 16: Create Eventbridge Schedule**

![2024-06-25_09h01_32](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a04b8d29-804a-4713-af1b-7c4166ed2104)


![2024-06-25_09h05_43](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/433b8c44-ff53-4854-a0d5-31df371a9163)


![2024-06-25_09h07_14](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/18864808-c276-4c1f-92e5-8a28df432f9d)


![2024-06-25_09h07_50](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/ff501b91-508e-43ff-bb21-57f672941f7c)


![2024-06-25_09h11_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a25c29fe-7749-45c0-931f-85cf4b33dd5b)


![2024-06-25_09h11_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/74316a20-9ea4-422b-af62-2b543fb91aee)


![2024-06-25_09h11_22](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a9a1aeec-2f18-485a-bb15-f54e552a31dc)


![2024-06-25_09h11_46](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/7e52549d-8103-492f-9e1e-c5a38ec2857e)


![2024-06-25_09h12_31](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/9ecdf6b6-3388-47f5-bf56-f9296735e8e1)


![2024-06-25_09h13_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/7d309cd8-4356-4a64-a695-8ccdbf0b4336)


![2024-06-25_09h13_20](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/dadddcf2-1b6a-49c4-944e-a15365800d3c)


**Step 17: Successfully sent the mail on Sheduled Time**

![2024-06-25_09h15_37](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/305d1c96-7a0f-456c-b2b6-9264c0d7692d)


![2024-06-25_09h15_59](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/4b06241a-cd3c-45d7-abee-0c01d8ae550a)


**Step 18: CloudWatch, Let's see the Logs**

![2024-06-25_09h18_25](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/aaf583a7-14ca-4626-8bae-cebdca590670)


![2024-06-25_09h19_33](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/18522f19-3bf6-4b78-a49d-a355a070b480)


![2024-06-25_09h21_06](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/6dac1ff9-34a0-434a-ad86-16dd7354dbee)
