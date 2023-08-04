The generated files are already checked in such that the
file `Makefile.am.libasncodec` is available from the start.

The ASN.1 definition of DiceTcbInfo are contained in the file `attestation.asn1`.

To update the generated files, execute:

```shell
asn1c -no-gen-OER -no-gen-PER -no-gen-example attestation.asn1
```

Hint: It is better to compile asn1c yourself with its most recent code,
since their last official release was in 2016. And this yields some old generated code,
e.g., it uses a macro which is deprecated in newer glibc versions and this
throws a lot of warnings.
