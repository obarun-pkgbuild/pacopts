# Maintainer Eric Vidal <eric@obarun.org>

pkgname=pacopts
pkgver=0.1.5
pkgrel=1
pkgdesc='A scripts to handle packages in conjonction with pacman'
url='https://github.com/Obarun/pacopts.git'
arch=(x86_64)
license=('ISC')
depends=('bash' 'pacman' 'cower' 'obarun-libs' 'expac' 'applysys')
backup=('etc/obarun/pacopts.conf')
makedepends=('git')
sha1sums=('SKIP')
source=("${pkgname}::git+${url}#tag=v${pkgver}")
validpgpkeys=('6DD4217456569BA711566AC7F06E8FDE7B45DAAC') # Eric Vidal

package() {

  cd "$pkgname"
		 
  make DESTDIR="$pkgdir" install
}
