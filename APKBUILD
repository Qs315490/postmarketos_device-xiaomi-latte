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
}

sha512sums="
7266127b624c85702b4564bdbdecb8170b5a3bcbaa0bd3bd59cb393bfbb0fd94987e2bf1243dae452fc2f475229228df4f29b8e2eed86140783b20f9260e3818  deviceinfo
e8064f39376b5c77872c7853240d33026cacaf560cd377fbf75561fd4cf324d5cc3b197ce4dd7801dbed4c22f68b760b370311d6260051e1d8cf1c5ff727490d  modules-initfs
"
