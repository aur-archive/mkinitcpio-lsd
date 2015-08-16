# $Id: PKGBUILD 164385 2012-08-01 01:04:59Z dreisner $
# Maintainer: Jubei-Mitsuyoshi <jubei.house.of.five.masters@gmail.com>
# Contributor: Ivailo Monev <xakepa10@gmail.com>

pkgname=mkinitcpio-lsd
_axepkgname=mkinitcpio
pkgver=0.10
pkgrel=2
groups=('base' 'lsd')
arch=('any')
pkgdesc="Modular initramfs image creation utility with udev re-instated as dependancy, part of the -lsd innitiative"
url="http://www.archlinux.org/"
license=('GPL')
depends=('awk' 'mkinitcpio-busybox>=1.19.4-2' 'kmod' 'util-linux>=2.21' 'libarchive' 'coreutils'
         'bash' 'findutils' 'grep' 'filesystem>=2011.10-1' 'file' 'gzip' 'udev>=182')
provides=("mkinitcpio=$pkgver")
conflicts=('mkinitcpio')
optdepends=('xz: Use lzma or xz compression for the initramfs image'
            'bzip2: Use bzip2 compression for the initramfs image'
            'lzop: Use lzo compression for the initramfs image'
            'mkinitcpio-nfs-utils: Support for root filesystem on NFS')
install='mkinitcpio.install'
backup=('etc/mkinitcpio.conf')
source=("ftp://ftp.archlinux.org/other/$_axepkgname/$_axepkgname-$pkgver.tar.gz"{,.sig})
sha256sums=('cd3526b135ede8ca60e05222b1e86cdf3a917947d4fd5b6e6a0a34ec408bc494'
            '21bd8a75203d15706fd66bfc9520ea1eb728736ee8f6c6a595f63f997b2673e3')

package() {
  make -C "$_axepkgname-$pkgver" DESTDIR="$pkgdir" install
}

