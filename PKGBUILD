pkgname=etcher
pkgver=1.0.0.17
pkgrel=1
pkgdesc="Burn images to SD cards & USB drives, safe & easy"
url="https://www.etcher.io/"
arch=('x86_64')
license=('GitHub Inc.')
depends=('fuse' 'gtk2')
source=("https://resin-production-downloads.s3.amazonaws.com/etcher/1.0.0-beta${pkgver/*./.}/Etcher-1.0.0-beta${pkgver/*./.}-linux-x64.zip"
        "Etcher.desktop")
md5sums=('40e2b620d2aecb87e44c8675f2028d03'
         '72b6f038845d37ff7b4efea9ce53bf33')

prepare() {
bsdtar -xf Etcher-linux-x64.AppImage
}

package() {
    install -dm755 "$pkgdir"/usr/{bin,share/{etcher,licenses/etcher}}
    install -Dm644 ../Etcher.desktop "$pkgdir/usr/share/applications/Etcher.desktop"
    install -Dm644 icon.png "${pkgdir}/usr/share/pixmaps/etcher.png"
    cd "$srcdir/usr/bin/"
    mv -f LICENSE* "$pkgdir/usr/share/licenses/etcher/"
    mv -f * "$pkgdir/usr/share/etcher/"
    ln -s /usr/share/etcher/etcher "${pkgdir}/usr/bin/"
}
