openvpn-install

OpenVPN road warrior installer for Debian, Ubuntu and CentOS.

This script will let you setup your own VPN server in no more than a minute, even if you haven't used OpenVPN before. It isn't bulletproof but has been designed to be as unobtrusive and universal as possible.

Fork

This fork includes :

No logs
No comp-lzo compression is a vector for oracle attacks, e.g. CRIME or BREACH
Better encryption (see below)
Avoid DNS leak
UFW support
TLS 1.2 only
Strong ciphers, DH keys and certificates. (see variants)
AES-256-CBC and SHA-512 for HMAC (instead of BF-128-CBC and SHA1)
Run server in unprivileged mode, reducing risks to the system
TLS-auth to help thwart DoS attacks and provide a 2nd line of defense to the TLS channel.
FDN's DNS Servers
Nearest OpenNIC DNS Servers
DNS.WATCH DNS Servers
Up-to-date OpenVPN (2.3.11) thanks to EPEL and swupdate.openvpn.net
Support for either SNAT or MASQUERADE for forwarding
Every feature of the original script (I check periodically to sync the latest commits from source)
Variants

When you lauch the script you will be asked to choose a mode. Both will work the same way, but slow has higher encryption settings, so it may slow down your connection and take more time to install.

If you're just using your VPN at home, you may choose "fast". But if you're often using public Wi-Fi or traveling a lot, you choose use slow.

FYI, "fast" is still more secured than default OpenVPN settings.

Slow (high encryption)

Features :

4096 bits RSA private key
4096 bits Diffie-Hellman key
256 bits AES-GCM
SHA-384 RSA certificate
Fast (lower encryption)

Features :

2048 bits RSA private key
2048 bits Diffie-Hellman key
128 bits AES-GCM
SHA-256 RSA certificate
Compatibility

The script is made to work on these OS :

Debian 7
Debian 8
Ubuntu 12.04 LTS
Ubuntu 14.04 LTS
Ubuntu 15.10
Ubuntu 16.04 LTS
CentOS 6
CentOS 7
Each one has been test by myself.

Installation

Run the script and follow the assistant:

wget https://raw.githubusercontent.com/safuansatay/OpenVPN1/master/install.sh
chmod +x openvpn-install.sh
./openvpn-install.sh

Once it ends, you can run it again to add more users, remove some of them or even completely uninstall OpenVPN.

You can get a cheap VPS for 2€/month at PulseHeberg.

Licence

Based on the work of Nyr

MIT Licence
