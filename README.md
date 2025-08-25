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

