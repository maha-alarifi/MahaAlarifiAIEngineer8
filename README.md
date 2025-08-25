In this challenge I analyzed a dataset of users logs and tring to predict the users who more likely to stop using the application/website of a music 
to understand the dataset I first tryed to understand the relation between the columns 
I took as a use case userID = 39 and the relation between the features ('level', 'sessionId', 'itemInSession') 
<img width="2332" height="978" alt="image" src="https://github.com/user-attachments/assets/0e6a33a1-42cd-4ef9-8e3f-f15752462fd7" />

As conclusion, customers can have either Pain or Free plan per session, and within same session there are mutiable items, these items can be the interaction the user ia having with this application (home page, help page, next music, ... etc) 

<img width="2268" height="876" alt="image" src="https://github.com/user-attachments/assets/51520888-2a55-4cbf-a2a1-a660c8e57074" />

I tried to catch the period of the subscription plan, it looks like its "daily" subscription by looking at this chart from our user use-case 
<img width="2280" height="944" alt="image" src="https://github.com/user-attachments/assets/e1a52a82-7b02-4d4d-876e-013c34ef65e2" />

Then I went and tried to make a decision of which features and actually usefull, I tested the "status" feature to understand its message, and I noticed a lot of the page (307 Temporary Redirect) it is not clear to me the redicet is to which page exactly ? but after searching about this message its most likely safe page so its okay to have it ,but there are some insedints of (404) which is page not found 
<img width="2236" height="864" alt="image" src="https://github.com/user-attachments/assets/43c7ac42-0e30-4654-bbf9-94b989be2dce" />

then I neede to capture the flag (what dose Customer Churn) means? at first I assumed that if the customer switched from Paied to Free it will be consedered a chrun, and I apply this logic, but no surprise, the dataset is extreemly unbalanced 
<img width="1612" height="858" alt="image" src="https://github.com/user-attachments/assets/a40759ae-038b-4427-b81e-e13b1ec19814" />

so I applied some "upsampling" and this is the result 
<img width="1836" height="958" alt="image" src="https://github.com/user-attachments/assets/e40d2574-3e98-4a68-af32-e40f05774513" />

and I tried to train a logistic regression, but then I thought about something else, what if the (Customer Churn) is gradually happening? so I added another feature, which is calculating the days sice last visit to the application 
but the majority of the useres happend to be really active, which is good as an engagment indicator 
<img width="1458" height="932" alt="image" src="https://github.com/user-attachments/assets/46bd90d5-68bb-49d1-8767-80266385f6f9" />

I tested this logic with the mini dataset and the large dataset , and it so happend that my model perform best with the large dataset, 
<img width="976" height="340" alt="image" src="https://github.com/user-attachments/assets/704020e8-74d6-432a-a92c-c87d12eb6d62" />


But then I assumeing dataleakage, becauese of the upsampling, therefore I applied the upsampling of the training dataset only, and this is the result 




