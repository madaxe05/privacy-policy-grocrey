# Privacy Policy — Grocressy

**Last updated: 10 August 2026**

Grocressy keeps your shopping data on your device. It has no account
system and no server.

This document is the same policy shown inside the app under
**Settings → Privacy**. Publish it at a public URL and link that URL in
the Google Play listing.

---

## What is stored

Your shopping list, purchase history, prices, quantities, units, stores,
categories, notes and app preferences are saved in a database file inside
the app's private storage on your device.

If you scan a receipt, Grocressy also stores the figures it read from it:
the shop name, the date, the subtotal, tax and total, how many products it
found, and a one-way fingerprint used to recognise the same receipt if you
scan it twice. If you scan a product barcode and tell Grocressy what it is,
the code and the name you gave it are saved so it is recognised next time.

**Photographs of receipts are not stored.** The picture is read, the figures
above are saved, and the image file is deleted — whether the scan succeeded
or failed. If you picked an existing photo from your gallery, that photo is
left exactly where it was and is not copied.

Grocressy also discards anything that looks like a payment card number
before it reads the receipt, so card details cannot be saved even by
accident.

## What is collected

Nothing.

Grocressy contains no analytics, advertising or crash-reporting
libraries. The app does not declare the Android `INTERNET` permission, so
it is not technically capable of sending your data anywhere.

This includes scanning. Receipts and barcodes are read by software that
runs entirely on your phone, using models built into the app itself. No
image, product name or barcode is ever uploaded, and Grocressy does not
look barcodes up in any online database — it only knows the products you
have told it about.

## What leaves your device

Only what you export yourself.

When you tap **Export** in Settings, Grocressy writes a file into its own
cache directory and hands it to Android's share sheet. Where that file
goes — email, cloud drive, another app — is entirely your choice, and is
then governed by whichever app or service you sent it to.

Android's own backup service may include the app's database if you have
device backup enabled in your system settings. That is a Google service
governed by your Google account settings, not by Grocressy. You can turn
it off in Android's Settings → System → Backup.

## Permissions

Grocressy asks you for two permissions, each at the moment you first use
the feature that needs it — never when you open the app:

- **Notifications** (`POST_NOTIFICATIONS`) — requested only if you switch
  archive reminders on in Settings. Declining leaves every other feature
  working normally.
- **Camera** (`CAMERA`) — requested the first time you photograph a receipt
  or scan a barcode. Declining leaves every other feature working normally,
  and you can still scan a receipt you have already photographed by choosing
  it from your gallery.

Choosing a receipt from your gallery uses Android's system photo picker,
which gives Grocressy the single image you select. The app does not request
access to your photo library.

It also declares one permission that Android grants automatically and
never prompts about:

- **Vibration** (`VIBRATE`) — used only for the short haptic feedback on
  actions such as ticking an item off your list. You can turn haptics off
  in Settings.

That is the complete list. The app does not access your location,
contacts, microphone, files outside its own storage, or any device
identifier, and it does not declare the `INTERNET` permission. The camera
is used only while a scanning screen is open; nothing is recorded and no
frame is kept.

## Deleting your data

Settings gives you two options at any time:

- **Delete purchase history** — removes every purchase record and price
  while keeping your current shopping list.
- **Delete all app data** — removes your list, history, prices, stores,
  categories, scanned receipt records and learned barcodes. This requires
  typing `DELETE` to confirm.

You can also remove individual learned barcodes under **Settings →
Scanned barcodes** without affecting your purchases or prices.

Uninstalling the app also removes its database from your device.

## Children

Grocressy is a general-purpose shopping utility. It does not knowingly
collect information from anyone, including children, because it does not
collect information at all.

## Changes to this policy

If a future version of Grocressy changes what is stored or transmitted,
this policy will be updated before that version is released, and the
in-app copy will be updated in the same release.

## Contact

Questions about this policy can be sent to the developer contact address
listed on the app's Google Play page.
