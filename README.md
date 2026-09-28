# Mellon Firmware

Signed firmware releases for **Mellon**, a bridge module that connects a
Ford F-150 Lightning to a WOLFBOX SmartSlide tonneau cover (BLE), watches the
truck's CAN bus for lock/gear/ignition state, and maps HomeLink buttons to
cover commands.

> [!WARNING]
> **This is beta software.** Mellon listens to your truck's CAN bus and controls your tonneau cover based on various vehicle states. Beta releases are tested only on the developer's own truck and may contain bugs that cause unexpected cover movement, lighting behaviour, or failure to respond. Don't rely on it where an unexpected cover movement could cause injury or damage, and keep clear of the cover when it may move. It's provided as-is, with no warranty. You install and use it at your own risk.
>
> After installing a beta, Mellon's portal asks you to acknowledge this before anything else.

This repository holds **release images only**. The source lives elsewhere.

## Installing an update

1. Open your Mellon's config portal (`http://mellon.local`, or join its
   `Mellon_…` WiFi network) and sign in.
2. Go to **Advanced → Firmware update**.
3. Paste the URL of the `.bin` file attached to the release you want
   (right-click the asset on the Releases page → *Copy link address*).
4. Press **Check & install**. The status LED blinks white while it downloads;
   Mellon reboots into the new version when it's done.

Every image is signed. Mellon verifies the signature before installing and
refuses anything that isn't signed by the project's release key, and it
falls back to the previous version automatically if a new one fails to boot.

## Supported vehicles

- Ford F-150 Lightning (CAN signals confirmed on the vehicle). Other trucks
  aren't supported yet.
