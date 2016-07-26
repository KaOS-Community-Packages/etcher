pkgname=etcher
pkgver=1.0.0.11
pkgrel=1
pkgdesc="Burn images to SD cards & USB drives, safe & easy"
url="http://www.etcher.io/"
arch=('x86_64')
license=('GitHub Inc.')
depends=('fuse')
source=("https://resin-production-downloads.s3.amazonaws.com/etcher/1.0.0-beta.${pkgver/*./}/Etcher-linux-x64.AppImage"
        "Etcher.desktop")
md5sums=('0758cc7c034802b6f9e0ec20c4bcd3ec'
         '72b6f038845d37ff7b4efea9ce53bf33')

package() {
    install -dm755 "$pkgdir"/usr/{bin,share/{etcher,licenses/etcher}}
    install -Dm644 Etcher.desktop "$pkgdir/usr/share/applications/Etcher.desktop"
    install -Dm644 icon.png "${pkgdir}/usr/share/pixmaps/etcher.png"
    cd "$srcdir/usr/bin/"
    mv -f LICENSE* "$pkgdir/usr/share/licenses/etcher/"
    mv -f * "$pkgdir/usr/share/etcher/"
    ln -s /usr/share/etcher/etcher "${pkgdir}/usr/bin/"
}
