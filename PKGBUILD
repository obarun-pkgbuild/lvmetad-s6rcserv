# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=lvmetad-s6rcserv
pkgver=0.1
pkgrel=1
pkgdesc="lvmetad service for s6-rc"
arch=(x86_64)
license=('beerware')
depends=('lvm2' 's6' 's6-rc' 's6-boot')
conflicts=()
install=lvmetad-s6rcserv.install
source=('lvmetad.prepare.dependencies.s6'
		'lvmetad.prepare.type.s6'
		'lvmetad.prepare.up.s6'
		
		'lvmetad.daemon.dependencies.s6'
		'lvmetad.daemon.pipeline-name.s6'
		'lvmetad.daemon.producer-for.s6'
		'lvmetad.daemon.run.s6'
		'lvmetad.daemon.type.s6'	
		
		'lvmetad.log.consumer-for.s6'
		'lvmetad.log.dependencies.s6'
		'lvmetad.log.run.s6'
		'lvmetad.log.type.s6'
		
		'lvmetad.after.dependencies.s6'
		'lvmetad.after.type.s6'
		'lvmetad.after.up.s6'
		
		'bundle.lvmetad.contents.s6'
		'bundle.lvmetad.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         'df6e2980da2f008ba8214d2478e3d0ea'
         '9ee5e523aaf03430bef09fa4adcf828d'
         '036c2235c383f64a9241b067ea1a36d9'
         'e63c425506d853c8259545fbcbf3b8ca'
         '418ad9335d610e2c043f63e5e313cd1d'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'e3aae33579e70e8605e6486e28452630'
         '68b329da9893e34099c7d8ad5cb9c940'
         '7c51b2dcd4b10615fc736a668fd17b66'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'e3aae33579e70e8605e6486e28452630'
         '85bceea1fb94d4166f24496dc40a35e6'
         '399b96372c52ce30a2502b36c002f234'
         'ca94b609773f227cbcd65a7205f2aed0'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-lvmetad need a maj at lvmetad e.g user-Base
	install -Dm 0644 "$srcdir/bundle.lvmetad.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Lvmetad/contents"
	install -Dm 0644 "$srcdir/bundle.lvmetad.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Lvmetad/type"
	
	#prepare
	install -Dm 0644 "$srcdir/lvmetad.prepare.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-prepare/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.prepare.type.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-prepare/type"
	install -Dm 0644 "$srcdir/lvmetad.prepare.up.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-prepare/up"
	
	# daemon
	install -Dm 0644 "$srcdir/lvmetad.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-daemon/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/lvmetad.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-daemon/producer-for"
	install -Dm 0644 "$srcdir/lvmetad.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-daemon/run"
	install -Dm 0644 "$srcdir/lvmetad.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-daemon/type"
	
	#after
	install -Dm 0644 "$srcdir/lvmetad.after.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-after/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.after.type.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-after/type"
	install -Dm 0644 "$srcdir/lvmetad.after.up.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-after/up"
	
	# log
	install -Dm 0644 "$srcdir/lvmetad.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/consumer-for"
	install -Dm 0644 "$srcdir/lvmetad.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/run"
	install -Dm 0644 "$srcdir/lvmetad.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/lvmetad-s6rcserv/LICENSE"
}
