# SPDX-License-Identifier: GPL-2.0
#
# Makefile for the linux ext4-filesystem routines.
#

obj-m += ext4_pmkv.o

ext4_pmkv-y	:= acl.o balloc.o bitmap.o block_validity.o dir.o ext4_jbd2.o extents.o \
		extents_status.o file.o fsmap.o fsync.o hash.o ialloc.o \
		indirect.o inline.o inode.o ioctl.o mballoc.o migrate.o \
		mmp.o move_extent.o namei.o page-io.o readpage.o resize.o \
		super.o symlink.o sysfs.o verity.o xattr.o xattr_hurd.o xattr_security.o xattr_trusted.o \
		xattr_user.o fast_commit.o orphan.o

#ext4-$(CONFIG_EXT4_FS_POSIX_ACL)	+= acl.o
#ext4-$(CONFIG_EXT4_FS_SECURITY)		+= xattr_security.o
#ext4-inode-test-objs			+= inode-test.o
#obj-$(CONFIG_EXT4_KUNIT_TESTS)		+= ext4-inode-test.o
#ext4-$(CONFIG_FS_VERITY)		+= verity.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=`pwd`

clean:
	make -C /lib/modules/$(shell uname -r)/build M=`pwd` clean

