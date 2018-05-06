# Maintainer: davidhdz <david dot vzla at gmail dot com>
# Contributor: llde 
# Contributor: rafaelsoaresbr <rafaelsoaresbr@gmail.com>
# git: https://github.com/davidhdz/modelio-bin
pkgname=modelio-bin

# Version
pkgver=3.7
pkgrel=1

# Generic
pkgdesc="The opensource modeling environment"
arch=('i686' 'x86_64')
url="https://www.modelio.org/"
license=('GPL3')
#groups=()

# Dependencies
depends=('libxtst' 'libstdc++5' 'webkitgtk2' 'glib2')
optdepends=('atk' 'gtk2' 'cairo')
#makedepends=()
#checkdepends=()

# Package Relations
#provides=()
#conflicts=()
#replaces=()

# Others
#backup=()
#options=()
#install=modelio
changelog=changelog

# Sources
source=("modelio.desktop" "changelog")
source_i686=("modelio-${pkgver}-i686::https://sourceforge.net/projects/modeliouml/files/${pkgver}.${pkgrel}/modelio-open-source${pkgver}_${pkgver}.${pkgrel}_i386.deb/download")
source_x86_64=("modelio-${pkgver}-x86_64::https://sourceforge.net/projects/modeliouml/files/${pkgver}.${pkgrel}/modelio-open-source${pkgver}_${pkgver}.${pkgrel}_amd64.deb/download
")
#noextract=()
#validpgpkeys=()
sha256sums=('SKIP'
            'SKIP')
sha256sums_i686=('SKIP')
sha256sums_x86_64=('SKIP')

#pkgver() {
#}

prepare() {
    ar p modelio-${pkgver}-${CARCH} data.tar.xz | tar xJ
}

#build() {
#}

#check() {
#}

package() {
    install -dm755 "${pkgdir}/usr/share/applications/"
    install -dm755 "${pkgdir}/opt/modelio"
    install -Dm755 "${srcdir}/modelio.desktop" "${pkgdir}/usr/share/applications/"
    cp -r "${srcdir}"/usr/lib/modelio-open-source3.7/* "${pkgdir}/opt/modelio/"
}
