
## riddlebot API


### GET /riddlebot/start

`GET https://api.noopschallenge.com/riddlebot/start`

`HTTP 200`

```
{
  "message": "Post your GitHub login to this URL to get started",
  "exampleResponse": { "login": "noops-challenge" }
}
```


### POST to /riddlebot/start to get started

`POST https://api.noopschallenge.com/riddlebot/start`


```
{
 "login": "noop-challenger"
}
```

`HTTP 200`

```
{
  "message": "Hello from Riddlebot. Get the first riddle at the provided riddlePath",
  "riddlePath": "/riddlebot/riddles/Zsy4sdsCuYrIPwbnw5HOowNvsWcxmh_uo31C8tkN4wU"
}
```


### GET the first riddle

`GET https://api.noopschallenge.com/riddlebot/riddles/Zsy4sdsCuYrIPwbnw5HOowNvsWcxmh_uo31C8tkN4wU`

`HTTP 200`

```
{
  "message": "The riddleText is reversed. When you have figured out the answer, post it back as JSON. See the exampleResponse for details.",
  "riddlePath": "/riddlebot/riddles/Zsy4sdsCuYrIPwbnw5HOowNvsWcxmh_uo31C8tkN4wU",
  "exampleResponse": { "answer": "ANSWER GOES HERE" },
  "riddleType": "reverse",
  "riddleText": "EVIF EERHT OREZ XIS OWT OWT NEVES RUOF EVIF THGIE TA KCAB EM LLAC ESAELP TOBHTAP SI TI OLLEH"
}
```


### POST to solve the first riddle

`POST https://api.noopschallenge.com/riddlebot/riddles/Zsy4sdsCuYrIPwbnw5HOowNvsWcxmh_uo31C8tkN4wU`


```
{
 "answer": "..."
}
```

`HTTP 200`

```
{
  "result": "correct",
  "nextRiddlePath": "/riddlebot/riddles/4LpseM7Yg8_wB0sX50eWCtQLPtassehfrZwjMSGhKLk"
}
```


### Solving the final riddle will give you a certificate

`GET https://api.noopschallenge.com/riddlebot/certificate/613oBeHRK_2BzTZ8YgRwxEN-hBxrD1ZOnRspvSuJ4hJks8svZvSBynJ09sOdoFQM`

`HTTP 200`

```
{
  "message": "This certifies that your-login-here completed the Riddlebot challenge.",
  "elapsed": 1928,
  "completed": "2019-06-24T22:11:39.231Z"
}
```

