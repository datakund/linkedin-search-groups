## Linkedin-Search-Groups
A python library that uses browser automation to login & search for groups on linkedin & fetch results
It uses [datakund](https://pypi.org/project/datakund) internally

Complete Documentation available [here](https://linkedin-api.datakund.com/en/latest/)


### Support
For any help / feedback you can message us here
* datakund@gmail.com
* https://t.me/datakund

### Installation

```sh
pip install linkedin-search-groups
```

### Import

```javascript
from linkedin-search-groups import *
```

### Login

To search for groups & fetch results on linkedin first we will login to linkedin. There are two ways of login:-
* Credentials
* Cookies

#### Credentials

```javascript
linkedin.login(email="",password="")
```

#### Cookies

```javascript
linkedin.login_cookie(cookies="list_of_cookies")
```

##### Example Cookies

To login with cookies [Edit this Cookie Extension](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=en) can be added to browser and login to linkedin.com , then export cookies and paste in above function of ``login_cookie``. Below is the example of cookies.

```[
{
    "domain": "linkedin.com",
    "expirationDate": 1671116358.392265,
    "hostOnly": false,
    "httpOnly": false,
    "name": "__Secure-3PAPISID",
    "path": "/",
    "sameSite": "no_restriction",
    "secure": true,
    "session": false,
    "storeId": "0",
    "value": "Y1zkx3HJhktM4Y__/A-aOUDHse1TaSaKpQ",
    "id": 1
},
{
    "domain": "linkedin.com",
    "expirationDate": 1672322803.302724,
    "hostOnly": false,
    "httpOnly": true,
    "name": "__Secure-3PSID",
    "path": "/",
    "sameSite": "no_restriction",
    "secure": true,
    "session": false,
    "storeId": "0",
    "value": "5AcqKCt5MuBkjOpLW7PdfNs83knLqt-qVZJzCriY_4_cftxmyExDbYRS65ezLjpKa_Xc7Q.",
    "id": 2
},
...
...

]
```

### Search Groups

To search for groups on linkedin we use ``search_groups`` function.
It requires **keyword** as input parameter.

```javascript
linkedin.search_groups(keyword="groups_search_keyword_here")
```
### Fetch Groups

To fetch groups from search results we use ``groups_results`` function.
It does not require any input parameter.

```javascript
response=linkedin.groups_results()
groups=response['body']
```
### Example Response

```javascript
[
   {
      "Title":"Title 1",
      "Group Link":"Group Link 1",
      "Members":"Members 1"
   },
   {
      "Title":"Title 2",
      "Group Link":"Group Link 2",
      "Members":"Members 2"
   }
]
```

### DataKund
It uses [datakund](https://pypi.org/project/datakund/) internally to do browser automation
DataKund is an automation library that uses selenium & supports automation of many sites including [Youtube](https://youtube-api.datakund.com/en/latest/), [Amazon](https://amazon-api.datakund.com/en/latest/), [Twitter](https://twitter-api.datakund.com/en/latest/), [LinkedIn](https://linkedin-api.datakund.com/en/latest/) , [Google](https://google-api.datakund.com/en/latest/) etc.
