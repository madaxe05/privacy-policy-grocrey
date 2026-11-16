# Privacy Policy — Grocressy

**Last updated: 16 November 2026**

Grocressy keeps your shopping data on your device and works fully without
an account. Signing in with Google is optional; it only adds backup and
family sharing of your lists.

This is the same policy shown inside the app under
**Settings → Privacy**.

---

## What is stored

Your shopping list, purchase history, prices, quantities, units, stores,
categories, notes and app preferences are saved in a database file inside
the app's private storage on your device.

If you scan a receipt, Grocressy also stores the figures it read from it:
the shop name, the date, the subtotal, tax and total, how many products it
found, and a one-way fingerprint used to recognise the same receipt if you
scan it twice. If a barcode is resolved to a product — whether that name
came from an online lookup or from you typing it — the code and the name
are saved so it is recognised next time.

**Photographs of receipts are not stored.** The picture is read, the figures
above are saved, and the image file is deleted — whether the scan succeeded
or failed. If you picked an existing photo from your gallery, that photo is
left exactly where it was and is not copied.

Grocressy also discards anything that looks like a payment card number
before it reads the receipt, so card details cannot be saved even by
accident.

Grocressy keeps a note of which app announcements you have already seen or
dismissed, purely so the same one does not keep reappearing — see
**App announcements** below.

## What is collected

Nothing for advertising. Grocressy contains no advertising libraries, does
not use your advertising ID and has no required account (an optional
Google sign-in exists, see below), and your shopping list, purchase history
and prices are never sent anywhere unless you sign in to sync your lists.

**Usage and crash data.** Grocressy uses Google's Firebase Analytics and
Crashlytics to understand how the app is used and to fix crashes. This
sends anonymous information such as which screens are opened, how long the
app is used, your device model, Android version, approximate country, and
the technical details of any crash or error. It is tied only to a random ID
created for this app install, never to your name, account or shopping
data, and is not used for advertising.

**On-device by default.** The built-in text and barcode readers run
entirely on this phone, using models bundled with the app, with nothing
about a receipt or barcode uploaded to read them.

**AI-assisted scanning** (Settings → AI-assisted scanning, off by default):
when switched on, if the on-device reading cannot make sense of
something, Grocressy may ask a free AI model for help. This can send:
the text a receipt photo was read into (payment-card-looking numbers are
stripped out first — the photo itself is never sent, only the text), a
photo you chose to take of a product to identify it, or text you typed
into the quick-add box. The request goes to Grocressy's own server (hosted
on Cloudflare), which passes it to OpenRouter, a service that routes it to
a free AI model. None of this carries your name, account or device
identity. Free AI providers may log these requests and use them to improve
their models, so do not use the quick-add box for anything private.
Turning this setting off returns every one of these features to asking you
directly instead.

**Barcodes:** the first time a code is scanned and Grocressy does not
already recognise it, the barcode itself (and nothing else — no account, no
list, no history) is sent to Open Food Facts, a free public product
database, to try to find its real name. If that fails, there is no
connection, or AI-assisted scanning is off, the app simply asks you what it
is. Every scan after the first is answered from what Grocressy already
knows, with no network request at all.

**Behind the scenes:** Grocressy uses Firebase (a Google service) to reach
the AI features above, and Firebase's App Check silently confirms to
Google that requests are coming from a genuine copy of the app — not a
piece of your data, just an attestation that the app itself is legitimate,
sent whenever the app opens regardless of whether you ever use
AI-assisted scanning.

**App announcements:** when the app opens or returns to the foreground (at
most once an hour), Grocressy checks Firebase for any current announcement
(a feature update, a tip, an occasional notice) so it can show one without
needing a full app update. This is a read-only check for public
announcement content — no part of your shopping
data, list, history or prices is sent with it. The app remembers, on this
device only, which announcements you have already seen or dismissed.

One honest caveat: any of the network activity above means this phone can
reach the internet at all, which it previously could not do under any
circumstance with AI-assisted scanning and the barcode lookup both off.
Google's on-device scanning components, bundled with the app, are
separately reported by some developers to periodically send their own
anonymous usage diagnostics when a connection exists — this is Google's
library behaviour, not something Grocressy's own code requests or
controls, and no reliable way to disable it has been published.

## Optional account, sync and family sharing

Everything below applies **only if you choose Settings → Account → Sign in
with Google**. Signed out, none of it happens.

- **Account data:** your Google name, email address and a Firebase user ID,
  provided by Google Sign-In through Firebase Authentication.
- **Synced data:** the names, budgets and items (name, quantity, unit,
  prices you typed, category, note, ticked and urgent state, order) of your
  shopping lists, stored in Google Cloud Firestore. **Purchase history,
  price history, barcodes, receipts and settings are not synced** and stay
  on your device.
- **Family sharing:** when you share a list, a 6-character code is created.
  It works for one hour, then a new one is needed. Anyone who enters it
  while it works can join the list, see and edit its items, and see
  that the list is shared. Your name and email are not shown to them by
  Grocressy. You can stop sharing (everyone else is removed and the code
  stops working) or, as a member, leave a list.
