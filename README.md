# salesforce_codes
Donation Management App [Here is the problem statement]
Objects:-
Account
Total Donation: Currency (Rollup Summary)
Status:Picklist(Active, Purged)

Donations:
Amount:Currency
Status:Picklist(Planned, Donated, Cancelled, Donation Cancelled)
Cancellation Reasons:Text Area
Account:Master Detail
Source:Text
Contact Email:Email
Contact Phone:Phone
Name: Auto Number

Volunteers:
Contact Name:Text
Contact Email:Email
Contact Address:Street, City, Zip
Interest:Sporting Event, Concert, Art Exhibition, Auction, Gala
Status:Picklist(Available, Busy, Not Interested)

Public Events:
Account:MasterDetail
Volunteer Assigned:Lookup(Volunteer)
Type:Picklist(Sporting Event, Concert, Art Exhibition, Auction, Gala)
Venue:Text
Event Date: Date
Fund raised : Cuurency
Status: Picklist(Upcoming, inprogress, Completed)

When Donation is made perform the following based on status:
1)Planned: Followup with creating task, subject as name of the donation
2)Donated: Email to Contact Person
  i)Subject: Thank You!!
 ii)To:Donator Contact email
iii)Body: Thank you for your donation
3)Cancelled:Capture the reason
4)Donation Cancelled:Deduct the amount from Account

2)User should not be ble to change the amount if the status is not "Planned"

3)When a public event is created a volunteer should be assigned based on the type and availability

4)Once the public event is completed, create a donation record on the related account with the status as Donated and source as 'Public Event'.
 In this case email should not be sent.
 
5)If all the donations are cancelled/donation cancelled change the status of the account to Purged.
