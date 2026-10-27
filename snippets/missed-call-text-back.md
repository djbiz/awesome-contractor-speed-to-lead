# Missed-call text-back playbook

When a call goes unanswered, an automatic text goes to the caller within seconds. In our audits the pattern we actually see is worse: contractors with neither a working call path nor a callback process. Fix the call path first (`sticky-tap-to-call.html`), then add text-back.

## The flow

1. Missed call detected (carrier feature, phone-system webhook, or CRM automation).
2. Text the caller within ~30 seconds: "Hi, this is {{Business}} - sorry we missed your call. How can we help?"
3. Route replies to whoever answers phones; escalate emergencies by phone per your own rules.
4. Log every exchange (timestamped) so nothing lives only in someone's phone.

## Compliance notes (US)

- Get the business's written carrier registration (10DLC campaign) sorted BEFORE sending; unregistered A2P texting gets filtered.
- Honor STOP immediately and permanently. Keep an internal suppression list; do not re-text opt-outs, even months later.
- Quiet hours: follow the business's local norms; emergency-plumbing audiences are an exception your compliance advisor should confirm.
- This is operational guidance, not legal advice.

## Where automation helps

A workflow engine (n8n, Make) watching the phone system can send the text, log it, and notify the owner. Keep a human approval step for anything beyond the first templated reply.