- **Purpose:** backup and keeping your lists in step between devices and
  family members. Not used for advertising or analytics.
- **Control:** signing out keeps all your data on the phone. Settings →
  Account → **Delete my cloud data** removes the lists you own from the
  cloud, removes you from lists shared with you, and signs you out; your
  data on the phone is kept. Settings → Account → **Delete my account**
  does the same and then permanently deletes your sign-in record (name,
  email and user ID) from Firebase Authentication; Google may ask you to
  confirm your Google account first.

## What leaves your device

**What you export yourself.** When you tap Export, Grocressy writes a file
into its own cache directory and hands it to Android's share sheet. Where
that file goes — email, cloud drive, another app — is entirely your
choice, and is then governed by whichever app or service you sent it to.

**If you sign in:** your lists and their items, and your Google name, email
and user ID, are sent to Google Firebase (Authentication and Firestore) over
HTTPS, as described under "Optional account, sync and family sharing".

**When scanning an unrecognised barcode:** the barcode itself — sent to
Open Food Facts to look up its name, as described above.

**When AI-assisted scanning is on and needed:** redacted receipt text, a
product photo you chose to take, or quick-add text you typed — sent
through Grocressy's server and OpenRouter to a free AI model, as described
above. Never sent automatically or in the
background, only when one of those features is actually used.

**A device attestation token,** sent to Google via Firebase App Check each
time the app opens, regardless of whether AI features are used — see
above.

**A request for the current app announcement,** when the app opens or
returns to the foreground (at most once an hour) — see above. Carries no
shopping data.

**Anonymous usage statistics and crash reports,** sent to Google via
Firebase Analytics and Crashlytics — see above. Carries no shopping data.

Android's own backup service may include the app's database if you have
device backup enabled in your system settings. That is a Google service
governed by your Google account settings, not by Grocressy. You can turn
it off in Android's Settings → System → Backup.

## Permissions

Grocressy asks you for two permissions, each at the moment you first use
the feature that needs it — never when you open the app:

- **Notifications** (`POST_NOTIFICATIONS`) — requested only if you switch
  archive reminders or occasional reminders on in Settings, or ask to be
  reminded about items you just added. Declining leaves every other
  feature working normally.
- **Camera** (`CAMERA`) — requested the first time you photograph a
  receipt, scan a barcode, or take a photo to identify a product. Declining
  leaves every other feature working normally, and you can still scan a
  receipt you have already photographed by choosing it from your gallery.

Choosing a receipt from your gallery uses Android's system photo picker,
which gives Grocressy the single image you select. The app does not request
access to your photo library.

It also declares permissions Android grants automatically and never
prompts about:

- **Vibration** (`VIBRATE`) — used only for the short haptic feedback on
  actions such as ticking an item off your list. You can turn haptics off
  in Settings.
- **Internet access** (`INTERNET`) and **network state** — used for the
  barcode lookup, app announcements, the optional sign-in and list sync,
  and, when AI-assisted scanning is on, the AI features described above.
- **Run at startup** (`RECEIVE_BOOT_COMPLETED`) — only re-arms reminders
  you switched on after the phone restarts.
- **Exact alarms** (`SCHEDULE_EXACT_ALARM`) — lets a reminder you set for
  items fire at the time you picked, when Android allows it. Recent Android
  versions leave it off unless you turn it on in system settings; the
  reminder then arrives a little late instead. Grocressy never asks for it.

That is the complete list. The app does not access your location,
contacts, microphone, files outside its own storage, your advertising ID,
or any hardware identifier (analytics uses only a random, app-specific ID,
as described above). The camera is used only while a scanning screen is open;
nothing is recorded and no frame is kept.

## Deleting your data

Settings gives you two options at any time:

- **Delete purchase history** — removes every purchase record and price
  while keeping your current shopping list.
- **Delete all app data** — removes your list, history, prices, stores,
  categories, scanned receipt records and learned barcodes. This requires
  typing `DELETE` to confirm.

You can also remove individual learned barcodes under **Settings →
Scanned barcodes** without affecting your purchases or prices.

If you use an account, **Settings → Account → Delete my cloud data**
removes your synced lists and shared memberships from the cloud, and
**Settings → Account → Delete my account** also deletes the account itself.

Uninstalling the app also removes its database from your device.

### Deleting your account without the app

If you no longer have the app installed, install it again, sign in with
the same Google account and use **Settings → Account → Delete my account**.
If you cannot do that, write to the developer contact address listed on the
app's Google Play page from the email address of the account and ask for it
to be deleted. Your sign-in record, the lists you own and your membership
of shared lists are then deleted within 30 days. Nothing is kept afterwards.

## Children

Grocressy is a general-purpose shopping utility. It does not knowingly
collect information from anyone, including children.

## Changes to this policy

If a future version of Grocressy changes what is stored or transmitted,
this policy will be updated before that version is released, and the
in-app copy will be updated in the same release.

## Contact

Questions about this policy can be sent to the developer contact address
listed on the app's Google Play page.
