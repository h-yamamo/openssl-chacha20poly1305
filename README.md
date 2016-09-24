# OpenSSL additional feature: Support ChaCha20+Poly1305 cipher suites

For Debian and Ubuntu packages.

## How to make packages

### Debian 7 (wheezy)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1e.orig.tar.gz
cd openssl-1.0.1e
tar xf ../openssl_1.0.1e-2+deb7u21.debian.tar.gz
cp -av ../openssl-chacha20poly1305/wheezy/debian/* debian/
debuild -uc -us
```

### Debian 8 (jessie)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1t.orig.tar.gz
cd openssl-1.0.1t
tar xf ../openssl_1.0.1t-1+deb8u5.debian.tar.xz
cp -av ../openssl-chacha20poly1305/jessie/debian/* debian/
debuild -uc -us
```

### Debian 8 (jessie-backports)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.2i.orig.tar.gz
cd openssl-1.0.2i
tar xf ../openssl_1.0.2i-1~bpo8+1.debian.tar.xz
cp -av ../openssl-chacha20poly1305/jessie-backports/debian/* debian/
debuild -uc -us
```

### Ubuntu 12.04 LTS (precise)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1.orig.tar.gz
cd openssl-1.0.1
tar xf ../openssl_1.0.1-4ubuntu5.38.debian.tar.gz
cp -av ../openssl-chacha20poly1305/precise/debian/* debian/
debuild -uc -us
```

### Ubuntu 14.04 LTS (trusty)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1f.orig.tar.gz
cd openssl-1.0.1f
tar xf ../openssl_1.0.1f-1ubuntu2.21.debian.tar.gz
cp -av ../openssl-chacha20poly1305/trusty/debian/* debian/
debuild -uc -us
```

### Ubuntu 16.04 LTS (xenial)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.2g.orig.tar.gz
cd openssl-1.0.2g
tar xf ../openssl_1.0.2g-1ubuntu4.5.debian.tar.xz
cp -av ../openssl-chacha20poly1305/xenial/debian/* debian/
debuild -uc -us
```

Since May 11 2016, an **update test-certs patch required** to build
packages in **wheezy**.
That certs patch named `Update-S-MIME-certificates.patch` is in the
debian-package-files of jessie.

Get from

`http://security.debian.org/pool/updates/main/o/openssl/openssl_1.0.1t-1+deb8u5.debian.tar.xz`

or some mirror site.

Before you build,
* copy `Update-S-MIME-certificates.patch` to `debian/patches/`
* add `Update-S-MIME-certificates.patch` to `debian/patches/series`
