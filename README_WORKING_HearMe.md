# HearMe Working Package

Use `HearMe_WORKING_FULL_COLAB.ipynb` first. It embeds both the fixed frontend and `ECommerceDB.db`, so you do not need to upload the DB separately.

If you prefer separate files, use `HearMe_WORKING_EXTERNAL_ASSETS_COLAB.ipynb` with `dist.zip` and `ECommerceDB.db` uploaded to Colab.

Demo queries:
- My order ID is 21. What is my order status?
- Where is my order?
- mera customer id 21 hai, order details batao
- mera order kaha hai? / mera aadar kaha hai?

What changed:
- Real DB is bundled and opened read-only, so Colab cannot create an empty DB silently.
- Order ID maps to customer_id because your DB has customer_id but no order_id column.
- Order answers are deterministic from SQLite, not guessed by the LLM.
- Hindi/Hinglish intent detection handles order/aadar/adar/order kaha/kahan.
- Frontend sends a stable session_id and language_hint.
