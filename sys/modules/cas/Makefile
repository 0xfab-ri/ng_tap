# $FreeBSD: releng/11.1/sys/modules/cas/Makefile 319182 2017-05-30 04:11:12Z ngie $

.PATH: ${SRCTOP}/sys/dev/cas

KMOD=	if_cas
SRCS=	bus_if.h device_if.h if_cas.c miibus_if.h pci_if.h ${ofw_bus_if}

.if ${MACHINE_CPUARCH} == "powerpc" || ${MACHINE_ARCH} == "sparc64"
ofw_bus_if=	ofw_bus_if.h
.endif

SRCS+= 	opt_netgraph.h

opt_netgraph.h:
	echo "#define NETGRAPH 1" > ${.TARGET}

.include <bsd.kmod.mk>
