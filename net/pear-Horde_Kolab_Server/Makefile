# Created by: Martin Matuska <mm@FreeBSD.org>
# $FreeBSD$

PORTNAME=	Horde_Kolab_Server
DISTVERSION=	2.0.5
CATEGORIES=	net www pear
PKGNAMEPREFIX=	pear-

MAINTAINER=	horde@FreeBSD.org
COMMENT=	Horde library for manipulating the Kolab user database

USES=	horde
USE_PHP=	hash
USE_HORDE_RUN=	Horde_Auth \
		Horde_Exception

OPTIONS_DEFAULT=	LDAP
OPTIONS_DEFINE=		LDAP
LDAP_DESC=		Enable LDAP support

# Not required but we want it
USE_HORDE_RUN+=	Horde_Date

LDAP_USE=	HORDE_RUN=Horde_Ldap

.include <bsd.port.mk>
