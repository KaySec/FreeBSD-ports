# Created by: Gea-Suan Lin <gslin@gslin.org>
# $FreeBSD$

PORTNAME=	memcached
PORTVERSION=	3.0.4
CATEGORIES=	databases

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	PHP extension for interfacing with memcached via libmemcached library

LICENSE=	PHP30
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	libmemcached>=1.0.18:databases/libmemcached
LIB_DEPENDS=	libmemcached.so:databases/libmemcached

OPTIONS_DEFINE=	IGBINARY SASL
OPTIONS_DEFAULT=SASL
IGBINARY_DESC=	Binary serializer support

CONFIGURE_ARGS=	--with-libmemcached-dir=${LOCALBASE}
IGNORE_WITH_PHP=56
USE_PHP=	json:build session:build
USES=		php:pecl pkgconfig

IGBINARY_CONFIGURE_ENABLE=	memcached-igbinary
IGBINARY_USE=		PHP=igbinary:build
SASL_CONFIGURE_ENABLE=	memcached-sasl
SASL_LIB_DEPENDS=	libsasl2.so:security/cyrus-sasl2

.include <bsd.port.mk>
