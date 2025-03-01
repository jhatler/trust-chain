# Personal Security Domain

The materials in this directory are used for personal communications and operations.

All OpSec measures described in the [README](../README.md) apply to these materials as well.
Any additional OpSec measures specific to this domain are described below.

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

