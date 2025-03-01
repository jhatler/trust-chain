# Professional Security Domain

The materials in this directory are used for professional communications and operations.
These materials are separate from any past or present employer.

All OpSec measures described in the [README](../README.md) apply to these materials as well.
Any additional OpSec measures specific to this domain are described below.


## GPG (PGP) Keys

My professional GPG key can be found at [gpg/certify.pub.asc](gpg/certify.pub.asc).

It is also available via my [Keybase account](https://keybase.io/jaremyhatler)
and the following keyservers:
- https://keyserver.ubuntu.com
- https://keys.openpgp.org
- https://pgp.mit.edu

This key is trusted by my [personal key](../personal/gpg/certify.pub.asc) to a depth
of 2, making it an introducer for my personal keyring. This means that any keys that I give a
trust signature to with my professional key may sign other keys which my personal key will trust.

Additionally, my personal key is trusted by this key to a depth of 1, which means that keys I sign
with my personal key are trusted by my professional key.

This key also received trust signatures from the
[Enacted Services](https://github.com/Enacted-Services/trust-chain) GPG key
for the domains `enacted.services` and `enacted.pro`, each to a depth of 2. This means that I may
give trust signatures to keys on those domains which will be trusted on behalf of Enacted Services.

I have given Enacted Services' GPG key a trust signature with this key to a depth of 3, making them
a meta-introducer for my professional keyring and an introducer for my personal keyring.

The Certify Key is kept offline, and instead Signing, Encryption, and Authentication subkeys are
used for day-to-day operations. The fingerprints of each key are and other relevant information
can be found below.

**Certify Key:**
```
Key ID:           BC7452575843F060
UIDs:             Jaremy Hatler <jhatler@enacted.services>, Jaremy Hatler <jhatler@enacted.pro>
Fingerprint:      34FB 0519 B05C 14BF 9571  52FE BC74 5257 5843 F060
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          Never
```

**Signing Key:**
```
Subkey ID:        973B2011B79353FA
Fingerprint:      0D0B 0CAD 77AF A28A 282D  C775 973B 2011 B793 53FA
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          2027-02-10
```

**Encryption Key:**
```
Subkey ID:        BC7452575843F060
Fingerprint:      B8CF 27E2 55FE ACD8 5E36  902E EE22 CB18 DBE6 49C4
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          2027-02-10
```

**Authentication Key:**
```
Subkey ID:        D5F5E45D68098391
Fingerprint:      2516 4AA1 DF9C 7356 78FF  0474 D5F5 E45D 6809 8391
Type:             RSA
Size:             4096
Created:          2025-02-10
Expires:          2027-02-10
```

## Professional x.509 Certificates

The following x.509 certificates are used for my professional operations and have been issued by
[Enacted Services' CA](https://github.com/Enacted-Services/trust-chain/tree/main/data/ca):
- [Client Authentication](x509/client-auth.pem): Used to authenticate myself to servers.
- [Digital Signature](x509/digtial-signature.pem): Used to sign documents and other materials.
- [Encryption](x509/encryption.pem): Used to encrypt documents and other materials.
- [Card Authentication](x509/card-auth.pem): Used to authenticate my YubiKey for physical access.
