# Remediation Notes

## Main Fixes

- Use short reservation windows, such as 3-5 minutes.
- Release tickets automatically when payment fails or expires.
- Rate-limit repeated holds and add cooldowns for recently released seats.

## Engineering Checklist

- Add server-side authorization checks.
- Add regression tests for the reported scenario.
- Log suspicious repeated attempts.
- Return minimal response data.
- Document intended business rules.
- Review related endpoints for the same pattern.

## Verification

After remediation, confirm:

- The old step no longer reproduces: Select tickets in one session.
- The old step no longer reproduces: Proceed to checkout but do not pay.
- The old step no longer reproduces: Wait beyond a reasonable hold time.
- The old step no longer reproduces: Refresh in another session and observe tickets remain unavailable.
