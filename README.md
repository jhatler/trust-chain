# Jaremy Hatler's Trust Chain

This repository contains my public cryptographic materials and the necessary tools and background
information to evaluate its trust chain.

You can cross-reference many of the materials in this repository with my
[jaremyhatler](https://keybase.io/jaremyhatler) Keybase account. This is a good way to verify
that the materials in this repository are indeed mine and have not been tampered with.
Additionally, all of the materials in this repository are signed by my personal SMIME certificate
which requires verification of my government-issued ID to obtain/renew.

In the event of a compromise, you will see a red message below explaining the situation and
providing instructions on how to proceed. Otherwise, you will see a purple message that 
indicates that the materials are valid and trusted.

> [!IMPORTANT]  
> No known compromises have occurred.
> This message **IS NOT** a substitute for your own due diligence.

## OpSec Overview

All cryptographic materials were generated offline using the instructions and scripts found at
[jhatler/YubiKey-Guide](https://github.com/jhatler/YubiKey-Guide).

Key materials are kept encrypted at rest at all times, possibly through the use of hardware tokens.
All decryption operations on these materials requires at least two factors (what you have and what
you know).

Techniques have been employed to ensure that the most sensitive materials (e.g. GPG Certify Keys)
are not needed for day-to-day operations. In situations where they are needed, they are decrypted
in memory on an air-gapped system and used only for the duration of those operations.

Day-to-day operations are exclusively performed using hardware tokens. These tokens are protected
by a PIN and are configured to require a touch to perform any cryptographic operations. The tokens
are also configured to require a touch after a short period of inactivity (where possible).

Hardware tokens are stored securely when not in use. An audit of the tokens is performed
regularly and their management keys are rotated periodically. Tokens which have been lost, stolen,
or reconfigured are considered irreversibly compromised and their materials are revoked. Tokens
which are to be decommissioned are securely wiped and physically destroyed.

To safeguard against the loss of these materials, they are backed up in multiple, secure,
geographically-distributed locations. These backups are themselves encrypted and the keys have been
sharded so they can be stored in multiple locations. A majority of the shards are required to
reconstruct the key and access the backups. Each key shard is encrypted with the combination of a
[one-time pad](https://en.wikipedia.org/wiki/One-time_pad) (shared among the shards) and a
[book cipher](https://en.wikipedia.org/wiki/Book_cipher) specific to a shared. The books used are
never written down or disclosed to other parties. These physical materials and digital media are
further protected by tamper-evident seals and a stringently documented chain of custody. 

For ecosystems that support it, revocation certificates have been pregenerated and are also stored
in the same manner as the key materials. In the event of a compromise, these certificates can be
immediately published to revoke the compromised materials.

Each commit to this repository updates the `SHA512SUMS` file with the SHA512 hashes of the files
it contains. The `SHA512SUMS` file is signed by using an SMIME certificate which has been issued by
a public CA and which required verification of my government-issued ID to obtain. Each commit is
also signed by one of my GPG keys (contained herein).
