# Reference: <https://postmarketos.org/devicepkg>
pkgname=device-xiaomi-latte
pkgdesc="XiaoMi Pad2"
pkgver=1
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="x86_64"
options="!check !archcheck"
depends="
	linux-xiaomi-latte
	firmware-xiaomi-latte
	postmarketos-base
	zstd
	btrfs-progs
	irqbalance
	udisks2
"
makedepends="devicepkg-dev"
source="
	deviceinfo
	modules-initfs
"

build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
	echo "/lib/firmware" >> "$pkgdir/usr/share/mkinitfs/files/00-$pkgname-modules.files"
}

sha512sums="
7266127b624c85702b4564bdbdecb8170b5a3bcbaa0bd3bd59cb393bfbb0fd94987e2bf1243dae452fc2f475229228df4f29b8e2eed86140783b20f9260e3818  deviceinfo
543456f2fc5eba0b50f5f474b451b508a40b2cfd872c1cadb17caf0c08a249e62b1883be472f70cedb21d42b0a162fa52a87f14b640f8b198cf17d9f5e391e47  modules-initfs
"
