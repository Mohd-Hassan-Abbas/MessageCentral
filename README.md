# MessageCentral

## Message Central OTP SMS Verification API
### Message Central is a CPaaS solution with OTP SMS APIs, SMS APIs, and WhatsApp marketing platform. You can reach customers across the globe and enable engaging and effective communication strategies.


### Send SMS with Lightning-Fast Delivery

Message Now is a bulk SMS service provided by Message Central. It allows businesses to send large volumes of text messages to their customers or subscribers simultaneously, enabling efficient and effective communication.

### MessageCentral Website https://www.messagecentral.com

- What are the benefits of using Message Now?
	- By using Message Now, you can reach a large audience quickly and cost-effectively. It enables personalized communication, helps increase customer 			engagement, and supports various use cases such as promotional campaigns, alerts, notifications, reminders, and more.

- Can I schedule SMS campaigns in advance?
	- Yes, Message Now offers the option to schedule messages for future delivery. This feature allows you to plan and automate your SMS campaigns, ensuring messages are 	sent at the most appropriate times for maximum impact.

- Is Message Now suitable for businesses of all sizes?
	- Yes, Message Now is designed to cater to businesses of all sizes, from small startups to large enterprises. It can be tailored to meet your specific requirements 	and scale according to your messaging needs.


### * You can integrate using language: Java, Python, C#, NodeJS, Ruby and more.
	
#### * VerifyNow : Verify Now is a user authentication service provided by Message Central, which enables businesses to verify users' phone numbers using a One-Time Password (OTP) sent via SMS.
[Verify NOW](https://www.messagecentral.com/product/verify-now/overview-india)

The usage of the API is based on several resources.

Before starting to use the API, the developer needs to know about the below specified details:

**API service endpoint**

- Base URL : https://cpaas.messagecentral.com <br>
Two endpoints are defined in One Time Password SMS API: <br>
- POST /verification/v2/verification/send : Sends an SMS with the desired message and an OTP code to the received phone number
- POST /verification/v2/verification/validateOtp : Verifies the received code as input is valid for the given authenticationId.

**Authentication**

Security access token is required for this API.

## Authentication and Authorization

Authentication is performed using an auth token. You can request an auth token by sending a request to the auth token API with your MessageCentral customer ID and key. The key is the base64 encoded password.


### Code Snippets
<span class="colour" style="color:rgb(36, 41, 47)">Snippets elaborates REST based API call with "*curl"* to request  </span>

| Snippet Request Code                               | 
| ----------------------------------------------- |
| curl --location--request POST'https://cpaas.messagecentral.com/verification/v2/verification/send?countryCode=XX&customerId=****************&flowType=SMS&mobileNumber=971X8X2X23&otpLength=4'\--header 'authToken: eyJhbGciOiJIUzUxMiJ9.eyJzdLIiOiJDLTMzNDMyQTVGNDlGNzQwNCIsImlhdCI6MTY5NjMxNDQzNiwiZXhwIjoxNjk2OTE5MjM2fQ.<br>UDSi6Mpjr5INVGm4SRFrPAFpxEanH64AD6JkiAv2zIReANR6pgmGEoo-T4AXXmgpqXjP56NYh6mFvLQzI__uaA'  |
| The response will be: <br> 200 <br>   {  <br>“responseCode”:200,<br>  “message”: “SUCCESS”,  <br>“data”:{      <br>“verificationId”: “20”,    <br>“mobileNumber”: “8846735392”,      <br>“responseCode”: “200”,      <br>“errorMessage”: null,      <br> “timeout”: “60”,      <br>“smsCLI”: null,      <br>“transactionId”: null    <br>}<br>}
<br>
| Snippet Validate code  |
| ----------------------------------------------- |
| curl --location'https://cpaas.messagecentral.com/verification/v2/verification/validateOtp?countryCode=XX&mobileNumber=971X8X2X23&verificationId=XX&customerId=************&code=XXXX'\--header 'authToken: eyJhbGciOiJIUzUxMiJ9.eyJzdLIiODMyQTVGNDlGNzQwNCIsImlhdCIMxNDQzNiwiZXhwIjoxNjk2OTE5MjM2fQ.UDSi6Mpjr<br>5INVGmpxEanH64AD6JkiAv2zIReANR6pgmGEoo-T4AXXmgpqXjP56NYh6mFvLQzI__uaA'  |
| The response will be: <br> {  <br>"responseCode": 200,  <br>"message": "SUCCESS",  <br>"data": {    <br>"verificationId":   "20",      <br>"mobileNumber":   "8846735392",<br>"verificationStatus":   "VERIFICATION_COMPLETED",      <br>"responseCode":  "200",      <br>"errorMessage":   null,      <br>"transactionId":   null,      <br>"authToken": eyJhbGciOiJIUzUxMiJ9.eyJzdLIiDMyQTVGNDlGNzQwNCIsImlhNjMxNDQzNiwiZXhwIjoxNjk2OTE5MjM2fQ.UDSi6Mpjr<br>5INVGm4SRFrP64AD6JkiAv2zIReANR6pgmGEoo-T4AXXmgpqXjP56NYh6mFvLQzI__uaA<br>}<br>}

<br>

#### * SMS Now : Message Now is a bulk SMS service provided by Message Central. It allows businesses to send large volumes of text messages to their customers or subscribers simultaneously, enabling efficient and effective communication.
[SMS NOW](https://www.messagecentral.com/product/message-now/overview-india)

#### * Whatsapp Now : WhatsApp Now is a comprehensive solution that integrates live customer support and WhatsApp marketing through WhatsApp Business APIs. It enables businesses to provide instant assistance to customers and leverage the power of WhatsApp for effective marketing campaigns.
[Whatsapp NOW](https://www.messagecentral.com/product/whatsapp-now/overview-india)

