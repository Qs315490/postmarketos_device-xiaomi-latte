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
b94e5c98e4771851ed57929cae76aeb7d6747b143f8cd9a9c9be9e010a725d914a286966f808a532894dde65640699c1d702a0762bad8878ff114fdf7b36caff  deviceinfo
543456f2fc5eba0b50f5f474b451b508a40b2cfd872c1cadb17caf0c08a249e62b1883be472f70cedb21d42b0a162fa52a87f14b640f8b198cf17d9f5e391e47  modules-initfs
"
