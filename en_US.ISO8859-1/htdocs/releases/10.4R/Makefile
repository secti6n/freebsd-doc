# $FreeBSD$

.if exists(../Makefile.conf)
.include "../Makefile.conf"
.endif
.if exists(../Makefile.inc)
.include "../Makefile.inc"
.endif

_OS?=		FreeBSD
_REVISION?=	10.4
_BRANCH?=	RELEASE
THISRELEASE?=	${_OS}-${_REVISION}-${_BRANCH}

DOCS=	index.xml \
	schedule.xml

DATA=	docbook.css

# PGP-signed checksums

_BIGIRON?=	amd64 \
		i386 \
		powerpc \
		powerpc-powerpc64 \
		sparc64

_VMS?=		amd64 \
		i386

_ARM?=		BEAGLEBONE \
		CUBOX-HUMMINGBOARD \
		GUMSTIX \
		PANDABOARD \
		RPI-B \
		WANDBOARD

.for CHECKSUM in SHA512 SHA256
. for _B in ${_BIGIRON}
#DATA+=		CHECKSUM.${CHECKSUM}-${THISRELEASE}-${_B}.asc
. endfor
. for _V in ${_VMS}
#DATA+=		CHECKSUM.${CHECKSUM}-${THISRELEASE}-${_V}-vm.asc
. endfor
. for _A in ${_ARM}
#DATA+=		CHECKSUM.${CHECKSUM}-${THISRELEASE}-arm-armv6-${_A}.asc
. endfor
.endfor

.include "${DOC_PREFIX}/share/mk/web.site.mk"
