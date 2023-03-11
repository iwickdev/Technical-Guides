---
layout: default
title: Passwords
parent: Security 
nav_order: 2
---

# Passwords

Created 26.8 by Heli

## Strong passwords
Here's a list of features good passwords have:
- At least 12 characters long, preferably over 16
- Combination of upper case & lower case letters, numbers and special symbols
- Not re-used on other accounts
- No personal info
- No common or repeating patterns

Another method for creating extremely strong but still easy to remember passwords is [Dice-Generated Passphrases](https://www.eff.org/dice) by EFF.

## Password Managers
  To help remember and generate strong passwords, you should use a password manager.
- I recommend **[Bitwarden](https://bitwarden.com/)**
  - Open source, audited, easy to use, free.
- Another option is **[1Password](https://1password.com/)**
  - Easy to use, audited but paid & closed source
- **Make sure your master password is very strong**
  - It should either be a dice-generated passphrase with a length of 6 words or
  - It should have **at least** 16 characters and meet the requirements defined above.

# MFA or Multi-Factor Authentication
MFA is a mechanism whre you have to provide additional verification on loign, so just entering your username and password isn't enough. Having this added factor increases security significantly, as it safeguards your account even if someone manages to guess or crack your password.

Common methods of MFA are codes sent via SMS or E-mail, app based solutions and hardware security keys. With hardware keys being the most secure.

### Implementing MFA

The recommended way to use MFA, in this case 2FA is via authenticator apps. This recommendation is due to it being widely supported, easy to use and reasonably secure. Authenticator apps use a protocol called TOTP which stands for *Time-based One-time Password*. This works by generating you a new code every 30 seconds which you can use on login.

It is important that you back up your recovery codes. You can do this in many ways, the recommended method is through your authenticator app, you should store this on another device.

#### Recommended applications
> Mobile authenticator applications are **highly** recommended, due to the tighter security models of mobile operating systems compared to desktop operating systems.

For Android **[Aegis](https://getaegis.app/)** is recommended
- Free and open source
- Easy and simple to use 
- Secure

For IOS **[Raivo OTP](https://raivo-otp.com/)** is recommended
- Free and open source
- Native and lightweight
- Secure
- iCloud sync & backups
