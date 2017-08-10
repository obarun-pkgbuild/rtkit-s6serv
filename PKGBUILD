# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=rtkit-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="rtkit service for s6"
arch=(x86_64)
license=('beerware')
depends=('rtkit' 's6' 's6-rc' 's6-boot')
conflicts=()
install=rtkit-s6serv.install
source=('rtkit.daemon.run.s6'	
		'rtkit.log.run.s6'
		'LICENSE')
md5sums=('98162c2668140476ae0bc3cad81a11ba'
         '868ad8dcadffc3826e8f465ce00a6ff7'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/rtkit.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/rtkit/run"
	
	# log
	install -Dm 0755 "$srcdir/rtkit.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/rtkit/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/rtkit-s6serv/LICENSE"
}
