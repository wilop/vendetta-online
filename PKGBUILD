pkgname=vendetta-online
pkgver=1.8.774
pkgrel=1
pkgdesc='Vendetta Online is a 3D space massively multiplayer online role-playing game.'
arch=('x86_64')
url='https://www.vendetta-online.com'
license=('custom')
depends=(glibc gtk3)
source=("https://cdn.vendetta-online.com/2024/New/vendetta-linux-amd64-installer.sh" "https://vo-wiki.com/vendettaicon.png" "vendetta-online.desktop" "vendetta-wrapper")
sha256sums=('e8e9f90a362bf7861b5f78cc2abafd93dbf47056f2fe4af717eb99b37a2564ee'
            'cc7ae84249dbf5351fe7a7f0ca33ed4f0faf5a15ade788a44efbd0dbc1ab7617'
            'ae4c8f911e4c7e0d8bbdb95b7dded3de3d7508f0cad213e4c48c5cbe36f9ec86'
            '5e9d787849475b8910b69d20e37e049ecb103ca9d61da7108bddc4e9a5c36536'
)
noextract=(vendetta-linux-amd64-installer.sh)

prepare() {
     chmod +x $srcdir/vendetta-linux-amd64-installer.sh
     $srcdir/vendetta-linux-amd64-installer.sh --target $pkgname --noexec
}

package() {
	install -dm755 "$pkgdir/opt"
	cp -r "$srcdir/$pkgname/install" "$pkgdir/opt/$pkgname"
	install -dm755 "$pkgdir/usr/bin"
	install -Dm755 "$srcdir/$pkgname/vendetta" "$pkgdir/usr/bin/vendetta"
	install -Dm755 "$srcdir/vendetta-wrapper" "$pkgdir/usr/bin/vendetta-wrapper"
	install -Dm644 "$srcdir/$pkgname.desktop" "$pkgdir/usr/share/applications/$pkgname.desktop"
	install -Dm644 "$srcdir/vendettaicon.png" "$pkgdir/usr/share/pixmaps/vendetta.png"
}
