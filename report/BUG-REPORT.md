# Bug Report: Ticket Reservation Business Logic Bug

## Summary

Tickets can be reserved without completing payment and remain locked too long, allowing an attacker to block real buyers.

## Vulnerability Type

Business Logic / Availability Abuse

## Severity

High

## Related CWE

CWE-840: Business Logic Errors

## Steps to Reproduce

1. Select tickets in one session.
2. Proceed to checkout but do not pay.
3. Wait beyond a reasonable hold time.
4. Refresh in another session and observe tickets remain unavailable.

## Expected Behavior

Unpaid reservations should expire quickly and abuse patterns should be rate-limited.

## Actual Behavior

Tickets remain locked for over 20 minutes after abandoned checkout and can potentially be rebooked repeatedly.

## Impact

- Denial of service against legitimate buyers.
- False scarcity or sold-out appearance.
- Revenue loss and reputational harm.

## Remediation

- Use short reservation windows, such as 3-5 minutes.
- Release tickets automatically when payment fails or expires.
- Rate-limit repeated holds and add cooldowns for recently released seats.

## Evidence Guidance

For a real responsible disclosure report, include only authorized evidence:

- Redacted screenshots
- Redacted request and response examples
- Timeline of testing
- Clear reproduction steps
- No real secrets, tokens, private personal data, or destructive live actions

## CTF Lab

The lab in `labs/ctf-game` teaches this bug class using safe mock data. Complete all missions to reveal the flag.
