# Maintainer: Alucryd <alucryd at gmail dot com>
pkgname=bleufear-gtk-theme-git
pkgver=20111130
pkgrel=2
pkgdesc="A dark GTK3-GTK2 theme with a wild streak of electric blue"
url="https://github.com/maxfierke/BleuFear"
license=('GPL3')
arch=('any')
depends=('gtk-engines' 'gtk-engine-unico' 'gtk-engine-murrine' 'gtk3')
makedepends=('git')

_gitroot="https://github.com/maxfierke/BleuFear.git"
_gitname="BleuFear"

build() {
  cd $srcdir
  msg "Connecting to the GIT server..."
  if [[ -d $srcdir/$_gitname ]] ; then
    cd ${_gitname}
    git pull origin
    msg "The local files are updated..."
  else
    git clone $_gitroot $_gitname
  fi
  msg "GIT checkout done."
}

package() {
    cd $srcdir
    mkdir -p $pkgdir/usr/share/themes
    mv BleuFear $pkgdir/usr/share/themes
}

