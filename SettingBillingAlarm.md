
Setting an AWS Billing Alarm to monitor your estimated AWS charges

# Setting an AWS Billing Alarm to monitor your estimated AWS charges

Although we use a free account, there are some limitations to the free policy due to the free tier features. Therefore, setting up a billing alarm will allow us to be aware of any unintended charges.

## Enabling billing alerts

1. Enter AWS Console as a root user. 
2. Write **'Billing'** on the search bar. 
3. On the left hand side you will see **Billing Preferences** under **Preferences**. Choose **Billing Preferences**.

 3.1 Choose **Receive PDF Invoice By Email** box . So you will receive the usage in pdf format as an e-mail.
 3.2 Choose **Receive Free Tier Usage Alerts** box. Turn on this feature to receive email alerts when your AWS service usage is approaching, or has exceeded, the AWS Free Tier usage limits. If you wish to receive these alerts at an email address that is not the primary email address associated with this account, please specify the email address below.
 3.3 In the Email Address section, your e-mail address will appear, this is the e-mail address we used when registering. You can edit this and use another e-mail address for alarms.
 3.4 Choose **Receive Billing Alerts** box. Turn on this feature to monitor your AWS usage charges and recurring fees automatically, making it easier to track and manage your spending on AWS. You can set up billing alerts to receive email notifications when your charges reach a specified threshold.
 3.5 Choose **Save Preferences**. At the top centre of the screen you will see the **'Preferences saved'** pop-up.

---

## Creating a billing alarm

We can access this section both from Cloudwatch Service or from the page where we set billing alarm by clicking Manage Billing Access.
On the left hand side menu; Choose CloudWatch →Alarms →Billing
>**Important: If necessary, change the Region to US East (N. Virginia). Billing metric data is stored in this Region and represents worldwide charges.**
1. In the navigation pane, choose **Create Alarm**
2. **Specify metric** and conditions:
In the Conditions section, we write Static more than **5$**. 

3. **Configure Actions:** In this section we will choose what to do when it is greater than 5$.
  3.1 Alarm state trigger: Choose **In Alarm**
 >**Note:** It is enough to receive notification only in case of In alarm.
  3.2 Select an SNS Topic: **Create a new topic**
  3.3 Name: write a name(like BillingTopic)
  3.4 Email end points that will receive the notification: Write here your mail adres
  3.5 **Create Topic**
Than we will see Billing Topic under Topics in the SNS service.

Go to your mailbox and confirm the mail address in the received mail.
1. Add Name and description: Let's make naming and explanation in this section
2. Preview and create: Choose **Create alarm** button.

 Now we have an alarm.


