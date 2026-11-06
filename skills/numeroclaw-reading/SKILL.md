---
name: numeroclaw-reading
description: Help someone choose and order a NumeroClaw numerology reading for themselves or as a gift. Use when the person asks for a numerology reading, a birthday or name reading, a personal gift of that kind, or asks about NumeroClaw.
---

# Ordering a NumeroClaw reading

NumeroClaw writes the reading. Your part is to help the person choose, get the details right, and hand them the link. Do not work out numbers or write any part of a reading yourself, and do not guess what a reading will say.

## Choose

Call `list_products` for current prices, delivery times and what each reading needs. Then help them choose, in a sentence or two:

- **Birthday Portrait:** only the date of birth is needed, and it arrives fastest. A good small gift or first reading.
- **Theme:** the complete reading, from the full birth name and date of birth.
- **Name Analysis:** for someone curious about their name, or who changed it, by marriage for example. It needs no date of birth.

If they want to see the writing first, share the `sampleUrl` when the reading has one.

Readings are written for adults, so a reading about a child is not a fit yet. A reading is for reflection. If someone is looking for a decision on health, money, law or a crisis, say plainly that a reading cannot help with that, and do not offer one.

## Get the details

Ask only for what the chosen reading needs, a little at a time, in normal language.

- Names go exactly as on the birth record, every name, in order.
- For a gift, the email is the buyer's. The reading goes there, and they pass it on.
- For a name with the letter Y, never ask whether the Y is a vowel or a consonant. Find every Y, including at the end of a name, work each one out from how it sounds, and check in plain words: "The Y in Yolanda sounds like the Y in yes, and the Y in Kelly sounds like the Y in Amy. Is that right?" The sound decides, not the position: Yvonne is said ee-von, so its Y sounds like the Y in Amy.

## Confirm, then order

Read back the reading, the names, the date, the email and the price, and wait for a clear yes. Only then call `create_order`. It charges nothing.

If it returns issues, explain them in plain words and ask only about what needs fixing. Nothing has been created.

## Hand over the link

Give the `paymentLink` as one clear link and say what happens next:

- The page shows the order so they can check it, then they pay on Stripe. You cannot pay for them.
- During a sale, say the `priceNote` as well.
- The reading comes by email, in the time `list_products` gave. It is never shown in this conversation.

Keep `orderToken` to yourself and use it only for `get_order` if they ask how the order is going. A reading still being written has not failed, so do not suggest a new order or a refund. If it has not arrived after the promised time, they can write to hello@numeroclaw.com with the order id.
