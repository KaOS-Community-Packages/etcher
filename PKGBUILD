pkgname=etcher
pkgver=1.0.0.7
pkgrel=1
pkgdesc="Burn images to SD cards & USB drives, safe & easy"
url="http://www.etcher.io/"
arch=('x86_64')
license=('GitHub Inc.')
source=("https://resin-production-downloads.s3.amazonaws.com/etcher/1.0.0-beta.${pkgver/*./}/Etcher-linux-x64.AppImage"
        "Etcher.desktop")
md5sums=('7f1da299a708d27d7f6b77cc1900ed6d'
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
