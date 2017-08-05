# Maintainer Eric Vidal <eric@obarun.org>

pkgname=pacopts
pkgver=0.1.1
pkgrel=1
pkgdesc='A scripts to provide option for pacman after installation'
url='https://github.com/Obarun/pacopts.git'
arch=(x86_64)
license=('BEERWARE')
depends=('bash' 'pacman' 'cower' 'shadow' 'obarun-libs' 'expac')
backup=('etc/obarun/pacopts.conf')
makedepends=('git')
source=("${pkgname}::git+${url}#tag=v$pkgver")
validpgpkeys=('6DD4217456569BA711566AC7F06E8FDE7B45DAAC') # Eric Vidal


package() {

	cd "$pkgname"
	
	# install files on good directory
	install -Dm 0755 "$srcdir/$pkgname/pacopts.in" "$pkgdir/usr/bin/pacopts"
	install -Dm 0755 "$srcdir/$pkgname/pacopts.sh" "$pkgdir/usr/lib/obarun/pacopts.sh"
	install -Dm 0755 "$srcdir/$pkgname/tmpfiles.sh.in" "$pkgdir/usr/lib/obarun/tmpfiles.sh"
	install -Dm 0644 "$srcdir/$pkgname/pacopts.conf" "$pkgdir/etc/obarun/pacopts.conf"
	install -Dm 0644 "$srcdir/$pkgname/applytmp.hook" "$pkgdir/usr/share/libalpm/hooks/applytmp.hook"
	install -Dm 0644 "$srcdir/$pkgname/applysys.hook" "$pkgdir/usr/share/libalpm/hooks/applysys.hook"
	install -dm 0755 "$pkgdir/usr/lib/obarun/pacopts/"
	for file in pacopts/{aur.sh,sysusers.sh};do
		install -Dm 0755 "${file}" "$pkgdir/usr/lib/obarun/pacopts/"
	done
	# Install man pages
	install -Dm 0644 "$srcdir/$pkgname/pacopts.1.gz" "$pkgdir/usr/share/man/man1/pacopts.1.gz"
	# Install the licence
	install -Dm 0644 "$srcdir/$pkgbase/LICENSE" "$pkgdir/usr/share/licenses/$pkgname"
}

sha1sums=('SKIP')
