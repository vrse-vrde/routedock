---
"@routedock/routedock": minor
"@routedock/nulth-sdk": patch
---

Sign at most one payment per `pay()` call and bind the unsigned 402 challenge to the signed manifest before signing. x402 and mpp-charge now retry the unpaid probe freely but resend the exact same payment headers once a credential exists, and they reject any challenge whose network, payee, asset or amount disagrees with the manifest. `PaymentResult.amount` now reports the amount actually signed, and `stroopsToUsdc` is exported as the inverse of `usdcToStroops`.
