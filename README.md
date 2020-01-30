# htb_api
A lot of endpoints for the HackTheBox API.

Since there is no documentation about the HackTheBox API, and I needed it to make my Discord bot (here : https://github.com/mxrch/HackTheBot), I manually searched inside the requests and in the .js used by those requests, for endpoint APIs, and found quite a few.

I leave it here, it's not documented, feel free to contribute, document and add new finds.
Hope you'll do great things ! ❤

<br>


### Some stuff
● POST /api/alert/read + api_token\
● POST /api/suggestions/post + api_token + data = { "text" : feedbackText }\
● GET /api/vouchers + api_token + voucherCode\
● POST /api/testimonials/publish + data = { "name" : name, "text" : text, "rating" : rating (int between 0 and 5), "publish" : publish (true / false) }\
● POST /api/features/vote + api_token + data = {feature: id, vote: vote}

### Subscriptions
● GET /api/subscriptions/recurly/balance + api_token\
● POST /api/subscriptions/snippet + api_token

### VPN Stats
● POST /api/vpnserver/freeslots + api_token\
● GET /api/vpnserver/status/all + api_token

### Conversations
● POST /api/conversations/list/ + api_token\
● POST /api/conversations/total/ + api_token

### Machines
● GET /api/machines/get/all + api_token\
● GET /api/machines/get/matrix/+id+/ + api_token\
● GET /api/machines/get/owns + api_token\
● POST /api/machines/vpnping/57 + api_token + data = {"id" : machine_id}\
● POST /api/machines/rate/+id+/+rating + api_token\
● POST /api/machines/rate/matrix + data = { "machine_id": id, "real": real, "cve" : cve, "enum": enumeration }\
● POST /api/machines/own/root/+id+/ + api_token + data = { "hash" : hash, "diff" : diff }\
● POST /api/machines/own/user/+id+/ + api_token + data = { "hash" : hash, "diff" : diff }\
● GET /api/machines/difficulty + api_token\
● GET /api/machines/reviews + api_token\
● GET /api/machines/todo + api_token\
● GET /api/machines/expiry + api_token\
● GET /api/machines/spawned + api_token\
● GET /api/machines/terminating + api_token\
● GET /api/machines/assigned + api_token\
● GET /api/machines/resetting + api_token\
● POST /api/machines/ping/+t + api_token

### VM actions
● POST /api/vm/reset/+id + api_token\
● POST /api/vm/vip/assign/+id + api_token\
● POST /api/vm/vip/remove/+id + api_token\
● POST /api/vm/vip/cancel/+id + api_token\
● POST /api/vm/vip/transfer/+id + api_token\
● POST /api/vm/vip/extend/+id + api_token

### Teams
● POST /api/teams/respect/+team_id + api_token

### Challenges
● POST /api/challenges/rate/+id+/+rating+ + api_token (rating pro = 1, rating sucks = 0)\
● POST /api/challenges/own/ + api_token + data = { "challenge_id" : id, "flag" : flag, "difficulty": difficulty }\
● POST /api/challenges/start + api_token + data = { "challenge_id": id, }\
● POST /api/challenges/stop + api_token + data = { "challenge_id": id, }

### Charts
● GET /api/charts/users/scores/ + api_token\
● GET /api/charts/teams/scores/ + api_token\
● GET /api/charts/universities/scores/ + api_token\
● GET /api/charts/countries/scores/ + api_token\
● GET /api/charts/vip/scores/ + api_token

### Stats
● POST /api/stats/global\
● POST /api/stats/daily/owns/+days

### Careers
● POST /api/careers/apply + api_token + data = { "name" : name, "email" : email, "phone" : phone, "cv" : cv, "id" : id }\
● POST /api/careers/application/track/+offer_id + api_token

### Users
● POST /api/user/id + api_token + data = { "username" : name }\
● POST /api/users/find + api_token + data = { "name" : query }\
● POST /api/users/respect/+user_id + api_token\
● POST /api/users/disrespect/+user_id + api_token\
● POST /api/users/htb/connection/status + api_token\
● POST /api/users/htb/fortress/connection/status + api_token\
● POST /api/users/htb/endgame/connection/status + api_token\
● POST /api/users/htb/private/connection/status/ + api_token\
● POST /api/users/htb/pro/connection/status/ + api_token

### Endgames
● POST /api/endgame/+id+/progress + api_token\
● POST /api/endgame/own + api_token + data = { "flag" : flag }

### Fortress
● POST /api/fortress/+id+/progress + api_token\
● POST /api/fortress/own/ + api_token + data = { "flag" : flag }\
● GET /api/fortress/+id+/ping + api_token

### Labs
● POST /api/labs/switch/+id + api_token\
● POST /api/labs/pro/resetrequest + api_token + data = { "resettext" : resettext }\
● POST /api/labs/pro/get/progress/+lab_id + api_token\
● POST /api/labs/pro/submit/flag/ + api_token + data = { "flag" : flag }\
● POST /api/labs/pro/feedback + api_token + data = { "text" : text, "lab" : lab_id, "rating" : proRating, "difficulty" : proDifficulty }

### Shoutbox
● POST /api/shouts/get/single/+id + api_token\
● POST /api/shouts/new/ + api_token + data = { "text" : text }\
● POST /api/shouts/get/initial/html/+num + api_token\
● POST /api/shouts/team/get/html/+num + api_token\
● POST /api/shouts/team/new/ + api_token + data = { "text" : text }\
● POST /api/shouts/support/get/html/+t + api_token\
● POST /api/shouts/support/new/ + api_token + data = { "text" : text }

### Map
● GET /vendor/d3/world-50m.v1.json\
● GET /storage/current.png
