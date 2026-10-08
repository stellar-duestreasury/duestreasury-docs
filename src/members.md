# Guide for members

1. Review the group id, token, atomic-unit dues amount and period length with the organizer.
2. Use the public group view to read its current record.
3. Check current-period status using your public address. `period` is elapsed time since creation divided by period_seconds. A false paid flag means unpaid for this period; it does not compute historical arrears.
4. If a reviewer and maintainer later authorize a synthetic testnet exercise, connect a testnet wallet and pay once for the current period. Inspect the wallet request carefully. Save the confirmed transaction hash and explorer link.

There is no current live deployment. Do not use real funds or send funds directly to the contract. Dues can be paid only by fixed members and requires member authorization (`pay_dues` in contract `src/treasury.rs`). Token-transfer failure rolls back the paid flag and group accounting; the behavior is covered by `failed_token_transfer_rolls_back_dues_and_accounting`.
