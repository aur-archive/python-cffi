# Maintainer: lilydjwg <lilydjwg@gmail.com>
_name=cffi
pkgname=python-${_name}
pkgver=0.8.2
pkgrel=2
pkgdesc="Foreign Function Interface for Python calling C code"
arch=('i686' 'x86_64')
url="http://cffi.readthedocs.org/"
license=('MIT')
depends=('python' 'python-pycparser')
makedepends=('python-setuptools')
md5sums=('37fc88c62f40d04e8a18192433f951ec')
source=("http://pypi.python.org/packages/source/c/${_name}/${_name}-${pkgver}.tar.gz")

build() {
  cd "$srcdir/$_name-$pkgver"

  python3 setup.py build
}

package() {
  cd "$srcdir/$_name-$pkgver"
  python3 setup.py install --root="$pkgdir/" --optimize=1
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
