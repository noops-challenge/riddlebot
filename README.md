![riddlebot](https://user-images.githubusercontent.com/212941/60119479-6713fc00-9733-11e9-93c6-91a773fc0270.png)

# 👋 Meet Riddlebot

Riddlebot loves puzzles, riddles, and most of all: [ciphers](https://en.wikipedia.org/wiki/Cipher).

Riddlebot will send you riddles in the form of encrypted messages. It's up to you to decrypt them and send them back to Riddlebot's API.

Each challenge is more difficlut than the last. Can you solve them all?

# 🤖 API

Get started at `https://api.noopschallenge.com/riddlebot/start`

### Post your login to riddlebot to get started with the challenge.

`POST https://api.noopschallenge.com/riddlebot/start`

```
{
 "login": "noop-challenger"
}
```

```
{
  "message": "Hello from Riddlebot. Get the first riddle at the provided riddlePath",
  "riddlePath": "/riddlebot/riddles/1234567"
}
```


### Get the first riddle

`GET https://api.noopschallenge.com/riddlebot/riddles/Zsy4sdsCuYrIPwbnw5HOowNvsWcxmh_uo31C8tkN4wU`

```
{
  "message": "The riddleText is reversed. When you have figured out the answer, post it back as JSON. See the exampleResponse for details.",
  "riddlePath": "/riddlebot/riddles/1234567",
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

If your answer is correct, you will get the path of the next riddle in the response.

If you can solve all of the riddles, Riddlebot will grant you a certificate of riddleology.

See the [API documentation](./API.md) for more information.

## Ruby starter kit

The included (ruby starter)[./riddlebot.rb] shows how to interact with the Riddlebot API. It's up to you to write the code to figure out the answers. Good luck!

More about Riddlebot here: https://noopschallenge.com/challenges/riddlebot
