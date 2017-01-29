# OpenSSL additional feature: Support ChaCha20+Poly1305 cipher suites

For Debian and Ubuntu packages.

## How to make packages

### Debian 7 (wheezy)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.1t.orig.tar.gz
cd openssl-1.0.1t
tar xf ../openssl_1.0.1t-1+deb7u1.debian.tar.gz
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
tar xf ../openssl_1.0.1t-1+deb8u6.debian.tar.xz
cp -av ../openssl-chacha20poly1305/jessie/debian/* debian/
debuild -uc -us
```

### Debian 8 (jessie-backports)

```bash
# In some directory
git clone --depth 1 https://github.com/h-yamamo/openssl-chacha20poly1305
apt-get -d source openssl
tar xf openssl_1.0.2k.orig.tar.gz
cd openssl-1.0.2k
tar xf ../openssl_1.0.2k-1~bpo8+1.debian.tar.xz
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
