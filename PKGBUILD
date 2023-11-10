# Maintainer: kj_sh604 
# don't talk to me 
pkgname=yt-dlp_youtube-dl
pkgver=1
pkgrel=1
pkgdesc="A symlink for using yt-dlp as a youtube-dl dropin replacement"
arch=('any')
url="https://github.com/yt-dlp/yt-dlp"
license=('The Unlicense')
depends=('yt-dlp')
provides=('youtube-dl')
conflicts=('youtube-dl' 'yt-dlp-drop-in')

package() {
  install -d "$pkgdir"/usr/bin
  ln -s $(which yt-dlp) "$pkgdir"/usr/bin/youtube-dl
}
