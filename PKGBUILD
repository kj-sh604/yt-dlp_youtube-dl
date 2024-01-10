# Maintainer: kj_sh604 
# don't talk to me 
pkgname=yt-dlp_youtube-dl
pkgver=1
pkgrel=1
pkgdesc="Provide both youtube-dl command and python imports using yt-dlp (originally, a symlink for using yt-dlp as a youtube-dl dropin replacement)"
arch=('any')
url="https://github.com/yt-dlp/yt-dlp"
license=('The Unlicense')
makedepends=('python')
depends=('yt-dlp')
provides=('youtube-dl')
conflicts=('youtube-dl' 'yt-dlp-drop-in')

source=(
  "youtube-dl.py"
)

package() {
  depends=('yt-dlp')

  install -Dm755 "${srcdir:?}/youtube-dl.py" "${pkgdir:?}/usr/bin/youtube-dl"

  local _sitepackages="$(python -c 'import site; print(site.getsitepackages()[0])')"
  install -dm755 "${pkgdir:?}${_sitepackages:?}"
  ln -sfT "yt_dlp" "${pkgdir:?}${_sitepackages:?}/youtube_dl"
}
