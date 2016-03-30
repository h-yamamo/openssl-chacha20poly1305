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
tar xf ../openssl_1.0.1e-2+deb7u20.debian.tar.gz
cp -av ../openssl-chacha20poly1305/wheezy/debian/* debian/
debuild -uc -us
```

### Debian 8 (jessie)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1k.orig.tar.gz
cd openssl-1.0.1k
tar xf ../openssl_1.0.1k-3+deb8u4.debian.tar.xz
cp -av ../openssl-chacha20poly1305/jessie/debian/* debian/
debuild -uc -us
```

### Ubuntu 12.04 LTS (precise)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1.orig.tar.gz
cd openssl-1.0.1
tar xf ../openssl_1.0.1-4ubuntu5.35.debian.tar.gz
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
tar xf ../openssl_1.0.1f-1ubuntu2.18.debian.tar.gz
cp -av ../openssl-chacha20poly1305/trusty/debian/* debian/
debuild -uc -us
```
