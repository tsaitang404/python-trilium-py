# Maintainer: tsaitang404 <tsaitang404@gmail.com>
# Follows upstream: Nriver/trilium-py (https://github.com/Nriver/trilium-py)
# Python client for Trilium Notes ETAPI + Web API, with extra features.

pkgname=python-trilium-py
pkgver=1.3.9
pkgrel=1
pkgdesc="Feature-rich Python client for interacting with the API and ETAPI of Trilium Notes"
arch=('any')
url="https://github.com/Nriver/trilium-py"
license=('AGPL-3.0-or-later')
depends=('python-requests' 'python-markdown2')
makedepends=('python-build' 'python-installer' 'python-wheel')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/Nriver/trilium-py/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('SKIP')
b2sums=('SKIP')

build() {
    cd "trilium-py-${pkgver}"
    python -m build --wheel --no-isolation
}

package() {
    cd "trilium-py-${pkgver}"
    python -m installer --destdir="$pkgdir" dist/*.whl
}
