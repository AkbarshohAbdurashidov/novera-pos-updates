fix: cash change and shortfall, 0% VAT, notification read-all (v1.0.10)

Payment:
- F12 puts the cursor in the cash field: the cash typed next counts,
  so the change is shown instead of 0
- "50 000" with spaces is read as 50 000; the last customer's cash is
  cleared after a sale and never counted for the next one
- less cash than the total is shown in red ("YETMAYDI 5 500"); the
  button stays active and the sale goes through

VAT:
- a basket restored before the catalog kept bare copies with the default
  12 % rate: the cart state now sees the catalog's products replace them
  (same price used to compare equal and the update was dropped)
- the printed receipt counts VAT per line at each product's own rate
  instead of a fixed 12 %; mixed rates print "VAT:" without a percent

Notifications:
- "read all" no longer turns every notification unread: read state comes
  from the server's status, and what was marked stays marked on refresh

Other:
- the update host no longer calls setState while the app is first built
  ("setState() or markNeedsBuild() called during build")

Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>

