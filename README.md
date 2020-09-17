# iOS 14 & macOS Big Sur Encrypted DNS Profile

## Disclaimer

**BY AGREEING TO USE THE FOLLOWING CONFIGURATION, YOU ARE AWARE OF THE RISKS, DANGERS, AND THAT THIS SETTING SHALL NOT BEAR RESPONSIBILITY FOR ANY DAMAGES DONE TO YOUR DEVICES.**

## Background

[Apple adds support for encrypted DNS (DoH and DoT)](https://www.zdnet.com/article/apple-adds-support-for-encrypted-dns-doh-and-dot/)

More info: https://developer.apple.com/videos/play/wwdc2020/10047/

The two main or most popular encrypted DNS protocols are:

1. [DoH (DNS-over-HTTPS)](https://en.wikipedia.org/wiki/DNS_over_HTTPS)
2. [DoT (DNS-over-TLS)](https://en.wikipedia.org/wiki/DNS_over_TLS)

## Motivation

Currently, for iOS users, a VPN profile is needed to run such encrypted DNS over the mobile network (3G/4G/LTE/5G). With the support from Apple using the profiles, it is now possible to run them natively without any VPN profile.

## Requirements

1. iOS 14 and later
2. iPadOS 14 and later
3. macOS Big Sur and later

## Usage

Download the mobile config profile using the Safari browser on the respective platforms and install the profiles. **Do note that the profile is unsigned and the settings page will display it as a warning.**

## Outcome

After the profile has been installed, you may verify if the encrypted DNS is working at [https://1.1.1.1/help](https://1.1.1.1/help).

You should expect the following:

#### Debug Information

|                          |            |
| ------------------------ | ---------- |
| Connected to 1.1.1.1     | Yes        |
| Using DNS over TLS (DoT) | Yes        |
| AS Name                  | Cloudflare |

#### Connectivity to Resolver IP Addresses

|         |     |
| ------- | --- |
| 1.1.1.1 | Yes |
| 1.0.0.1 | Yes |

![](<./Cloudflare%20DoT%20(Desktop).png>)
![](<./Cloudflare%20DoT%20(Mobile).jpeg>)

## Credits

- [Reddit - How To Set Up Cloudflare DNS over TLS (Secure DNS)](https://www.reddit.com/r/MacOSBeta/comments/i21e59/how_to_set_up_cloudflare_dns_over_tls_secure_dns/)
