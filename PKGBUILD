# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=googlecharts
pkgname=ruby-$_gemname
pkgver=1.6.8
pkgrel=1
pkgdesc='Generate charts using Google API & Ruby'
arch=(any)
url='http://googlecharts.rubyforge.org/'
license=(MIT)
depends=(ruby)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('24d4677f2739c50085f07c57676818d2402e684f')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/License.txt" "$pkgdir/usr/share/licenses/$pkgname/License.txt"
}
