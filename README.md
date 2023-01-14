# Articles API
Use Express.js+mongoDB+Redis to create and recieve(cache) aricles.
# APIs
* `POST api/articles`: create an article
* `GET api/articles`: recieve(cache) articles
# Examples
## Create an article
```bash
curl -X POST http://localhost:3000/api/articles \
-H 'Content-Type: application/json' \
-d '{"title":"test_title","author":"test_author", "content":"testcontent"}'
```
```json
{"title":"test_title","author":"test_author","content":"testcontent","_id":"63c212b68d873772704f5a24","createdAt":"2023-01-14T02:25:58.837Z","__v":0}          
```
## Receive articles
```bash
curl http://localhost:3000/api/articles
```
```json
[{"_id":"63c168eafbf776fa01294b36","title":"my_login","author":"my_password","content":"testcontent","createdAt":"2023-01-13T14:21:30.516Z","__v":0},{"_id":"63c1697168ce3318a331e67e","title":"my_login","author":"my_password","content":"testcontent","createdAt":"2023-01-13T14:23:45.714Z","__v":0}]
```