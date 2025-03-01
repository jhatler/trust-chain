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
