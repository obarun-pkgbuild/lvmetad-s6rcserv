# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=lvmetad-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="lvmetad service for s6-rc"
arch=(x86_64)
license=('beerware')
depends=('lvm2' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('lvmetad.prepare.dependencies'
		'lvmetad.prepare.type'
		'lvmetad.prepare.up'
		
		'lvmetad.longrun.dependencies'
		'lvmetad.longrun.pipeline-name'
		'lvmetad.longrun.producer-for'
		'lvmetad.longrun.run'
		'lvmetad.longrun.type'	
		
		'lvmetad.log.consumer-for'
		'lvmetad.log.dependencies'
		'lvmetad.log.run'
		'lvmetad.log.type'
		
		'lvmetad.after.dependencies'
		'lvmetad.after.type'
		'lvmetad.after.up'
		
		'bundle.lvmetad.contents'
		'bundle.lvmetad.type'
		'lvmetad.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         'df6e2980da2f008ba8214d2478e3d0ea'
         '9ee5e523aaf03430bef09fa4adcf828d'
         '036c2235c383f64a9241b067ea1a36d9'
         'e63c425506d853c8259545fbcbf3b8ca'
         '418ad9335d610e2c043f63e5e313cd1d'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'f1e13ba6c14d2f41430d5e54dcab62e2'
         '68b329da9893e34099c7d8ad5cb9c940'
         '7c51b2dcd4b10615fc736a668fd17b66'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'f1e13ba6c14d2f41430d5e54dcab62e2'
         '85bceea1fb94d4166f24496dc40a35e6'
         '780906471390587743f0ed86eb0374a2'
         'ef6fd7543b4fe62605eb6fe0e6e0f159'
         '71abe97e2554d37f1d12c5bf4945297f'
         'b9c90e17229ca104f9b3f65f8baa805f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-lvmetad need a maj at lvmetad e.g user-Base
	install -Dm 0644 "$srcdir/bundle.lvmetad.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Lvmetad/contents"
	install -Dm 0644 "$srcdir/bundle.lvmetad.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Lvmetad/type"
	
	#prepare
	install -Dm 0644 "$srcdir/lvmetad.prepare.dependencies" "$pkgdir/etc/s6-serv/available/rc/lvmetad-prepare/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.prepare.type" "$pkgdir/etc/s6-serv/available/rc/lvmetad-prepare/type"
	install -Dm 0644 "$srcdir/lvmetad.prepare.up" "$pkgdir/etc/s6-serv/available/rc/lvmetad-prepare/up"
	
	# longrun
	install -Dm 0644 "$srcdir/lvmetad.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/lvmetad-longrun/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/lvmetad-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/lvmetad.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/lvmetad-longrun/producer-for"
	install -Dm 0644 "$srcdir/lvmetad.longrun.run" "$pkgdir/etc/s6-serv/available/rc/lvmetad-longrun/run"
	install -Dm 0644 "$srcdir/lvmetad.longrun.type" "$pkgdir/etc/s6-serv/available/rc/lvmetad-longrun/type"
	
	#after
	install -Dm 0644 "$srcdir/lvmetad.after.dependencies" "$pkgdir/etc/s6-serv/available/rc/lvmetad-after/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.after.type" "$pkgdir/etc/s6-serv/available/rc/lvmetad-after/type"
	install -Dm 0644 "$srcdir/lvmetad.after.up" "$pkgdir/etc/s6-serv/available/rc/lvmetad-after/up"
	
	# log
	install -Dm 0644 "$srcdir/lvmetad.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/consumer-for"
	install -Dm 0644 "$srcdir/lvmetad.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/dependencies"
	install -Dm 0644 "$srcdir/lvmetad.log.run" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/run"
	install -Dm 0644 "$srcdir/lvmetad.log.type" "$pkgdir/etc/s6-serv/available/rc/lvmetad-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/lvmetad.logd" "$pkgdir/etc/s6-serv/log.d/lvmetad-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/lvmetad-s6rcserv/LICENSE"
}
