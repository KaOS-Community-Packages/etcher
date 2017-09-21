pkgname=etcher
pkgver=1.1.2
pkgrel=1
pkgdesc="Burn images to SD cards & USB drives, safe & easy"
url="http://www.etcher.io/"
arch=('x86_64')
license=('apache')
depends=('gtk2' 'libxtst' 'libxss' 'gconf' 'nss' 'alsa-lib')
optdepends=('libnotify: for notifications'
	    'speech-dispatcher: for text-to-speech')
source=("https://github.com/resin-io/etcher/releases/download/v${pkgver}/etcher-electron_${pkgver}_amd64.deb")
options=("!strip")
sha256sums=('45ab555e470b382120923730e607e7a951da4f6d8a4320f0f08a960f8254942b')


package() {
    cd "$pkgdir"
    tar xf "$srcdir/data.tar.xz"
}
