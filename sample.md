# Project title:_P.I. Works_
---
## Purpose and Goals
### To provide features like
- __user management__ (save user)
- __display system__ for all users

***
## Project requirements
Project Requirements|Technology to use| extra/optional|
---| ---| ---|
UI design| Java etc.|Cross platform support|
Database design|SQL||

### User Interface design
UI view requirements|Status|
---|---|
Save form page|x|
Users list page|x|

### Page will consist sub pages/boxes as explained below
#### Top Border box
- A box which covers top border(~%10 of the page), which contains:
- New user button: to add new user, left justified
- hide disabled user checkbox: to hide users those field 'Enabled' is false, left justified
- Save user Button: to submit filled form, right justified

Example:
[+]New user|Hide Disabled user [x]|________________________|Save User|
---| ---| ---| ---|
#### SaveScreen borderBox
- a form which covers right border(half of page), contains forwarding information labels, and fields to add information related to that labels
    - user name: to be keep on DB
    - user display name: to be showe on UI when signed in
    - Phone: to be keep on DB
    - email: to be keep on DB
    - authentication role comboBox: to set privilege of user(guest, admin, superUser)
    - enabled tickBox: to set user enabled
    - SaveUser Button: to forward context to database

Example:
label|textField|
---| ---|
UserName|    |
Display Name|    |
Phone|    |
Email|    |

label|comboBox|
---| ---|
User role|< Select  > |

label|tick box|
---| ---|
Enabled| [ +/- ] |

#### Users page borderBox
- a page covers left border(half of screen), which contains information about saved users:
- 4 rows of information buttons, and fields related to that labels
- when information buttons clicked, fields will be sort by containing data in columns

Example as following :
ID|Name|Email|Enabled|
---| ---| ---| ---|
1|Admin1|admin@plworks.net|True
2|Test user|test@plworks.net|True
---

UI Controller Requirements|Status|
---|---|
Database connection driver|x|
get DB content for sign in|x|
set DB content for update privilege|x|
set DB content for sign up|x|
***

### Database 
DB Requirements|Status|
---|---|
Database design for user, mail, authenticationType|x|
Database setup|x|
Database deploy on a server|x|
***

- ## Sample Use Case
- User opens the UI to append a new user to system
- Form page __greets user with contents of all saved user informations before__, by getting from DB
- User enters required informations about certain user
- User selects the authentication role for new user(Guest, admin, superUser)
- User mark the tick to give access to the new user to use the system right now.
- User submits the form
    - Form forwarded to the database by server.
    - Contents checked and DB updated.
-User can see the new user at the bottom of the list on the left page
