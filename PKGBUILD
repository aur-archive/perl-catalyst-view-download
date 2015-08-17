# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-catalyst-view-download'
pkgver='0.09'
pkgrel='1'
pkgdesc=""
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl')
makedepends=('perl-catalyst-runtime' 'perl-test-use-ok' 'perl-test-www-mechanize-catalyst' 'perl-text-csv' 'perl-xml-simple')
url='http://search.cpan.org/dist/Catalyst-View-Download'
source=('http://search.cpan.org/CPAN/authors/id/G/GA/GAUDEON/Catalyst-View-Download-0.09.tar.gz')
md5sums=('98a803d8e7683a2535d1e7a6db0fbbc8')
sha512sums=('f7987e1e1e7eb505d9139d0aa0d3937107aa9922c44ff398c7eb5e8a1807e8223c3121572c68340a2b96d38922504d9b8da06abf2603dcc855ae7c9dbe7a9915')
_distdir="Catalyst-View-Download-0.09"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
