# Personal Security Domain

The materials in this directory are used for personal communications and operations.

All OpSec measures described in the [README](../README.md) apply to these materials as well.
Any additional OpSec measures specific to this domain are described below.

## GPG (PGP) Keys

My personal GPG key can be found at [gpg/certify.pub.asc](gpg/certify.pub.asc).

It is also available via my [Keybase account](https://keybase.io/jaremyhatler)
and the following keyservers:
- https://keyserver.ubuntu.com
- https://keys.openpgp.org
- https://pgp.mit.edu

This key is trusted by my [professional key](../professional/gpg/certify.pub.asc) to a depth
of 1, which means that keys I sign with my personal key are trusted by my professional key.

Additionally, my professional key is trusted by this key to a depth of 2, making it an
introducer for my personal keyring. This means that any keys that I give a trust signature to
with my professional key may sign other keys which my personal key will trust.

The Certify Key is kept offline, and instead Signing, Encryption, and Authentication subkeys are
used for day-to-day operations. The fingerprints of each key are and other relevant information
can be found below.

**Certify Key:**
```
Key ID:           B4A8EB6FC43FF611
UIDs:             Jaremy Hatler <root@jhatler.com>, Jaremy Hatler <hatler.jaremy@gmail.com>
Fingerprint:      1B9C CE90 1F56 7FF0 DC8D  0F8D B4A8 EB6F C43F F611
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          Never
```

**Signing Key:**
```
Subkey ID:        13E13DDA35ED1BA1
Fingerprint:      FCF8 602F BCDB 3C92 E60F  1019 13E1 3DDA 35ED 1BA1
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          2027-02-10
```

**Encryption Key:**
```
Subkey ID:        CB859E689761C236
Fingerprint:      2B63 CB2F 2B29 22A8 0A4D  F8B2 CB85 9E68 9761 C236
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          2027-02-10
```

**Authentication Key:**
```
Subkey ID:        734967A14F21B091
Fingerprint:      1880 4530 91AD 48D7 8F72  61BD 7349 67A1 4F21 B091
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          2027-02-10
```

## SMIME

I use SMIME for email encryption and signing in my personal life, along with GPG. I have
obtained a certificate from a public CA for this purpose, which requires verification of my
government-issued ID to obtain/renew. You can find the certificate at
[x509/smime.pem](x509/smime.pem). The intermediate CA which issued the certificate can be
found at [x509/smime-chain.pem](x509/smime-chain.pem).

## Certificate Authorities
I operate a private Root and Intermediate CA for issuing certificates used within my home and
for private services I host in various places. The Root CA is kept offline and is only used to
sign the Intermediate CA and CRLs. The Intermediate CA is used to sign all other certificates
and CRLs, and is generally kept offline as well. I will occasionally create certificates for
other people, but only for those I know personally and trust.

You can find the Root CA at [ca/Jaremy_Hatler-RootCA.pem](ca/Jaremy_Hatler-RootCA.pem) and the
Intermediate CA at [ca/Jaremy_Hatler-InermediateCA.pem](ca/Jaremy_Hatler-InermediateCA.pem).

## Personal x.509 Certificates

The following x.509 certificates are used for my personal operations and have been issued by
my private CA:
- [Client Authentication](x509/client-auth.pem): Used to authenticate myself to servers.
- [Digital Signature](x509/digital-signature.pem): Used to sign documents and other materials.
- [Card Authentication](x509/card-auth.pem): Used to authenticate my YubiKey for physical access.

