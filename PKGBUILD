# Maintainer: Michael Haggerty <mhagger@github.com>

_realname="git-sizer"
pkgname=("${_realname}")
pkgver=1.5.0
pkgrel=1
pkgdesc="Compute various size metrics for a Git repository, flagging those that might cause problems"
arch=('any')
url="https://github.com/github/git-sizer"
src_zip_url="${url}/archive/v${pkgver}.zip"
license=('MIT')
groups=('VCS')

case "$CARCH" in
i686)
  zipname="git-sizer-$pkgver-windows-386.zip"
  sha256sum=55930026eb444f8f852e03716525067bfc4a0329a9c778b026da150a8ed8abd8
  ;;
x86_64)
  zipname="git-sizer-$pkgver-windows-amd64.zip"
  sha256sum=52093c1cba0bb8e00da14c9eef678eb052fc729c32419415817076f06b5c85d8
  ;;
esac

source=("https://github.com/github/git-sizer/releases/download/v$pkgver/$zipname"
	"$src_zip_url")

sha256sums=("$sha256sum" SKIP)
options=('!strip')

package() {
  install -d -m755 $pkgdir/$MSYSTEM_PREFIX/bin
  install -m755 $srcdir/git-sizer.exe $pkgdir/$MSYSTEM_PREFIX/bin/git-sizer.exe
  install -d -m755 $pkgdir/$MSYSTEM_PREFIX/share/doc/git-sizer
  install -m644 $srcdir/README.md $pkgdir/$MSYSTEM_PREFIX/share/doc/git-sizer/README.md
}
