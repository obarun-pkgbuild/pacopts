# Maintainer Eric Vidal <eric@obarun.org>

pkgname=pacopts
pkgver=0.1.2
pkgrel=1
pkgdesc='A scripts to provide option for pacman after installation'
url='https://github.com/Obarun/pacopts.git'
arch=(x86_64)
license=('BEERWARE')
depends=('bash' 'pacman' 'cower' 'shadow' 'obarun-libs' 'expac')
backup=('etc/obarun/pacopts.conf')
makedepends=('git')
sha1sums=('SKIP')
source=("${pkgname}::git+${url}#tag=v${pkgver}")
validpgpkeys=('6DD4217456569BA711566AC7F06E8FDE7B45DAAC') # Eric Vidal

package() {

  cd "$pkgname"
		 
  make DESTDIR="$pkgdir" install
}
