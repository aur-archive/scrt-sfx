# Maintainer : maz-1 <loveayawaka at gmail dot com>

pkgname=scrt-sfx
pkgver=7.3.1.685
pkgrel=1
pkgdesc="Bundle of two Remote Clients : SecureCRT and SecureFX"
arch=('x86_64' 'i686')
url="http://www.vandyke.com/products/securecrt/"
license=('custom')
depends=('openssl' 'glibc' 'qt4')
source_x86_64=("${pkgname}-${pkgver}.ubuntu13-64.tar.gz::http://storage.live.com/items/EED7455B8FCA288F%211029?a.tar.gz")
md5sums_x86_64=('9905af66853cf42c4718775055cdd4b5')
source_i686=("${pkgname}-${pkgver}.ubuntu13.tar.gz::http://storage.live.com/items/EED7455B8FCA288F%211035?a.tar.gz")
md5sums_i686=('ad85b53b115414d77935fb31a6292cca')
options=('!strip')
package() {
	cd "${srcdir}"/${pkgname}-${pkgver}
	
	install -Dm 755 ./SecureCRT ${pkgdir}/usr/bin/SecureCRT
	install -Dm 755 ./SecureFX ${pkgdir}/usr/bin/SecureFX
	install -Dm 755 ./sfxcl ${pkgdir}/usr/bin/sfxcl
	
	install -Dm 644 ./libQtCore.so.4  ${pkgdir}/usr/lib/scrt-sfx/libQtCore.so.4
	install -Dm 644 ./libQtDBus.so.4  ${pkgdir}/usr/lib/scrt-sfx/libQtDBus.so.4
	install -Dm 644 ./libQtGui.so.4  ${pkgdir}/usr/lib/scrt-sfx/libQtGui.so.4
	install -Dm 644 ./libQtNetwork.so.4  ${pkgdir}/usr/lib/scrt-sfx/libQtNetwork.so.4

	install -Dm 644 ./SecureCRT.desktop ${pkgdir}/usr/share/applications/SecureCRT.desktop
	install -Dm 644 ./SecureFX.desktop ${pkgdir}/usr/share/applications/SecureFX.desktop
	install -Dm 644 ./securecrt_64.png ${pkgdir}/usr/share/vandyke/data/securecrt_64.png
	install -Dm 644 ./securefx_64.png ${pkgdir}/usr/share/vandyke/data/securefx_64.png

	install -Dm 644 ./SecureCRT_HISTORY.txt ${pkgdir}/usr/share/doc/scrt/SecureCRT_HISTORY.txt
	install -Dm 644 ./SecureCRT_README.txt ${pkgdir}/usr/share/doc/scrt/SecureCRT_README.txt
	install -Dm 644 ./SecureCRT_SecureFX_EULA.txt ${pkgdir}/usr/share/doc/scrt/SecureCRT_SecureFX_EULA.txt 
	cp -r ./SecureCRTHelp ${pkgdir}/usr/share/doc/scrt/
	
	install -Dm 644 ./SecureFX_HISTORY.txt ${pkgdir}/usr/share/doc/sfx/SecureFX_HISTORY.txt 
	install -Dm 644 ./SecureFX_README.txt ${pkgdir}/usr/share/doc/sfx/SecureFX_README.txt
	install -Dm 644 ./SecureCRT_SecureFX_EULA.txt ${pkgdir}/usr/share/doc/sfx/SecureCRT_SecureFX_EULA.txt
	cp -r ./SecureFXHelp ${pkgdir}/usr/share/doc/scrt/
	
	install -Dm 644 ./changelog.Debian.gz ${pkgdir}/usr/share/doc/scrt-sfx/changelog.Debian.gz
#	install -Dm 644 ./copyright ${pkgdir}/usr/share/doc/scrt-sfx/copyright
	
	install -Dm 644 ./sfxcl.1.gz  ${pkgdir}/usr/share/man/man1/sfxcl.1.gz

}


