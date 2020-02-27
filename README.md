# salesforce_codes
Donation Management App [Here is the problem statement]
Objects:-
1)Account
a)Total Donation: Currency (Rollup Summary)
b)Status:Picklist(Active, Purged)

2)Donations:
a)Amount:Currency
b)Status:Picklist(Planned, Donated, Cancelled, Donation Cancelled)
c)Cancellation Reasons:Text Area
d)Account:Master Detail
e)Source:Text
f)Contact Email:Email
g)Contact Phone:Phone
h)Name: Auto Number

3)Volunteers:
a)Contact Name:Text
b)Contact Email:Email
c)Contact Address:Street, City, Zip
d)Interest:Sporting Event, Concert, Art Exhibition, Auction, Gala
e)Status:Picklist(Available, Busy, Not Interested)

4)Public Events:
a)Account:MasterDetail
b)Volunteer Assigned:Lookup(Volunteer)
c)Type:Picklist(Sporting Event, Concert, Art Exhibition, Auction, Gala)
d)Venue:Text
e)Event Date: Date
f)Fund raised : Cuurency
g)Status: Picklist(Upcoming, inprogress, Completed)

When Donation is made perform the following based on status:
1)Planned: Followup with creating task, subject as name of the donation
2)Donated: Email to Contact Person
  i)Subject: Thank You!!
 ii)To:Donator Contact email
iii)Body: Thank you for your donation
3)Cancelled:Capture the reason
4)Donation Cancelled:Deduct the amount from Account.

2)User should not be ble to change the amount if the status is not "Planned"

3)When a public event is created a volunteer should be assigned based on the type and availability

4)Once the public event is completed, create a donation record on the related account with the status as Donated and source as 'Public Event'.
 In this case email should not be sent.
 
5)If all the donations are cancelled/donation cancelled change the status of the account to Purged.
