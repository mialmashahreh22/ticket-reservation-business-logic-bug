# Ticket Reservation Business Logic Bug - Bug Explanation

## What Is the Bug?

A user can reserve tickets without paying, abandon payment, and keep tickets unavailable for too long.

## Vulnerability Type

Business Logic / Availability Abuse

## Why It Happens

The reservation system creates a hold but does not release it quickly enough when payment is not completed.

## Why It Matters

Business workflows need abuse controls, not only normal happy-path behavior.

## Safe Lab Version

This repository includes a safe local simulation of the bug. The lab does not contact any real target or live service.

Lab path:

```text
labs/ctf-game/
```

## How to Fix

- Expire unpaid holds quickly, such as after 3 to 5 minutes.
- Release seats immediately when payment fails or is abandoned.
- Rate-limit repeated holds and add cooldowns before rebooking recently released seats.

## Responsible Disclosure Note

For a real report, keep evidence redacted, avoid publishing secrets or private user data, and test only systems where you have permission.
