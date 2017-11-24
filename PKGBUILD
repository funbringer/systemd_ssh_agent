# Maintainer: Dmitry Ivanov <ivadmi5@gmail.com>

pkgname=systemd-ssh-agent
pkgver=1.0
pkgrel=1
pkgdesc="systemd unit for ssh agent"
arch=('any')
url="https://github.com/funbringer/systemd_ssh_agent"
license=('MIT')
depends=('openssh' 'systemd')
source=('ssh-agent.service' 'ssh_auth_sock.sh')
md5sums=('0c02ae7352e2d82f2433c97c5b388956'
         '3ba390977185803aa2797048242e4962')

package() {
	install -m 755 -d $pkgdir/etc/systemd/user/
	install -m 755 -d $pkgdir/etc/profile.d/
	install -m 644 ssh-agent.service $pkgdir/etc/systemd/user/
	install -m 644 ssh_auth_sock.sh  $pkgdir/etc/profile.d/
}
