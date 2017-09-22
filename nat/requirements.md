# Requirements & DB Schema
# How it works

**Assumptions:**
* Listed tasks can no longer be modified, but may be deleted

Task creators can create a task which will be listed on the catalogue.  They can wait for bidders and select a bidder to do his/her task. After the task is done, he/she will mark the task as `COMPLETED` and give a review to the task doer (/advanced/).

Task doers who are looking for a job can search by clicking on the listed categories or typing in search bar (advanced) / filtering by attributes, and we’ll find relevant tasks.  Once they’ve found a task that they’re interested in doing, they can bid for that task (give a price) and wait for the task creator to confirm who will be the task doer.

# Requirements
##### Users
* Types of users: `Admins`, `Taskers` (Taskers can request or complete tasks)
* Log in/out
* Create a new task
* View all tasks created before
	* View bidders for task
	* Confirm bidder for task
	* View profiles of bidders for task
* Bid for a listed task
	* Give a price for one’s services in $ / hr
	* Leave a note explaining one’s expertise
	* Can’t bid more than 10 bids (10 tasks)
* Edit tasks created before (All bidders need to be notified & remove their bid?)
* Delete task created before (All bidders need to be notified)

_Attributes_
* Name
* Email
* HP no.
* Gender
* Description quote ‘about me’

_Advanced_
* Attributes: Profile picture
* Tasks completed (can even have a rank)
* View reviews from others
* Give reviews to other users

##### Tasks
**Assumptions:** Tasks should only last for 1 day (max). Tasks are one-off.
* Types of tasks: `AWAITING_BIDDERS`, `ONGOING`, `COMPLETED`
* List all tasks which are `AWAITING_BIDDERS`  for all users
* List all tasks which are `ONGOING`  only for own tasks requested
* List all tasks which are `COMPLETED` only for own tasks requested
* Sort tasks by due date
* Sort tasks by difficulty

_Attributes_
* User who posted this task
* Title
* Description
* Location (Latitude/Longitude so that Google Maps can be used)
* Due date
* Time to meet task requester before beginning task
* Tags: e.g. washing, cleaning, moving, heavy things, repairs (at least 1)
* Price / hr
* Bidders (list of users currently bidding for this task)

_Advanced_
* Attributes: Difficulty level of task
* Show ‘Most tasks with this category were requested at $22 / hr’ when a tasker is setting a price
* Mini-forum of questions for this task that any user can ask
* Task creator can reply to questions

##### Admins
**Assumptions:** Only authorised company personnel.
* Number of users in system week-on-week / month-on-month
* Number of tasks requested in system week-on-week / month-on-month
* Number of tasks completed in system week-on-week / month-on-month
* Percentage of male / female users
* List percentage of tasks which are `AWAITING_BIDDERS`  for all users
* List percentage of tasks which are `ONGOING`  for all users
* List percentage of tasks which are `COMPLETED`  for all users
* Filter percentage of tasks with their different tags

_Attributes_
* Name
* Email
* Contact no.
