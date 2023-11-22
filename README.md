# Xiaomi BootLoader Bypass

![Version: 1.0](https://img.shields.io/badge/Version-1.0-brightgreen?style=for-the-badge) ![中文文档](https://img.shields.io/badge/中文文档-brightgreen?style=for-the-badge)

A PoC that exploits a vulnerability to bypass the Xiaomi HyperOS community restrictions of BootLoader unlocked account bindings.

Feel free pull request if you want :)

## php-adb

The project proudly uses the [php-adb](https://github.com/MlgmXyysd/php-adb) library.

## Buy me a Coffee

✨ If you like my projects, you can buy me a coffee at:

 - [爱发电](https://afdian.net/@MlgmXyysd)
 - [PayPal](https://paypal.me/MlgmXyysd)
 - [Patreon](https://www.patreon.com/MlgmXyysd)

## Warning

After unlocking the BootLoader, you may encounter the following situations:

- Software or hardware not working properly or even damaged.
- Loss of data stored in the device.
- Credit card theft, or other financial loss.

If you're experiencing any of the above, you should take all the responsibility yourself as this is the risk you may encounter when unlocking BootLoader. This obviously does not cover all risks. You've been warned.

- Warranty lost. Not only the base warranty, but some of the extra extended warranties (such as Mi Care or broken-screen warranty) that you have purchased may also be lost according to the exclusions provided by Xiaomi.
- Hardware level self-destruct like Samsung Knox. TEE-related features will be permanently damaged. There is no way to restore other than by replacing the motherboard.
- Functional anomalies after flashing a third-party system due to closed-source kernel source code.
- Device or account banned by unlocking BootLoader.

If you're experiencing any of the above, consider yourself damned. Ever since Xiaomi restricted unlocking BootLoader, it has been against Xiaomi's 'geek' spirit and even the GPL. Xiaomi's restrictions on BootLoader unlocking are endless, and there's nothing we as developers can do about it.

## Unlocking requirements

- An valid device:
  - A unbanned\* Xiaomi, Redmi or POCO device.
  - Device is running the official version of HyperOS.
  - (Update 2023/11/23) Device is not forced to verify account qualification by Xiaomi.
- An valid SIM card:
  - Except for tablets that cannot use SIM cards.
  - SIM card must not be out of service.
  - SIM card needs to be able to access the internet.
  - Only 2 devices per valid SIM card are allowed to be unlock to a valid SIM card within a three-month period.
- An valid Xiaomi account:
  - Each account can only unlock 1 phone in a month and 3 phones in a year period.
  - Account not banned\*.
- You have read and understood the Warning above.

- \*  According to the unlocking instructions provided by Xiaomi, it will prohibit some accounts and devices from using the unlocking tool, which is called "risk control".

## How to use

1. Download and install PHP 8.0+ for your system from the [official website](https://www.php.net/downloads).
2. Enable OpenSSL extension in `php.ini`.
3. Place `adb.php` in [php-adb](https://github.com/MlgmXyysd/php-adb) to the directory.
4. Download [platform-tools](https://developer.android.com/studio/releases/platform-tools) and place them in `libraries`. *Note: Mac OS needs to rename `adb` to `adb-darwin`.*
5. Open a terminal and use PHP interpreter to execute the [script](bypass.php).

- p.s. Releases has packaged the required files and click-to-run scripts.

6. Tap repeatedly on the `Settings - About Phone - MIUI Version` to enable `Development Options`.
7. Enable `OEM Unlocking`, `USB Debugging` and `USB Debugging (Security Settings)` in `Settings - Additional Settings - Development Options`.
8. Log in an _valid_\* Xiaomi account.
9. Connect phone to PC via wired interface.
10. Check `Always allow from this computer` and click `OK`.

- \* See "Unlocking Requirements" below.

11. Wait and follow the prompts of script.
12. After successful binding, you can use the [official unlock tool](https://en.miui.com/unlock/index.html) to check the time you need to wait.

## Workaround

- [52 Pojie]()
- [My Blog]()
- [My Blog (English)]()

## FAQ

- Q: Why does the unlock tool still remind me to wait 168/360 (or more) hours?
- A: By principle, this PoC only bypasses the restrictions added for HyperOS. You still need to comply with the restrictions for MIUI.

- Q: Binding failed with error code 401.
- A: Your Xiaomi account credentials have expired, you need to log out and log in again in your device.

- Q: Binding failed with error code 20086.
- A: Your device credentials have expired, you need to reboot your device.

- Q: Binding failed with error code 20090 & 20091.
- A: Device's Security Device Credential Manager function failure, contact after-sales.

- Q: Binding failed with error code 30001.
- A: Your device has been forced to verify the account qualification by Xiaomi. Xiaomi lost its 'geek' spirit a long time ago, and there's nothing we can do about it.

## License
No license, you are only allowed to use this project. All copyright (and link, etc.) in this software is not allowed to be deleted or changed without permission. All rights are reserved by [MeowCat Studio](https://github.com/MeowCat-Studio), [Meow Mobile](https://github.com/Meow-Mobile) and [NekoYuzu](https://github.com/MlgmXyysd).