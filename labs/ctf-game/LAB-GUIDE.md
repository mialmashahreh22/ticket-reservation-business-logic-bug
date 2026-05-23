# Ticket Reservation Business Logic Bug - CTF Lab Guide

This lab is a realistic mock simulation for one bug class.

## Goal

Find the bug in the mock app and unlock the flag.

## How to Run

From this repo root:

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/labs/ctf-game/
```

## What to Do

1. Reserve all tickets in the mock event.
2. Abandon the payment.
3. Advance the clock by 21 minutes.
4. Check availability from the second tab simulation.
5. The flag appears when tickets are still locked.

## What You Should Learn

Business workflows need abuse controls, not only normal happy-path behavior.

## Safety

This is a local mock app. Do not repeat these actions against real websites unless you have explicit authorization.
