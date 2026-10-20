feat: receipt discount in so'm or percent, by the cashier's limit (v1.0.11)

- the payment panel (desktop and phone) has a «CHEGIRMA» field with a
  so'm | % switch: a percent shows its so'm under it and the other way
  round; switching keeps the same discount; quick 5/10/15/20 % chips
- the limit comes from the permissions: discount:up_to_10, up_to_25 or
  unlimited; none hides the field; above it the cashier is told
  "Sizga berilgan chegirma limiti 10%" and the sale does not go
- totals show the goods, the discount and what is paid; change, the
  shortfall, the QR amount and the debt all count from what is paid
- the sale sends discount_amount with the paid total; the printed receipt
  has the discount line, the paid total and VAT reduced by the discount
- a server refusal about the discount is no longer taken for a stock
  shortage
- summary labels shrink instead of overflowing on narrow phones

Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>

