# NumeroClaw

![NumeroClaw](assets/icon.png)

NumeroClaw writes personalized English numerology readings for adults, for themselves or as a gift. Ask your assistant which readings are available, what they cost and what each one needs.

Three readings are available. The Theme is a complete portrait from a full birth name and date of birth. The Name Analysis looks at a birth name and, if it differs, the name used today. The Birthday Portrait reads the day of the month someone was born.

Your assistant creates an unpaid order and gives you a link to a NumeroClaw page. It shows the order as we received it, so you can check it, then you confirm and pay on Stripe. Nothing is charged before that, and your assistant cannot pay for you. The reading arrives by email as a private link with a PDF: usually within a few hours and always within 6 hours. If a reading is not delivered in that time or is materially wrong, the payment is refunded in full on request within 14 days.

There is no account and nothing to sign in to. NumeroClaw receives only the order details your assistant sends, not the rest of your conversation. A reading is for reflection. It is not a prediction, and it is not medical, legal, financial or other professional advice.

## What to ask

- What readings does NumeroClaw offer, and what do they cost?
- Get me a NumeroClaw Birthday Portrait for my sister. She was born on May 17, 1990.
- Order a numerology Theme from NumeroClaw for Yvonne Marie Kelly, born November 2, 1984.
- I want a NumeroClaw Name Analysis of my birth name and my married name.

## Install

Once listed, find NumeroClaw in Claude's directory. In Claude Code:

```
/plugin install numeroclaw --marketplace Apiruck-Corp/numeroclaw-plugin
```

## What this plugin contains

- **A connection to NumeroClaw's server** at `https://api.numeroclaw.com/mcp/claude`, with three tools: `list_products` (read-only), `create_order` (creates an unpaid order and charges nothing) and `get_order` (read-only).
- **One skill**, `numeroclaw-reading`, that helps the assistant explain the readings, ask only for what is needed, and read the details back before ordering.

It holds no code, runs nothing on your machine, and asks for no keys.

## What it sends and where

When you order, your assistant sends NumeroClaw the details of the order, as far as the reading needs them: the reading you chose, the names, the date of birth, the grammatical gender for a Theme, how each letter Y sounds, where and how much a current name is used, any opening note, and your email. It sends them only to `api.numeroclaw.com`, and only when you ask for an order or its status. NumeroClaw does not receive the rest of your conversation. Payment happens in your browser on Stripe, and your assistant cannot pay for you. The reading link goes only to your email.

## Links

- Help: https://numeroclaw.com/assistants/
- Privacy policy: https://numeroclaw.com/privacy/
- Sales terms: https://numeroclaw.com/terms/
- Support: hello@numeroclaw.com

## License

The contents of this repository are under the MIT License. The readings, the calculations behind them and the NumeroClaw service are not part of this repository.
