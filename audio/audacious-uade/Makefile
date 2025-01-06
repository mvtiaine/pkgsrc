DISTNAME=	audacious-uade-0.12.4
CATEGORIES=	audio
MASTER_SITES=	https://github.com/mvtiaine/audacious-uade/releases/download/${PKGVERSION_NOREV}/
EXTRACT_SUFX=	.tar.bz2

HOMEPAGE=	https://github.com/mvtiaine/audacious-uade
COMMENT=	UADE plugin for Audacious music player
LICENSE=	gnu-gpl-v2

USE_LANGUAGES=	c c++
USE_CXX_FEATURES+=	c++17 has_include
USE_TOOLS+=	gmake pkg-config
GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	--enable-plugin-audacious=yes
CONFIGURE_ARGS+=	--with-static-stdlibs=no
TEST_TARGET=	check

.include "../../audio/audacious/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
