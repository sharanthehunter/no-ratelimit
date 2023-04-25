# no-ratelimit

vulnerability name: No rate limiting leads to Email triggering

A little bit about Rate Limit:
A rate-limiting algorithm is used to check if the user session (or IP-address) has to be limited based on the information in the session cache.
In case a client makes too many requests within a given timeframe, HTTP-Servers can respond with status code 429: Too Many Requests.

steps to reproduce :

1. Go to this URL https://partner-portal.persequor.com/register.php?

 2. Enter your email address name to create an account.

 3. Now you can check your email. login credentials will be there.

 4. We are going to reset password page https://partner-portal.persequor.com/reset-password.php

 5. Enter the Email address .

 6. click send token and intercept the request and  Now Send This Request To Intruder And Repeat It 1000 or n number of times By Fixing Any Arbitrary Payload Which Doesn't No Effect Request I Choose Accept-Language: en-US, en;q=0.5 $1$

 7. See You Will Get 302  Status Code & 1000+ ,  n number of emails In Your INBOX

 See It Is Resulting In Mass Mailing Or Email Bombing To Your Users Which Is Bad For Business Impact.




Solution -

I Will Recommend You To Add A ReCaptcha & Sort Of Something Which Requires Manual Human Interaction To Proceed Like You Can Add Captcha Like 2+2=___ so that it cannot be brute-forced and you also can have a limit at the backend for a particular number up to 5 times a day user can request verify Email or Link something like that will prevent you from someone exploiting this vulnerability
  
POC- Attached Below


![image](https://user-images.githubusercontent.com/84071887/234297747-ce4b0e9d-c36c-4283-8e65-a9e3ab47665b.png)


![image](https://user-images.githubusercontent.com/84071887/234297802-4fd17522-bf61-42a8-8e4a-0b1887d0f6c2.png)


Impact:

If You Are Using Any Email Service Software API Or Some Tool Which Costs You For Your Email This Type Of Attack Can Result from You In Financial Lose And It Can Also Slow Down Your Services It Can Take Bulk Of Storage In Sent Mail Although If Users Are Affected By This Vulnerability They Can Stop Using Your Services Which Can Lead To Business Risk.
