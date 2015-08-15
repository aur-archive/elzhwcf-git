# Maintainer: Maximilien Noal (noal dot maximilien at gmail dot com) [AUR: xcomcmdr]

pkgname=elzhwcf-git
_gitname=touhy
_pkgprog=elzhwcf
pkgver=67.dcd9ed2
pkgrel=1
pkgdesc="Elzen's settings manager"
arch='any'
license='GPL3'
url='http://fadrienn.irlnc.org/touhy/'
groups='touhy'
depends=('touhy-git' 'pygtk' 'python2-pyalsaaudio')
makedepends='git'
replaces='elzaudm-git'
md5sums=('SKIP')
source=('git://fadrienn.irlnc.org/touhy')

pkgver() {
  cd ${srcdir}/${_gitname}
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd ${srcdir}/${_gitname}
  mkdir -p ${pkgdir}/usr/bin
  install ${_pkgprog} ${pkgdir}/usr/bin
  install -Dm 644 resources/appinfos/${_pkgprog}.desktop \
    ${pkgdir}/usr/share/applications/${_pkgprog}.desktop
}
