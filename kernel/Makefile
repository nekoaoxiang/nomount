MODULE_NAME := nomount

# 模块目标与依赖的源文件
obj-m += $(MODULE_NAME).o
$(MODULE_NAME)-objs := src/nomount.o

# DDK 默认内核头文件目录（Android 14 6.1 KMI）
KDIR ?= /opt/ddk/kdir/android14-6.1
PWD := $(shell pwd)

all:
	$(MAKE) -C $(KDIR) M=$(PWD) modules

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean