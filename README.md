# Guess the Number — Socket Game

A simple number guessing game made with Python using sockets.

## How It Works

* The **server** chooses a random number between 1 and 100.
* The **client** connects and tries to guess the number.
* After each guess, the server replies:

  * **Too low**
  * **Too high**
  * **Correct!** (you win)

---

## Requirements

* Python 3.6 or higher
* No extra downloads needed
---

## How to Run

### Step 1: Start the Server

Open a terminal and run:

```bash
python3 server.py
```

The server will wait for a player on port 5000.

---

### Step 2: Start the Client

Open a second terminal and run:

```bash
python3 clkient.py
```

The client connects to `localhost:5000`.

---

### Step 3: Play the Game

Type a number between 1 and 100 and press Enter.
Keep guessing until you get it right!

---

## Playing on Another Computer

If the server is running on a different computer:

1. Find that computer’s IP address.
2. Open `clkient.py`.
3. Change the `SERVER_IP` to the server’s IP address.
4. Run the client again.

---
## Example Gameplay

### Server terminal:

[SERVER] Listening on 0.0.0.0:5000...
[SERVER] Waiting for a client to connect...

[SERVER] Client connected from 127.0.0.1:54321
[SERVER] Secret number is 42

[SERVER] Guess #1: 50

[SERVER] Guess #2: 25

[SERVER] Guess #3: 37

[SERVER] Guess #4: 43

[SERVER] Guess #5: 42

[SERVER] Client guessed correctly in 5 attempt(s)!

[SERVER] Closing connections...

[SERVER] Done.

### Client terminal:

[CLIENT] Connecting to localhost:5000...
[CLIENT] Connected!

Server: Welcome! I'm thinking of a number between 1 and 100. Take a guess!

Your guess (1-100): 50
Server: Too high! Try again.

Your guess (1-100): 25
Server: Too low! Try again.

Your guess (1-100): 37
Server: Too low! Try again.

Your guess (1-100): 43
Server: Too high! Try again.

Your guess (1-100): 42
Server: Correct! You got it in 5 attempt(s)!

You win! Game over.

[CLIENT] Disconnected.

## What Happens If Something Goes Wrong?

* If the server isn’t running → the client tells you.
* If someone disconnects → the program closes safely.
* If you type something that isn’t a number → it asks again.
* Pressing Ctrl+C safely closes the program.

---

## Files

```
socjentem/
├── server.py
├── clkient.py
└── README.md
```