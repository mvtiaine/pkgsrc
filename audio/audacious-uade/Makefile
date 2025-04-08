DISTNAME=	audacious-uade-0.13.1
CATEGORIES=	audio
MASTER_SITES=	https://github.com/mvtiaine/audacious-uade/releases/download/${PKGVERSION_NOREV}/
EXTRACT_SUFX=	.tar.bz2

HOMEPAGE=	https://github.com/mvtiaine/audacious-uade
COMMENT=	UADE plugin for Audacious and DeaDBeeF
LICENSE=	gnu-gpl-v2

USE_LANGUAGES=	c c++
USE_CXX_FEATURES+=	c++17 has_include
USE_TOOLS+=	gmake pkg-config
GNU_CONFIGURE=	yes

# TODO DeaDBeeF support does not work, needs separate deadbeef option for PLIST
CONFIGURE_ARGS+=	--enable-plugin-deadbeef=no
# (optional) install DeaDBeeF from https://pkgsrc.se/wip/deadbeef
# needed for DeaDBeeF support
#CPPFLAGS+=	-isystem${PREFIX}/include

CONFIGURE_ARGS+=	--enable-players=all
CONFIGURE_ARGS+=	--enable-plugin-audacious=yes
CONFIGURE_ARGS+=	--with-static-stdlibs=no
TEST_TARGET=	check

# XXX needed to find/link libopenmpt
.include "../../audio/mpg123/buildlink3.mk"
.include "../../audio/libvorbis/buildlink3.mk"
.include "../../multimedia/libogg/buildlink3.mk"

.include "../../audio/libopenmpt/buildlink3.mk"
.include "../../audio/libxmp/buildlink3.mk"
.include "../../audio/audacious/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
