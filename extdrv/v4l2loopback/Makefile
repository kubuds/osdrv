PWD := $(shell pwd)

ccflags-y += -I$(src) -I$(src)/$(CHIP) -I$(srctree)/drivers/tee

obj-m += v4l2loopback.o

all:
	$(MAKE) ARCH=$(ARCH) -C $(KERNEL_DIR) M=$(PWD) modules

clean:
	rm -f *.o* *.ko
	rm -f Module.symvers modules.order
	rm -rf .tmp_versions
	rm -f .*cmd
	rm -f *.mod.c
	rm -f $(CHIP)/*.o*
	rm -f $(CHIP)/.*cmd
