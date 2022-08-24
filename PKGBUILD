# Maintainer: Ayush Jaipuriyar <ayushjaipuriyar21@gmail.com>
pkgname=battmngr-14are05-git
pkgver=1
pkgrel=1
pkgdesc="Battery manager to handle system performance modes and charge modes 
        through acpi_calls (for ideapad 14are05 only)."
url="https://github.com/ayushjaipuriyar/battmngr"
arch=('x86_64')
license=('GPL3')
depends=('acpi_call')
makedepends=('git')
provides=("${pkgname}")
source=("git+$url")
sha256sums=('SKIP')

pkgver() {
    cd ${pkgname}
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd ${pkgname}
    install -D "${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
