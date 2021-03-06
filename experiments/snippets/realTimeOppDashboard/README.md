# Real Time Opportunity Dashboard

Skuid pages generally only query the database on user request.  The user reloads the page or takes some action on the page to trigger a query.  But customers often ask whether Skuid can create a page where new data is constantly retrieved for the page—also known as "polling."  

This page uses a simple snippet that polls an "updates indicator" model periodically.  If this model returns data, the user is warned that there is new data, and they can update the page as they see fit. 

It is not wise to simply continuously poll the primary model. While the model is polling, all components connected to it are frozen (no updates can be made in the UI).  Also, unsaved changes in the model would likely be discarded every time the polling action occurred.  That could get really annoying. 
