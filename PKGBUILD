# Maintainer: LinRs <LinRs at users.noreply.github.com>
# Contributor: Gavin Lloyd <gavinhungry@gmail.com>

# Image cloned from http://www.stickpng.com/img/bots-and-robots/android-robot-sideview-character
# License: Free for personal use only
# Commercial usage: Not allowed

pkgname=androidscreencast
_pkgname=androidscreencast
pkgver=0.0.13s
pkgrel=2
pkgdesc='Desktop app to control an android device remotely using mouse and keyboard'
arch=('any')
url='https://github.com/xSAVIKx/AndroidScreencast'
license=('Apache')
depends=('java-runtime>=7' 'android-tools')
source=("${pkgname}-${pkgver}.tgz"::"https://github.com/xSAVIKx/AndroidScreencast/releases/download/v$pkgver/androidscreencast-$pkgver-linux.tar.gz"
        'androidscreencast' "${_pkgname}.png" "${_pkgname}.desktop" )
sha256sums=('3f2b33b7d7067d78793c49ab3b59f4bb7d2ae939b583cae6dd4e71919ac82329'
            '7f9ae071315067a3f90eb37e52c69125bd8a332f51dc179ef67847853b0a2c0d'
            '0d53f19e9599873e5319cb5eae3235be1b931537d9297e630266cb5360438fc7'
            '5fbcf8f699c48ec21dd7e46a73b43fc90711d774f430574a8630067fc2def0a1')


package() {
    cd "${srcdir}/${_pkgname}-${pkgver}"
    install -Dm644 "${_pkgname}-${pkgver}-executable.jar" "${pkgdir}"/usr/share/java/"${_pkgname}/${_pkgname}.jar"
    cd "${srcdir}"
    install -Dm755 "${_pkgname}" "${pkgdir}/usr/bin/${_pkgname}"
    install -Dm644 "${_pkgname}.png" "${pkgdir}/usr/share/pixmaps/${_pkgname}.png"
    install -Dm644 "${_pkgname}.desktop" "${pkgdir}/usr/share/applications/${_pkgname}.desktop"
}
