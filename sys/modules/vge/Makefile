# $FreeBSD: releng/11.1/sys/modules/vge/Makefile 319182 2017-05-30 04:11:12Z ngie $

.PATH: ${SRCTOP}/sys/dev/vge

KMOD=	if_vge
SRCS=	if_vge.c miibus_if.h device_if.h bus_if.h pci_if.h
SRCS+= 	opt_netgraph.h

opt_netgraph.h:
	echo "#define NETGRAPH 1" > ${.TARGET}

.include <bsd.kmod.mk>
