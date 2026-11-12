# Evidence and publication checklist

The actual lab screenshots have **not** been uploaded yet.

Expected files (add only after reviewing the originals):

- `NSG-001-Before.png`: temporary `Allow-RDP-From-Internet-Lab` rule with source `0.0.0.0/0`, TCP/3389, priority 100.
- `NSG-001-After.png`: NSG inbound rules showing zero custom inbound rules after deletion.

Before publishing:

1. Crop to the relevant rule list and remove unnecessary Azure Portal chrome.
2. Redact account names, email addresses, subscription IDs, tenant IDs, correlation IDs, and unrelated resources.
3. Ensure the evidence comes from the **personal** Azure lab, not employer infrastructure.
4. Verify that before/after captions accurately describe the observed configuration.
5. Do not claim live internet reachability, RDP exploitation, or a penetration test.

Evidence must be real: never substitute a mock screenshot for a screenshot of the actual configuration.
