Here’s a **simplified version** of your README:

---

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