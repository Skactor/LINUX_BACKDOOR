# $FreeBSD: src/bin/ps/Makefile,v 1.25 2004/02/23 20:05:14 johan Exp $
#	@(#)Makefile	8.1 (Berkeley) 6/2/93

PROG=	ps
SRCS=	fmt.c keyword.c nlist.c print.c ps.c
WARNS?=	5
#
# To support "lazy" ps for non root/wheel users
# add -DLAZY_PS to the cflags.  This helps
# keep ps from being an unnecessary load
# on large systems.
#
CFLAGS+=-DLAZY_PS
DPADD=	${LIBM} ${LIBKVM}
LDADD=	-lm -lkvm
#BINGRP=	kmem
#BINMODE=2555

.include <bsd.prog.mk>
